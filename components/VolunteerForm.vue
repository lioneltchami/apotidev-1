<template>
    <section class="volunteer-form-area">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <div class="volunteer-form">
                        <div class="section-title">
                            <h5 class="subtitle">Volunteer with Us</h5>
                            <h2 class="title">Want to make a difference? Join Us <span>As A Volunteer.</span></h2>
                            <p>We invite you to join our mission to support those in need. Volunteering with ADA lets you contribute to impactful outreach efforts for widows, orphans, young girls, and vulnerable communities. Your efforts can create lasting change through training, donations, educational programs, and more. Together, we can build a brighter future for all.</p>
                        </div>
                        <form class="volunteer-form-wrapper" ref="form" @submit.prevent="sendEmail">
                            <div class="row">
                                <div class="col-lg-12">
                                    <div class="row row-gutter-20">
                                        <div class="col-md-4">
                                            <div class="form-group">
                                                <input class="form-control" type="text" name="from_name" placeholder="Full Name" required pattern="[A-Za-z\s]+">
                                            </div>
                                        </div>
                                        <div class="col-md-4">
                                            <div class="form-group">
                                                <input class="form-control" type="email" name="to_name" placeholder="Email Address" required>
                                            </div>
                                        </div>
                                        <div class="col-md-4">
                                            <div class="form-group">
                                                <input class="form-control" type="text" name="phone" placeholder="Phone Number" pattern="\d{10,15}" title="Please enter a valid phone number">
                                            </div>
                                        </div>
<!--                                        <div class="col-md-4">-->
<!--                                            <div class="form-group">-->
<!--                                                <input class="form-control" type="text" name="con_age" placeholder="Age">-->
<!--                                            </div>-->
<!--                                        </div>-->
<!--                                        <div class="col-md-4">-->
<!--                                            <div class="form-group">-->
<!--                                                <input class="form-control" type="text" name="con_religion" placeholder="Religion">-->
<!--                                            </div>-->
<!--                                        </div>-->
<!--                                        <div class="col-md-4">-->
<!--                                            <div class="form-group">-->
<!--                                                <input class="form-control" type="text" name="con_phone" placeholder="Phone">-->
<!--                                            </div>-->
<!--                                        </div>-->
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
                </div>
            </div>
        </div>
    </section>
</template>

