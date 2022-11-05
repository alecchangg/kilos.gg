<template>
    <div class="header-box">
        <div class="leftHeader">
            <IButton filename="logo.webp" class="headerLogo"></IButton>
            <IButton filename="hamburger-menu.jpeg" class="headerHamburger"></IButton>
            <HButton text="Dashboard" class="btn"></HButton>
            <HButton text="Blocks" class="btn"></HButton>
            <HButton text="Analytics" class="btn"></HButton>
        </div>
        <div class="middleHeader"></div>
        <div class="rightHeader">
            <IButton filename="search-icon.png" class="headerSearchIcon"></IButton>
            <HButton text="Account" class="btn"></HButton>
        </div>
    </div>
</template>

<script>
import HButton from './HButton'
import IButton from './IButton'

export default {
    name: 'Header',
    props: {

    },
    components: {
        HButton,
        IButton,
    }
}
</script>

<style scoped>
    .header-box {
        display: flex;
        flex-direction: row;
        position: fixed;
        top: 20px;
        left: 20px;
        right: 20px;
        height: 65px;
        background-color: black;
        border-radius: 33px;
        color: white;
    }

    .leftHeader {
        display: flex;
        width: 500px;
        align-items: center;
        justify-content: space-between;
        padding-left: 50px;
    }

    .middleHeader {
        flex: 1;
    }

    .rightHeader {
        display: flex;
        width: 150px;
        align-items: center;
        justify-content: space-between;
        padding-right: 50px;
    }

    .headerLogo {
        height: 30px;
        width: 30px;
        border-radius: 15px;
    }

    .headerLogo:hover {
        cursor: pointer;
    }

    .headerHamburger {
    display: none;
    }

    @media (max-width: 800px) {
        .btn {
            display: none;
        }

        .headerHamburger {
            display: block;
            height: 30px;
            width: 30px;
            
        }

        .headerHamburger:hover {
            cursor: pointer;
        }
        
        .leftHeader {
            width: 80px;
        }
    }
    .headerSearchIcon {
    height: 26px;
    width: 26px;
    margin-left: 20px;
    }

    .headerSearchIcon:hover {
        cursor: pointer;
    }

</style>
