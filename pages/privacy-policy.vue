<template>
  <div class="main-container">
    <Header />
    <OffCanvasMobileMenu />
    <Breadcrumb items="Privacy Policy" title="Privacy Policy" />
    <PrivacyPolicyContent />
    <Footer />
  </div>
</template>

<script>
export default {
  components: {
    Header: () => import('@/components/Header'),
    OffCanvasMobileMenu: () => import('@/components/OffCanvasMobileMenu'),
    Breadcrumb: () => import('@/components/Breadcrumb'),
    PrivacyPolicyContent: () => import('@/components/PrivacyPolicyContent.vue'),
    Footer: () => import('@/components/Footer'),
  }
};
</script>


