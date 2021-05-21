<template>
    <div class="main-container">
      
            <div>La 2eme page</div>
    </div>
</template>

<script>
import mainTitle from '@/components/title/main-title'
import {gsap} from 'gsap'

export default {
    components: {
        mainTitle,
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

.fade-enter-active, .fade-leave-active {
  transition: opacity .5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
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