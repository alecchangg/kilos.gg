<template>
  <div>
    <Header class="head"></Header>
    <div class="mainGrid">
      <div class="leftBox">
        <Backdrop height="500px">hello world</Backdrop>
      </div>
      <div class="rightBox">
        <Backdrop height="250px" marginBottom="20px"> goodbye world</Backdrop>
        <Backdrop height="250px">Horizon Worlds!</Backdrop>
      </div>
      
    </div>
    
  </div>

</template>

<script>
import Header from './components/Header'
import Backdrop from './components/Backdrop'

export default {
  name: 'App',
  components: {
    Header,
    Backdrop
  }
}
</script>

<style scoped>
  .head {
    z-index: 10;
  }

  .mainGrid {
    display: grid;
    grid-template-columns: 300px 1fr;
    column-gap: 35px;
    position: absolute;
    top: 110px;
    left: 85px;
    right: 85px;

  }

  .leftBox, .rightBox {
    color: white;
    border-radius: 15px;
  }

  .leftBox {
      padding-top: 20px;
      padding-left: 20px;
      padding-right: 20px;
  }

  .rightBox {

      padding-top: 20px;
      padding-left: 20px;
      padding-right: 20px;
      display: grid;
      grid-template-columns: 1fr;
      column-gap: 10px;
  }
</style>

<style>
@import url('https://fonts.googleapis.com/css2?family=Ubuntu:wght@400;500;700&display=swap');
</style>


