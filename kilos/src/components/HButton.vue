<template>
    <div class="button" @click="onClick()">{{ text }}</div>
</template>

<script>

export default {
    name: 'HButton',
    props: {
        text: String
    },
    methods: {
        onClick() {
            this.$emit('btn-click')
        }
    }
}

</script>

<style scoped>
    .button {
        color: white;
        font-weight: 500;
        padding-top: 6px;
        padding-bottom: 6px;
        padding-right: 10px;
        padding-left: 10px;
        border-radius: 50px;
        transition: background-color 0.15s;
        transition: display 0.5s; 
    }

    .button:hover {
        background-color: rgb(65, 65, 65);
        cursor: pointer;
    }
</style>



