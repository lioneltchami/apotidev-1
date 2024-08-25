<template>
    <section class="contact-area">
        <div class="container-fluid">
            <div class="row">
                <div class="col-lg-12">
                    <div class="contact-colunm">
                        <div class="contact-form">
                            <form class="contact-form-wrapper" ref="form" @submit.prevent="sendEmail">
                                <div class="row">
                                    <div class="col-lg-12">
                                        <div class="section-title">
                                            <h5 class="subtitle line-theme-color">Contact Us Now</h5>
                                            <h2 class="title">Get In Touch.</h2>
                                            <p>Want to connect? Please don't hesitate to email us. We will reply to your email swiftly. God bless you & thank you.</p>
                                        </div>
                                    </div>
                                </div>
                                <div class="row">
                                    <div class="col-lg-12">
                                        <div class="row row-gutter-20">
                                            <div class="col-md-12">
                                                <div class="form-group">
                                                    <input class="form-control" type="text" name="from_name" placeholder="Full Name" required pattern="[A-Za-z\s]+">
                                                </div>
                                            </div>
                                            <div class="col-md-12">
                                                <div class="form-group">
                                                    <input class="form-control" type="email" name="to_name" placeholder="Email Address" required>
                                                </div>
                                            </div>
                                            <div class="col-md-12">
                                                <div class="form-group">
                                                    <input class="form-control" type="text" name="phone" placeholder="Phone Number" pattern="\d{10,15}" title="Please enter a valid phone number">
                                                </div>
                                            </div>
                                            <div class="col-md-12">
                                                <div class="form-group mb-0">
                                                    <textarea class="form-control textarea" name="message" placeholder="Message" required></textarea>
                                                </div>
                                            </div>
                                            <div class="col-md-12">
                                                <div class="form-group mb-0">
                                                    <button class="btn-theme btn-gradient btn-slide no-border" type="submit">Send Message</button>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </form>
                        </div>
                        <div class="contact-map-area">
                            <div class="contact-info-content">
                                <div class="contact-info-item">
                                    <div class="icon">
                                        <img class="icon-img" src="/images/icons/c1.png" alt="Icon">
                                    </div>
                                    <div class="content">
                                        <h4>Phone</h4>
                                        <img class="line-icon" src="/images/shape/line-s1.png" alt="Image-Givest">
                                        <a href="tel:0123456789">+1 (587) 432 0753</a>
                                        <a href="tel:0123456789">(+237) 672 274 959</a>
                                    </div>
                                </div>
                                <div class="contact-info-item">
                                    <div class="icon icon-mail">
                                        <img class="icon-img" src="/images/icons/c2.png" alt="Icon">
                                    </div>
                                    <div class="content">
                                        <h4>Email</h4>
                                        <img class="line-icon" src="/images/shape/line-s1.png" alt="Image-Givest">
                                        <a href="mailto://info@apotidev.org">info@apotidev.org</a>
                                        <a href="mailto://volunteer@apotidev.org">volunteer@apotidev.org</a>
                                    </div>
                                </div>
                                <div class="contact-info-item mb-0 pb-0">
                                    <div class="icon icon-location">
                                        <img class="icon-img" src="/images/icons/c3.png" alt="Icon">
                                    </div>
                                    <div class="content">
                                        <h4>Address</h4>
                                        <img class="line-icon" src="/images/shape/line-s1.png" alt="Image-Givest">
                                        <p>140 10th Ave SW, Calgary, CA <br>17 Street NW Clerks Quaters, Buea, CMR</p>
                                    </div>
                                </div>
                            </div>
                            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d10000!2d-114.0719!3d51.0447!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x53716f9f5f9e5b3b%3A0x7c9e9d8b9e6b6f9!2sCalgary%2C%20AB%2C%20Canada!5e0!3m2!1sen!2sca!4v1714302644672"></iframe>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<!--<script>-->
<!--    import Volunteer from "~/pages/volunteer.vue";-->

<!--    export default {-->
<!--      components: {Volunteer}-->

<!--    };-->
<!--</script>-->
<script>
import emailjs from 'emailjs-com';
import Volunteer from "~/pages/volunteer.vue";

export default {
  components: { Volunteer },
  methods: {
    sendEmail(event) {
      // Additional JavaScript validation
      const form = this.$refs.form;
      const name = form.querySelector('input[name="from_name"]').value;
      const email = form.querySelector('input[name="to_name"]').value;
      const phone = form.querySelector('input[name="phone"]').value;
      const message = form.querySelector('textarea[name="message"]').value;

      const emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
      const namePattern = /^[A-Za-z\s]+$/;
      const phonePattern = /^\d{10,15}$/;

      if (!namePattern.test(name)) {
        alert('Please enter a valid name.');
        return;
      }
      if (!emailPattern.test(email)) {
        alert('Please enter a valid email address.');
        return;
      }
      if (phone && !phonePattern.test(phone)) {
        alert('Please enter a valid phone number.');
        return;
      }
      if (!message) {
        alert('Please enter a message.');
        return;
      }

      // If validation passes, send the email
      emailjs.sendForm('service_nu6zgna', 'template_hreifr8', form, 'hWCCGr-8vhbtD2mdm')
          .then(() => {
            alert('Thank you for your message. We will get back to you shortly.');
            window.location.reload(); // Refresh the page after successful email send
          }, (error) => {
            alert('Failed to send message: ' + error.text);
          });
    }
  }
}
</script>