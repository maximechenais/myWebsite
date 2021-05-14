<template>
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
</template>

<script>
export default {
    
    name: 'mainTitle',

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
        }
    }

}
</script>

<style scoped>

    
</style>