<template>
    <section class="donate-area donate-default-area bgcolor-theme3">
        <div class="container">
            <div class="row">
                <div class="col-lg-7 col-xxl-7">
                    <div class="content" data-aos="fade-up" data-aos-duration="1000">
                        <div class="section-title">
                            <h5 class="subtitle line-theme-color mb-7">Make A Donation</h5>
                            <h2 class="title title-style text-white">Need Pure Water For Mozambique People.
                                <img class="img-shape" src="/images/shape/3.png" alt="Image">
                            </h2>
                        </div>
                        <div class="donate-form">
                            <form action="#">
                                <div class="amount-info">
                                    <a href="javascript:void(0)" class="donate-amount">$20</a>
                                    <a href="javascript:void(0)" class="donate-amount">$50</a>
                                    <a href="javascript:void(0)" class="donate-amount">$200</a>
                                    <div class="donate-amount donate-custom-amount">
                                        <input class="form-control" type="text" placeholder="Custom">
                                    </div>
                                </div>
                                <div class="btn-wrp">
                                    <a href="javascript:void(0)" class="btn-theme btn-gradient btn-slide">
                                        Donate Now
                                        <img class="icon icon-img" src="/images/icons/arrow-line-right2.png" alt="Icon">
                                    </a>
                                    <nuxt-link to="/causes" class="btn-theme btn-gradient btn-border">
                                        View Causes
                                        <img class="icon icon-img" src="/images/icons/arrow-line-right2-gradient.png" alt="Icon">
                                    </nuxt-link>
                                </div>
                            </form>
                        </div>
                    </div>
                </div>
                <div class="col-lg-5 col-xxl-4 offset-xxl-1 position-static">
                    <div class="donners-content">
                        <div class="thumb-bg-layer" :style="{ backgroundImage: `url('/images/photos/bg-donate1.jpg')` }"></div>
                        <div class="donners-info" data-aos="fade-up" data-aos-duration="1000">
                            <h3>We appreciate your generous support</h3>
                            <p>Your contributions got us started and made a real difference in the lives of those we serve every day. Thank you.</p>
                            <div class="donners-item">
                                <div class="donner-item">
                                    <img src="/images/photos/donner1.png" alt="Image">
                                </div>
                                <div class="donner-item">
                                    <img src="/images/photos/donner2.png" alt="Image">
                                </div>
                                <div class="donner-item">
                                    <img src="/images/photos/donner3.png" alt="Image">
                                </div>
                                <div class="donner-item donner-number">+16</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>