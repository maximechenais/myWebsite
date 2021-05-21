<template>
    <div class="title-content">
        <p 
            :style="
                `font-size: ${fontSize}; 
                font-weight: ${fontWeight};
                color: ${color};`
            "
        >
            <slot></slot>
        </p>
    </div>
</template>

<script>
export default {
    
    name: 'baseline',

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
    }

}
</script>

<style scoped>

    p {
        margin: 0;
    }

    .title-content {
        height: auto;
    }
    
</style>