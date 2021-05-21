<template>
    <div class="title-content">
        <h1 
            :style="
                `font-size: ${fontSize}; 
                font-weight: ${fontWeight};
                color: ${color};
                text-shadow: ${shadow}`
            "
        >
            <slot></slot>
        </h1>
    </div>
</template>

<script>
export default {
    
    name: 'pageTitle',

    props: {
        fontSize: {
            type: String,
            require: true
        },
        fontWeight: {
            type: String,
            require: false
        },
        color: {
            type: String,
            require: false
        },
        shadow: {
            type: String,
            require: false
        },
    }

}
</script>

<style scoped>

    h1 {
        margin: 0;
    }

    .title-content {
        height: auto;
    }
    
</style>