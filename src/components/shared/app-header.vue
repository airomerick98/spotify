<template>
   <div class="app-header">
       <div class="app-header-image">
           <img src="../../assets/hero.svg" alt="" height="340">
       </div>
       <div class="app-header-content bold">
           Your favourite tunes
            <p>
                All 🌞 and all 🌙
            </p>
       </div>
    </div> 
</template>

<script>
export default {
    name: 'app-header'
}
</script>

<style lang="scss" scoped>
.app-header {
    @include flex-center ;
    background-color: $primary;
    font-size: 25px;
    padding: 35px 30px;
    text-align: left;

    @media (min-width: 970px) {
        @include flex-between;
        font-size: 35px;
        padding: 0 60px;
    }

    &-content {
        color: $white;
    }

    &-image {
        padding-right: 155px;
        transform: scaleX(-1);

        @media (max-width: 970px) {
            display: none;
        }
    }
}
</style>