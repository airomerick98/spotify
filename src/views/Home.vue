<template>
  <div class="home">
    <app-header />
    <app-sidebar />
    <div class="home-content">
      <h2 class="home-title">RELEASED THIS WEEK</h2>
    </div>
  </div>
</template>

<script>
import appHeader from '../components/shared/app-header.vue';
import appSidebar from '../components/shared/app-sidebar.vue';
// @ is an alias to /src

export default {
  name: 'Home',
  components: {
    appHeader,
    appSidebar,
  },
}
</script>

<style lang="scss" scoped>
.home {
  &-content {
    background-color: $white;
    padding: 25px 20px;
  }

  &-title {
    color: $gray;
  }
}
</style>
