<template>
  <div class="app-sidebar">
      <img src="../../assets/avatar.svg" alt="" height="35">
      <h3 class="app-sidebar-title">Bob Smit</h3>
      <div
       class="app-sidebar-content"
       v-for="(item, index) in itemsSidebar" :key="index">
        <div class="app-sidebar-items bold"
        :class="{'active' : item.active }">
            {{ item.name }}
        </div>
      </div>
   </div>  
</template>

<script>
function data() {
    return {
        itemsSidebar: [
            {
                id: 1,
                name: 'Discover',
                active: true,
            },
            {
                id: 2,
                name: 'Search',
                active: false,
            },
            {
                id: 3,
                name: 'Favorites',
                active: false,
            },
            {
                id: 4,
                name: 'Playlist',
                active: false,
            },
            {
                id: 4,
                name: 'Charts',
                active: false,
            },
        ],
    }
}

export default {
    name: 'app-sidebar',
    data,
};
</script>

<style lang="scss" scoped>
.app-sidebar {
    background-color: $secundary;
    height: 100%;
    overflow-x: inherit!important;
    overflow-y: initial!important;
    padding: 55px 0 0 0;
    position: absolute;
    top: 0;
    width: 20%;

    @media (min-width: 970px) {
        width: 15%;
    }

    &-title {
        color: $white;
        font-size: 15px;
        display: none;

        @media (min-width: 970px) {
            display: block;
            font-size: 25px;
        }
    }

    &-content {
        margin-top: 35px;
    }

    &-items {
        color: white;
        padding: 25px 0;

        &.active {
           background: rgb(2,0,36);
            background: linear-gradient(90deg, rgba(2,0,36,1) 0%, rgba(9,9,121,1) 0%, rgba(255,0,239,1) 75%);
            padding: 25px 0;
        }
    }
}
</style>