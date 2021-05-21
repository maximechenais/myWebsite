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

        <experienceCard 
            :experiences="experiences"
            :stacks="experiences.stack"
        />

    </div>
</template>

<script>
import pageTitle from '@/components/title/page-title'
import baseline from '@/components/title/baseline'
import experienceCard from '@/components/cards/experience-card'
import experiences from '@/static/experiences.json'
import {gsap} from 'gsap'

export default {
    components: {
        pageTitle,
        baseline,
        experienceCard
    },

    data() {
        return {
            pageTitle: 'Réalisations',
            baseline: 'Pour des raisons de confidentialité, certains projets ne seront pas  publiques. Me consulter ici pour en savoir plus.',
            
        }
    },
    asyncData ({ params }) {
        return { experiences }
    }

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

.baseline {
    margin-top: 20px;
    width: 700px;
}

</style>