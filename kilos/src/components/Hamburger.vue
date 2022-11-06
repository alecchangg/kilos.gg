<template>
    <div class="menu">
        <img src="@/assets/img/hamburger-menu.jpeg" class="hamburger" @click="isOpen = !isOpen">
        <transition name="fade" appear>
            <div class="sub-menu" v-if="isOpen" >
                <div class="menu-item">Dashboard</div>
                <div class="menu-item">Blocks</div>
                <div class="last-item">Analytics</div>
            </div>
        </transition>
    </div>   
</template>

<script>
    export default {
        name: "Hamburger",
        props: {
            items: Object
        },
        data() {
            return {
                isOpen: false
            }
        }
    }
    
</script>

<style scoped>
    .hamburger {
            display: block;
            height: 30px;
            width: 30px;
            
        }

    .hamburger:hover {
        cursor: pointer;
    }


    .menu-item, .last-item {
        
        padding-right: 20px;
        padding-left: 20px;
        padding-top: 15px;
        padding-bottom: 20px;
        text-align: center;
        transition: background-color 0.15s;
    }

    .last-item {
        border-radius: 0 0 25px 25px;
    }

    .menu-item:hover, .last-item:hover{
        cursor: pointer;
        background-color: rgb(65, 65, 65);
    }
    .sub-menu {
        background-color: black;
        position: absolute;
        top: calc(100%);
        left: 58px;
        width: max-content;
        border-radius: 0 0 25px 25px;
   
    }

    .fade-enter-active, .fade-leave-active{
        transition: all 0.1s ease-out;
        transition: all 0.1s ease-in;
    }

    .fade-enter, .fade-leave-to {
        opacity: 0;
    }
</style>
