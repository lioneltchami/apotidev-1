<template>
    <section class="blog-grid-area">
        <div class="container">
            <div class="row">
                <div class="col-12">
                    <div class="blog-content-column">
                        <div class="blog-content-area post-items-style2">
                            <div class="post-item" v-for="(blog, index) in blogs" :key="index">
                                <div class="thumb">
                                    <nuxt-link to="/blog-details">
                                        <img :src="blog.imgSrc" :alt="blog.title">
                                    </nuxt-link>
                                    <div class="meta-date">
                                        <nuxt-link to="/blog"><span>{{ blog.day }}</span>{{ blog.month }}</nuxt-link>
                                    </div>
                                    <div class="shape-line"></div>
                                </div>
                                <div class="content">
                                    <div class="inner-content">
                                        <div class="meta">
                                            <nuxt-link to="/blog" class="post-category">{{ blog.category }}</nuxt-link>
                                            <nuxt-link to="/blog" class="post-author">
                                                <span class="icon">
                                                    <img class="icon-img" src="/images/icons/admin1.png" alt="Icon-Image">
                                                </span>By: {{ blog.author }}
                                            </nuxt-link>
                                        </div>
                                        <h4 class="title">
                                        <nuxt-link to="/blog-details">{{ blog.title }}</nuxt-link>
                                        </h4>
                                        <p>{{ blog.desc }}</p>
                                        <nuxt-link to="/blog-details" class="btn-theme btn-border-gradient btn-size-md">
                                            <span>Read More 
                                                <img class="icon icon-img" src="/images/icons/arrow-line-right-gradient.png" alt="Icon">
                                            </span>
                                        </nuxt-link>
                                    </div>
                                </div>
                            </div>
                            <div class="pagination-area pt-0 pb-0">
                                <nav>
                                    <ul class="page-numbers">
                                        <li>
                                            <a class="page-number" href="#">1</a>
                                        </li>
                                        <li>
                                            <a class="page-number" href="#">2</a>
                                        </li>
                                        <li>
                                            <a class="page-number" href="#">3</a>
                                        </li>
                                        <li>
                                            <a class="page-number next" href="#">
                                                <img src="/images/icons/arrow-line-right-gradient.png" alt="Icon-Image">
                                            </a>
                                        </li>
                                    </ul>
                                </nav>
                            </div>
                        </div>

                        <SidebarWrapper />
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        components: {
            SidebarWrapper: () => import('@/components/SidebarWrapper'),
        },

        data() {
            return {
                blogs: [
                    {
                        imgSrc: "/images/blog/g1.jpg",
                        day: 15,
                        month: "June",
                        category: "Education",
                        author: "Marinda Roderick",
                        title: "Children education needs for change the world.",
                        desc: "Education is key to change. Empowering children with knowledge and skills can transform communities and create lasting impact for future generations.",
                    },
                    {
                        imgSrc: "/images/blog/g2.jpg",
                        day: 10,
                        month: "July",
                        category: "Health",
                        author: "Maria Merry",
                        title: "Need school for mozambique children.",
                        desc: "Access to education is vital for Mozambique's youth. Building schools and providing resources can help secure a brighter future for these children.",
                    },
                    {
                        imgSrc: "/images/blog/g3.jpg",
                        day: 17,
                        month: "March",
                        category: "Water",
                        author: "Robbin",
                        title: "Need pure water for all people",
                        desc: "Clean water is a basic human right. Initiatives to provide safe and pure water can improve health and quality of life for all communities.",
                    },
                    {
                        imgSrc: "/images/blog/g4.jpg",
                        day: 26,
                        month: "August",
                        category: "Health",
                        author: "Uzzal Hossain",
                        title: "Save Children Life For Future.",
                        desc: "Protecting children's health is crucial for the future. Efforts to improve healthcare access can save lives and empower the next generation.",
                    },
                ]
            }
        },
    };
</script>
