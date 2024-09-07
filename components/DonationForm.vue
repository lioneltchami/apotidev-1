<template>
  <div class="donation-form bgcolor-theme3">
    <div class="section-title">
      <h5 class="subtitle line-theme-color mb-14">Make A Donation</h5>
      <h2 class="title text-white">Donate Now</h2>
      <img class="line-shape" src="/images/shape/line-t3.png" alt="image">
    </div>
    <form @submit.prevent="submitDonation">
      <div class="amount-info">
        <div v-for="amount in predefinedAmounts" :key="amount"
             class="donate-amount"
             :class="{ 'active': selectedAmount === amount }"
             @click="selectAmount(amount)">
          ${{ amount }}
        </div>
        <div class="donate-amount donate-custom-amount">
          <input class="form-control" type="number" v-model="customAmount" placeholder="Custom" @input="updateCustomAmount">
        </div>
      </div>
      <div class="payment-method-wrp">
        <h4>Payment Method:</h4>
        <div class="payment-method">
          <div class="payment-type">
            <div class="form-check form-check-inline">
              <input class="form-check-input" type="radio" id="stripeRadio" value="stripe" v-model="paymentMethod">
              <label class="form-check-label" for="stripeRadio">Credit Card (Stripe)</label>
            </div>
          </div>
          <img src="/images/photos/payment-card.png" alt="image">
        </div>
      </div>
      <div v-if="paymentMethod === 'stripe'" class="stripe-element-container">
        <div id="card-element"></div>
        <div id="card-errors" role="alert"></div>
      </div>
      <div class="personal-info">
        <h4>Personal Info:</h4>
        <div class="row row-gutter-20">
          <div class="col-md-6">
            <div class="form-group">
              <input class="form-control" type="text" v-model="name" placeholder="Name" required>
            </div>
          </div>
          <div class="col-md-6">
            <div class="form-group">
              <input class="form-control" type="email" v-model="email" placeholder="Email" required>
            </div>
          </div>
        </div>
      </div>
      <div class="btn-wrp">
        <button type="submit" class="btn-theme btn-gradient btn-slide">
          Donate Now <img class="icon icon-img" src="/images/icons/arrow-line-right2.png" alt="Icon">
        </button>
        <div class="btn-theme btn-gradient btn-border">Total Donation: ${{ totalAmount }}</div>
      </div>
    </form>
    <div class="layer-style">
      <img class="layer-style1" src="/images/shape/form-shape1.png" alt="image">
      <img class="layer-style2" src="/images/shape/form-shape2.png" alt="image">
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      predefinedAmounts: [20, 50, 200],
      selectedAmount: null,
      customAmount: '',
      paymentMethod: 'stripe',
      name: '',
      email: '',
      stripe: null,
      cardElement: null,
      stripeLoaded: false,
    };
  },
  computed: {
    totalAmount() {
      return this.selectedAmount || parseFloat(this.customAmount) || 0;
    },
  },
  mounted() {
    this.loadStripe();
  },
  methods: {
    loadStripe() {
      if (typeof Stripe === 'undefined') {
        const script = document.createElement('script');
        script.src = 'https://js.stripe.com/v3/';
        script.onload = () => {
          this.stripeLoaded = true;
          this.initializeStripe();
        };
        document.head.appendChild(script);
      } else {
        this.stripeLoaded = true;
        this.initializeStripe();
      }
    },
    initializeStripe() {
      if (!this.stripeLoaded) return;

      const stripeKey = process.env.VUE_APP_STRIPE_PUBLISHABLE_KEY;
      if (!stripeKey) {
        console.error('Stripe publishable key is missing');
        return;
      }

      this.stripe = Stripe(stripeKey);
      const elements = this.stripe.elements();
      this.cardElement = elements.create('card');

      this.$nextTick(() => {
        const mountElement = document.getElementById('card-element');
        if (mountElement) {
          this.cardElement.mount('#card-element');
          this.cardElement.on('change', (event) => {
            const displayError = document.getElementById('card-errors');
            if (displayError) {
              displayError.textContent = event.error ? event.error.message : '';
            }
          });
        } else {
          console.error('Card element mount point not found');
        }
      });
    },
  },
};
</script>

<style scoped>
.donate-amount.active {
  background-color: #13373e;
  color: white;
}
.stripe-element-container {
  margin-bottom: 20px;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 4px;
}
#card-element {
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 4px;
}
#card-errors {
  color: #fa755a;
  text-align: left;
  font-size: 13px;
  line-height: 17px;
  margin-top: 12px;
}
</style>