<template>
    <div class="main-container">
        <div class="content" >

            <div class="website-name">
                {{ websiteName }}
            </div>

            <mainTitle 
                fontSize="64px"
                fontWeight="bold"
                color="#FFF510"
                color2="rgba(255, 245, 16, 0.01)"
                shadow="0px 0px 7px #FFF5F5"
                shadow2="0px 0px 7px rgba(255, 245, 245, 0.1)"
                transform="matrix(1, 0, 0, -1, 0, 0)"
            >
                {{ mainTitle }}
            </mainTitle>

            <p class="stack-element">
                {{ stackElements }}
            </p>
        </div>
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
            websiteName: 'Maxime Chenais',
            stackElements: 'Vue js, Nuxt js, Javascript, Html5 & Css3',
                
        }
    },

}

</script>

<style scoped>

.home-enter-active, .home-leave-active { transition: opacity .5s; }
  .home-enter, .home-leave-active { opacity: 0; }

.content {
    display: flex;
    flex-direction: column;
    align-items: flex-end;
    margin-left: 250px;
}

.menu div{
    color: #FFF5F5;
}

.website-name {
    color: #FFF5F5;
    font-size: 64px;
    text-shadow: 0px 0px 7px #FFF5F5;
}

.stack-element {
    color: #7D7B7B;
    font-size: 18px;
}

</style>