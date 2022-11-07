<template>
    <div class="backdrop">
        <slot>

        </slot>
    </div>
    
</template>

<script>
export default {
    name: "Backdrop",
    props: ['width', 'height', 'marginBottom']
}

</script>

<style scoped>
    .backdrop {
        background-color: black;
        border-radius: 15px;
        width: v-bind(width);
        height: v-bind(height);
        color: white;
        padding-right: 10px;
        padding-left: 10px;
        padding-top: 10px;
        padding-bottom: 10px;
        margin-bottom: v-bind(marginBottom)
    }
</style>
