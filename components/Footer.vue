<template>
    <footer class="footer-area" :style="{ backgroundImage: `url('/images/shape/footer-line.png')` }">
        <div class="footer-main">
            <div class="container">
                <div class="row mtn-40">
                    <div class="col-sm-12 col-md-6 col-lg-4 col-xl-4 mt-40">
                        <div class="widget-item">
                            <div class="about-widget">
                                <nuxt-link to="/" class="footer-logo">
                                    <img src="/images/logo/logo.png" alt="Logo">
                                </nuxt-link>
                                <p>Our mission is to support communities in need. Join us in making a difference and spreading hope where it's most needed.</p>
                                <div class="widget-total-raised">
                                    <h4 class="raised-title">Total Contributed:</h4>
                                    <div class="raised-amount">$8,965</div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="col-sm-6 col-md-6 col-lg-4 col-xl-4 mt-40">
                        <div class="widget-item">
                            <h4 class="widget-title line-style">Photo Gallery</h4>
                            <div class="widget-gallery">
                                <div class="row row-cols-3 row-gutter-10 mtn-10">
                                    <div class="col mt-10">
                                        <div class="gallery-item">
                                            <img src="/images/photos/gallery1.jpg" alt="image">
                                            <a class="icon" href="#">
                                                <i class="icofont-instagram"></i>
                                            </a>
                                        </div>
                                    </div>
                                    <div class="col mt-10">
                                        <div class="gallery-item">
                                            <img src="/images/photos/gallery2.jpg" alt="image">
                                            <a class="icon" href="#">
                                                <i class="icofont-instagram"></i>
                                            </a>
                                        </div>
                                    </div>
                                    <div class="col mt-10">
                                        <div class="gallery-item">
                                            <img src="/images/photos/gallery3.jpg" alt="image">
                                            <a class="icon" href="#">
                                                <i class="icofont-instagram"></i>
                                            </a>
                                        </div>
                                    </div>
                                    <div class="col mt-10">
                                        <div class="gallery-item">
                                            <img src="/images/photos/gallery4.jpg" alt="image">
                                            <a class="icon" href="#">
                                                <i class="icofont-instagram"></i>
                                            </a>
                                        </div>
                                    </div>
                                    <div class="col mt-10">
                                        <div class="gallery-item">
                                            <img src="/images/photos/gallery5.jpg" alt="image">
                                            <a class="icon" href="#">
                                                <i class="icofont-instagram"></i>
                                            </a>
                                        </div>
                                    </div>
                                    <div class="col mt-10">
                                        <div class="gallery-item">
                                            <img src="/images/photos/gallery6.jpg" alt="image">
                                            <a class="icon" href="#">
                                                <i class="icofont-instagram"></i>
                                            </a>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="col-sm-6 col-md-6 col-lg-4 col-xl-4 mt-40">
                        <div class="widget-item menu-wrap-two-column">
                            <h4 class="widget-title line-style">Quick Links</h4>
                            <div class="widget-menu-wrap">
                                <div class="row">
                                    <div class="col-6">
                                        <ul class="nav-menu nav">
                                            <li><a href="/causes">Causes</a></li>
                                            <li><a href="/volunteer">Gallery</a></li>
                                            <li><a href="/privacy-policy">Privacy Policy</a></li>
                                            <li><a href="/volunteer">Project Reports</a></li>
                                        </ul>
                                    </div>
                                    <div class="col-6">
                                        <ul class="nav-menu nav align-right">
                                            <li><a href="https://apotidev.substack.com/" target="_blank" rel="noopener noreferrer">Blog</a></li>
                                            <li><a href="/donation">Donate</a></li>
                                            <li><a href="/event-details">Events</a></li>
                                            <li><a href="/volunteer">Volunteer</a></li>
                                        </ul>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="footer-bottom">
            <div class="container">
                <div class="footer-bottom-content">
                    <div class="row align-items-center">
                        <div class="col-12">
                            <div class="widget-copyright text-center">
                                <p>&copy; 2024 <span>Apoti Dev Association</span> Made with <i class="icofont-heart-alt"></i> by <a href="https://apotitech.com">Apoti Tech Inc</a></p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
    export default {

    };
</script>