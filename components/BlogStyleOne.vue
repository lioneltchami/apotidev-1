<template>
    <section class="blog-area blog-default-area">
        <div class="container">
            <div class="row">
                <div class="col-md-8 col-lg-6 m-auto">
                    <div class="section-title text-center" data-aos="fade-up" data-aos-duration="1000">
                        <h5 class="subtitle line-theme-color">Blog Post</h5>
                        <h2 class="title title-style">Latest News From our Blog <img class="img-shape" src="/images/shape/3.png" alt="Image-ADA"></h2>
                    </div>
                </div>
            </div>
            <div class="row mtn-150" data-aos="fade-up" data-aos-duration="1000">
                <div class="col-md-6 col-lg-4 mt-150" v-for="(blog, index) in blogs" :key="index">
                    <div class="post-item">
                        <div class="thumb">
                            <a href="https://apotidev.substack.com/" target="_blank" rel="noopener noreferrer">
                                <img :src="blog.imgSrc" :alt="blog.title">
                            </a>
                            <div class="meta-date">
                                <a href="https://apotidev.substack.com/" target="_blank" rel="noopener noreferrer"><span>{{ blog.metaDate }}</span> {{ blog.metaMonth }}</a>
                            </div>
                            <div class="shape-line"></div>
                        </div>
                        <div class="content">
                            <div class="inner-content">
                                <div class="meta">
                                    <a href="https://apotidev.substack.com/" target="_blank" rel="noopener noreferrer">{{ blog.category }}</a>
                                    <div class="post-share">
                                        <button class="icon-share">
                                            <img src="/images/icons/share-line-gradient.png" alt="Icon">
                                        </button>
                                        <ul>
                                            <li v-for="(social, index) in blog.socials" :key="index">
                                                <a :href="social.url" :class="social.addColorClass">
                                                    <i :class="social.icon"></i>
                                                </a>
                                            </li>
                                        </ul>
                                    </div>
                                </div>
                                <h4 class="title">
                                    <a href="https://apotidev.substack.com/" target="_blank" rel="noopener noreferrer">{{ blog.title }}</a>
                                </h4>
                                <p>{{ blog.desc }}</p>
                            </div>
                            <div class="post-footer">
                                <a href="https://apotidev.substack.com/" target="_blank" rel="noopener noreferrer" class="btn-theme btn-border-gradient btn-size-xs">
                                    <span>Details <img class="icon icon-img" src="/images/icons/arrow-line-right-gradient.png" alt="Icon"></span>
                                </a>
                                <a href="https://apotidev.substack.com/" target="_blank" rel="noopener noreferrer" class="post-author">By: Robbins</a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        data() {
            return {
                blogs: [
                    {
                        imgSrc: "/images/blog/1.jpg",
                        metaDate: 15,
                        metaMonth: "June",
                        category: "Finances",
                        title: "Why do people really donate? Ever wondered ?",
                        desc: "Understanding the motivations behind donations to better connect with potential supporters.",
                        socials: [
                            {
                                icon: "icofont-facebook",
                                url: "#",
                                addColorClass: "color-facebook"
                            },
                            {
                                icon: "icofont-twitter",
                                url: "#",
                                addColorClass: "color-twitter"
                            },
                            {
                                icon: "icofont-dribbble",
                                url: "#",
                                addColorClass: "color-dribbble"
                            },
                            {
                                icon: "icofont-pinterest",
                                url: "#",
                                addColorClass: "color-pinterest"
                            }
                        ]
                    },
                    {
                        imgSrc: "/images/blog/2.jpg",
                        metaDate: 10,
                        metaMonth: "July",
                        category: "Health",
                        title: "Technology grants for nonprofits",
                        desc: "Explore available technology grants and discounts to enhance your non-profit's operations.",
                        socials: [
                            {
                                icon: "icofont-facebook",
                                url: "#",
                                addColorClass: "color-facebook"
                            },
                            {
                                icon: "icofont-twitter",
                                url: "#",
                                addColorClass: "color-twitter"
                            },
                            {
                                icon: "icofont-dribbble",
                                url: "#",
                                addColorClass: "color-dribbble"
                            },
                            {
                                icon: "icofont-pinterest",
                                url: "#",
                                addColorClass: "color-pinterest"
                            }
                        ]
                    },
                    {
                        imgSrc: "/images/blog/3.jpg",
                        metaDate: 17,
                        metaMonth: "March",
                        category: "Water",
                        title: "Is Your Website Truly Working for Your Non-Profit?",
                        desc: "Evaluate your website's effectiveness in engaging supporters and achieving your non-profit's goals.",
                        socials: [
                            {
                                icon: "icofont-facebook",
                                url: "#",
                                addColorClass: "color-facebook"
                            },
                            {
                                icon: "icofont-twitter",
                                url: "#",
                                addColorClass: "color-twitter"
                            },
                            {
                                icon: "icofont-dribbble",
                                url: "#",
                                addColorClass: "color-dribbble"
                            },
                            {
                                icon: "icofont-pinterest",
                                url: "#",
                                addColorClass: "color-pinterest"
                            }
                        ]
                    },
                ]
            }
        },
    };
</script>
