<template>
    <img :src="require(`@/assets/img/${filename}`)" @click="onClick()">
</template>

<script>
export default {
    name: 'IButton',
    props: {
        filename: String
    },
    methods: {
        onClick() {
            this.$emit('img-click')
        }
    }
}
</script>
