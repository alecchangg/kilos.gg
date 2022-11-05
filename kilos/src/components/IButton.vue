<template>
    <img :src="require(`@/assets/img/${filename}`)">
</template>

<script>
export default {
    name: 'IButton',
    props: {
        filename: String
    }
}
</script>
