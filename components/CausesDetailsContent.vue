<template>
    <section class="causes-details-area">
        <div class="container">
            <div class="row">
                <div class="col-12">
                    <div class="causes-details-column">
                        <div class="causes-details-content">
                            <div class="causes-details">
                                <div class="thumb">
                                    <img class="w-100" src="/images/causes/d1.jpg" alt="image">
                                </div>
                                <h3 class="cause-title">Food Distribution for Families in Need</h3>
                                <div class="donate-info-wrp">
                                    <div class="row">
                                        <div class="col-md-6">
                                            <ul class="donate-info">
                                                <li class="info-item">
                                                    <span class="info-title">Goal:</span>
                                                    <span class="amount">$ 5,000</span>
                                                </li>
                                                <li class="info-item">
                                                    <span class="info-title">Raised:</span>
                                                    <span class="amount">$ 3,500</span>
                                                </li>
                                                <li class="info-item">
                                                    <span class="info-title">To Go:</span>
                                                    <span class="amount">$ 1,500</span>
                                                </li>
                                            </ul>
                                        </div>
                                        <div class="col-md-6">
                                            <div class="progress-item">
                                                <div class="progress-line">
                                                    <div class="progress-bar-line" style="width: 70%">
                                                        <span class="percent">70%</span>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                                <p>Our mission is to provide nutritious food to families in need. We distribute fresh fruits, vegetables, dairy, proteins, and grains to ensure that everyone has access to healthy meals. Each month, we serve thousands of families, helping to alleviate hunger and improve nutrition.</p>
                                <p class="mb-26">We partner with local businesses, farms, and community organizations to gather and distribute food. Our volunteers play a crucial role in sorting, packing, and distributing food hampers to those in need. Together, we are making a significant impact on food security in our community.</p>
                                <h3>The Challenges</h3>
                                <p>One of the biggest challenges we face is ensuring a consistent supply of fresh and nutritious food. We rely heavily on donations and the support of our community partners. Additionally, logistical issues such as transportation and storage can sometimes hinder our efforts to distribute food efficiently.</p>
                                <p class="mb-26">Despite these challenges, we remain committed to our mission. We continuously seek new partnerships and innovative solutions to improve our food distribution processes and reach more families in need.</p>
                                <h3>The Documents</h3>
                                <div class="row">
                                    <div class="col-sm-6">
                                        <button class="document-item bgcolor-theme3">
                                            <a href="/documents/Terms_of_Reference_Documents.pdf" target="_blank">Terms of Reference</a>
                                            <img src="/images/icons/file.png" alt="Icon">
                                        </button>
                                    </div>
                                    <div class="col-sm-6">
                                        <button class="document-item bgcolor-theme2">
                                            <a href="/documents/Food_Distribution_Documents.pdf" target="_blank">Project Document</a>
                                            <img src="/images/icons/file.png" alt="Icon">
                                        </button>
                                    </div>
                                </div>
                                <p>We have compiled a comprehensive document that outlines our food distribution program, including our goals, challenges, and the impact we have made. This document is available for download and provides detailed information about our operations and how you can support our cause.</p>
                                <p>Thank you for your continued support. Together, we can make a difference in the lives of families in need.</p>
                            </div>
                            <DonnerList />
                            <DonationForm />
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
            DonnerList: () => import('@/components/DonnerList'),
            DonationForm: () => import('@/components/DonationForm'),
            SidebarWrapper: () => import('@/components/SidebarWrapper'),
        },
    };
</script>
