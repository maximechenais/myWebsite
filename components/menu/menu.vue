<template>
    <div class="menu">

        <nuxtLink
            v-for="(menu, index) in menuList"
            :key="`menu-${index}`"
            :to="menu.path" class="menu-list"
        >
            {{ menu.name }}
        </nuxtLink>
        
    </div>
</template>

<script>
export default {
    name: 'menuNavigation',
    data() {
        return {
            menuList: [
                {name: 'Home', path: '/'},
                {name: 'Présentation', path: '/presentation'},
                {name: 'Réalisations', path: '/realisations'},
                {name: 'Avis', path: '/avis'},
                {name: 'Contact', path: '/contact'}
            ]
        }
    },
}
</script>

<style scoped>

    .menu {
        display: flex;
        flex-direction: column;
        justify-content: space-evenly;
        height: 300px;
        min-width: 170px;
        width: 170px;
        margin: 0 50px 0 20px;
    }

    .menu-list {
        text-decoration: none;
        color: #7D7B7B;
        font-size: 18px;
        transition-duration: 0.3s;
    }

    .menu-list:hover {
        color: #FFF510;
    }

    a.nuxt-link-exact-active {
        color: #FFF5F5;
        font-size: 25px;
        text-shadow: 0px 0px 7px #FFF5F5;
    }

</style>