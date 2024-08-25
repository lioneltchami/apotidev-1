<template>
    <ul class="main-menu nav">
        <li>
            <nuxt-link to="/about">About Us</nuxt-link>
        </li>
      <!--CAUSES-->
        <li class="has-submenu">
          <nuxt-link to="/causes">Causes</nuxt-link>
          <ul class="submenu-nav">
            <li>
              <nuxt-link to="/causes">Causes</nuxt-link>
            </li>
            <li>
              <nuxt-link to="/causes-details">Causes Details</nuxt-link>
            </li>
          </ul>
        </li>
        <!--BLOG-->
        <li>
          <a href="https://apotidev.substack.com/" target="_blank" rel="noopener noreferrer">Blog</a>
<!--          <nuxt-link to="https://apotidev.substack.com/">Blog</nuxt-link>-->
<!--          <ul class="submenu-nav">-->
<!--            <li>-->
<!--              <nuxt-link to="/blog">Blog</nuxt-link>-->
<!--            </li>-->
<!--            <li>-->
<!--              <nuxt-link to="/blog-details">Blog Details</nuxt-link>-->
<!--            </li>-->
<!--          </ul>-->
        </li>
      <!--Event Details-->
        <li class="has-submenu">
          <nuxt-link to="/event-details">Event</nuxt-link>
          <ul class="submenu-nav">
            <li>
              <nuxt-link to="/event-details">Event Details</nuxt-link>
            </li>
            <li>
              <nuxt-link to="/donation">Donation</nuxt-link>
            </li>
          </ul>
        </li>
      <!--Partner with Us-->
        <li class="has-submenu">
            <nuxt-link to="/volunteer">Partner with Us</nuxt-link>
            <ul class="submenu-nav">
                <li>
                    <nuxt-link to="/volunteer">Volunteer</nuxt-link>
                </li>
                <li>
                    <nuxt-link to="/donation">Donation</nuxt-link>
                </li>
            </ul>
        </li>
      <!--Contact Us-->
        <li>
            <nuxt-link to="/contact">Contact Us</nuxt-link>
        </li>
    </ul>
</template>
<script setup lang="ts">
</script>