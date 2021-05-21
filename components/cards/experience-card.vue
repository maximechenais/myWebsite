<template>
    <div class="main-cards-container">
        <div class="card-container" 
            v-for="(exp, index) in experiences"
            :key="`card-${index}`"
        >
            <div class="image-container" :style="`background-color:${exp.background_image}`">
                    <img :src="require(`@/assets/logo/${exp.logo_image}`)"  alt="company-logo" class="image-company">
            </div>
            
            <div class="infos-container">
                <div class="name-link">
                    <div class="name">{{ exp.name }}</div>
                    <div class="link" v-if="exp.github">
                        <a :href="`${exp.github_link}`" target="_blank">
                            Voir sur Github 
                            <img src="@/assets/icons/github.svg" class="link-icon" alt="github-icon">
                        </a>
                    </div>
                    <div class="link" v-else><a :href="`${exp.website_link}`" target="_blank">Vers le site</a></div>
                </div>
                <div class="description">{{ exp.description }}</div>
                <div class="stack-container" >
                    <div class="stack-card" :style="`background-color:${item.color}`" v-for="(item, index) in exp.stack"
                :key="`stack-${index}`">{{ item.name }}</div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'experienceCard',

    props: {
        experiences: {
            type: Object,
            required: true
        },
        stacks: {
            type: Object,
            required: true
        }
    },   
}
</script>

<style scoped>
    .main-cards-container {
        height: 350px;
        width: 800px;
        overflow: auto;
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        margin-top: 20px;
    }
    .main-cards-container::-webkit-scrollbar {
        display: none;
    }

    .card-container {
        width: 736px;
        height: 155px;
        background: #282828;
        box-shadow: 0px 0px 7px #FFF5F5;
        border-radius: 10px;
        margin: 30px 10px 10px 10px;
        padding: 10px;
        padding-right: 20px;
        display: flex;
        flex-direction: row;
    }

    .image-container {
        min-width: 158px;
        width: 158px;
        min-height: 114px;
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 5px;
        border-radius: 10px;
    }

    .image-company {
        width: 90%;
        height: auto;
    }

    .infos-container {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        margin-left: 20px;
        width: 100%;
    }

    .stack-container {
        display: flex;
        flex-direction: row;
        justify-content: flex-start;
        width: 100%;
    }

    .name-link {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        width: 100%;
    }

    .name {
        font-size: 18px;
        color: #fff5f5;
    }

    .link {
        font-size: 12px;
        color: #fff5f5;
    }

    .link a {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        text-decoration: none;
        color: #fff5f5;
        transition-duration: 0.2s;
        cursor: pointer;
    }

    .link a:hover {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        text-decoration: none;
        color: #FFF510;
    }

    .link-icon {
        width: 20px;
        height: 20px;
        margin-left: 10px;
    }

    .description {
        font-size: 14px;
        color: #fff5f5;
    }

    .stack-card {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 77px;
        height: 21px;
        padding: 5px;
        margin-right: 5px;
        border-radius: 50px;
        color: #fff;
        font-size: 11px;
    }
</style>