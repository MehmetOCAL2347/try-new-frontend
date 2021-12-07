<template>
  <header>
    <nav>
      <div class="branding">
        <img src="@/assets/logo.png" alt="" />
      </div>
      <ul v-show="!mobile" class="navigation">
        <li><router-link class="link">Home</router-link></li>
        <li><router-link class="link">About</router-link></li>
        <li><router-link class="link">Portfolio</router-link></li>
        <li><router-link class="link">Contact</router-link></li>
      </ul>
      <div class="icon">
        <button
          @click="toggleMobileNav"
          v-show="mobile"
          :class="{ 'icon-active': mobileNav }"
        >
          BAS
        </button>
      </div>
      <transition name="mobile-nav">
        <ul v-show="mobile" class="dropdown-nav">
          <li><router-link class="link">Home</router-link></li>
          <li><router-link class="link">About</router-link></li>
          <li><router-link class="link">Portfolio</router-link></li>
          <li><router-link class="link">Contact</router-link></li>
        </ul>
      </transition>
    </nav>
  </header>
</template>
<script>
export default {
  name: "Navbar",
  props: {},
};
</script>

<style scoped>
header {
  background-color: red;
  z-index: 99;
  width: 100%;
  position: fixed;
  transition: 0.5s ease all;
  color: white;
}

nav {
  display: flex;
  flex-direction: row;
  padding: 12px 0;
  transition: 0.5s ease all;
  margin: 0 auto;
  width: 90%;
  @media (min-width: 1140px) {
    max-width: 1140px;
  }
}
</style>
