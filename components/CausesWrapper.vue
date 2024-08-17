<template>
    <section class="causes-area causes-default-area">
        <div class="container">
            <div class="row mtn-30">
                <div class="col-md-6 col-lg-4 mt-30" v-for="(causes, index) in causesData" :key="index">
                    <div class="causes-item">
                        <div class="thumb">
                            <img :src="causes.imgSrc" :alt="causes.title">
                        </div>
                        <div class="content">
                            <ul class="donate-info">
                                <li class="info-item" v-for="(info, index) in causes.infoList" :key="index">
                                    <span class="info-title">{{ info.infoTitle }}:</span>
                                    <span class="amount">{{ info.amount }}</span>
                                </li>
                            </ul>
                            <h4 class="title">
                                <nuxt-link to="/causes-details">{{ causes.title }}</nuxt-link>
                            </h4>
                            <p>{{ causes.desc }}</p>
                        </div>
                        <div class="causes-footer">
                            <div class="admin">
                                <h5>
                                    <nuxt-link to="/causes">
                                        <span class="icon-img">
                                            <img src="/images/icons/admin1.png" alt="Icon">
                                        </span> {{ causes.name }}
                                    </nuxt-link>
                                </h5>
                            </div>
                            <nuxt-link to="/donation" class="btn-theme btn-border-gradient gray-border btn-size-md">
                                <span>
                                    Help Us
                                    <img class="icon icon-img" src="/images/icons/arrow-line-right-gradient.png" alt="Icon">
                                </span>
                            </nuxt-link>
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
                causesData: [
                    {
                        imgSrc: "/images/causes/01.jpg",
                        title: "Help Provide Shelter for Homeless Children",
                        desc: "We aim to provide safe and secure housing for children who are currently living on the streets.",
                        name: "Kristin Horton",
                        infoList: [
                            {
                                infoTitle: "Goal",
                                amount: "$ 4500"
                            },
                            {
                                infoTitle: "Raised",
                                amount: "$ 2500"
                            },
                            {
                                infoTitle: "To Go",
                                amount: "$ 2000"
                            }
                        ]
                    },
                    {
                        imgSrc: "/images/causes/02.jpg",
                        title: "Support Education for Underprivileged Kids",
                        desc: "Your donation will help us provide educational materials and resources to children in need.",
                        name: "Cristian Dominy",
                        infoList: [
                            {
                                infoTitle: "Goal",
                                amount: "$ 3500"
                            },
                            {
                                infoTitle: "Raised",
                                amount: "$ 1500"
                            },
                            {
                                infoTitle: "To Go",
                                amount: "$ 2000"
                            }
                        ]
                    },
                    {
                        imgSrc: "/images/causes/03.jpg",
                        title: "Clean Water for Mozambique Communities",
                        desc: "We are working to ensure that every person in Mozambique has access to clean and safe drinking water.",
                        name: "Maria Jeccy",
                        infoList: [
                            {
                                infoTitle: "Goal",
                                amount: "$ 9000"
                            },
                            {
                                infoTitle: "Raised",
                                amount: "$ 6000"
                            },
                            {
                                infoTitle: "To Go",
                                amount: "$ 3000"
                            }
                        ]
                    },
                    {
                        imgSrc: "/images/causes/01.jpg",
                        title: "Medical Supplies for Rural Clinics",
                        desc: "Providing essential medical supplies to clinics in rural areas to improve healthcare access.",
                        name: "John Doe",
                        infoList: [
                            {
                                infoTitle: "Goal",
                                amount: "$ 7000"
                            },
                            {
                                infoTitle: "Raised",
                                amount: "$ 3000"
                            },
                            {
                                infoTitle: "To Go",
                                amount: "$ 4000"
                            }
                        ]
                    },
                    {
                        imgSrc: "/images/causes/02.jpg",
                        title: "Food Distribution for Families in Need",
                        desc: "Ensuring that families in need have access to nutritious food through our distribution programs.",
                        name: "Jane Smith",
                        infoList: [
                            {
                                infoTitle: "Goal",
                                amount: "$ 5000"
                            },
                            {
                                infoTitle: "Raised",
                                amount: "$ 3500"
                            },
                            {
                                infoTitle: "To Go",
                                amount: "$ 1500"
                            }
                        ]
                    },
                    {
                        imgSrc: "/images/causes/03.jpg",
                        title: "Educational Programs for Refugees",
                        desc: "Supporting educational programs for refugees to help them build a better future.",
                        name: "Emily Johnson",
                        infoList: [
                            {
                                infoTitle: "Goal",
                                amount: "$ 8000"
                            },
                            {
                                infoTitle: "Raised",
                                amount: "$ 5000"
                            },
                            {
                                infoTitle: "To Go",
                                amount: "$ 3000"
                            }
                        ]
                    }
                ]
            }
        },
    };
</script>
