<template>
    <div class="main-container">
        <div class="top">
            <topbar />
            <planetStars />
        </div>

        <div class="content" >
            <div class="menu">
                <menu />
            </div>
           <div>La 2eme page</div>
        </div>
    </div>
</template>

<script>
import topbar from '@/components/topbar/topbar'
import planetStars from '@/components/topbar/planet'
import mainTitle from '@/components/title/main-title'
import menu from '@/components/menu/menu'
import {gsap} from 'gsap'

export default {
    components: {
        topbar,
        planetStars,
        mainTitle,
        menu
    },

    data() {
        return {
            mainTitle: 'Développeur front end',
            ref: 'rocket'
        }
    },

}

</script>

<style scoped>

.top {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
}
.content {
    display: flex;
    flex-direction: row;
    align-items: center;
}

.menu div{
    color: #FFF5F5;
}

</style>