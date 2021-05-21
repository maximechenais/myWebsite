<template>
    <div class="content">

        <pageTitle
            fontSize="48px"
            fontWeight="bold"
            color="#FFF5F5"
            shadow="0px 0px 7px #FFF5F5"
            class="page-title"
        >
            {{ pageTitle }}
        </pageTitle>

        <baseline
            fontSize="18px"
            color="#FFF5F5"
            class="baseline"
        >
            {{ baseline }}
        </baseline>

        <video src="" controls class="video-presentation"></video>
    </div>
</template>

<script>
import pageTitle from '@/components/title/page-title'
import baseline from '@/components/title/baseline'
import {gsap} from 'gsap'

export default {
    components: {
        pageTitle,
        baseline
    },

    data() {
        return {
            pageTitle: 'Présentation',
            baseline: 'Parce que les images valent mille mots, une vidéo vaut mille images.'
        }
    },

}

</script>

<style scoped>

.content {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    margin-left: 100px;
}

.page-title {
    margin-top: -80px;
}

video.video-presentation {
    width: 774px;
    height: 400px;
    margin: 0;
    border-radius: 10px;
    box-shadow: 0px 0px 7px #FFF5F5;
    margin-top: 50px;
}

.baseline {
    margin-top: 20px;
}

</style>