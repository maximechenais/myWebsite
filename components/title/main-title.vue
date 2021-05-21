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
        <h1
            :style="
                `font-size: ${fontSize}; 
                font-weight: ${fontWeight};
                color: ${color2};
                text-shadow: ${shadow2};
                transform: ${transform}`
            "
            class="title-reverse"
        >
            <slot></slot>
        </h1>
    </div>
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
        color2: {
            type: String,
            require: false
        },
        shadow: {
            type: String,
            require: false
        },
        shadow2: {
            type: String,
            require: false
        },
        transform: {
            type: String,
            require: false
        }
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

    .title-reverse {
        position: relative;
        bottom: 30px;
    }
    
</style>