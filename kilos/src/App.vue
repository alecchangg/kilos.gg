<template>
  <div>
    <Header class="head"></Header>
    <div class="mainGrid">
      <Backdrop class="leftBox">hello world</Backdrop>
      <Backdrop class="rightBox"> goodbye world</Backdrop>
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
    column-gap: 50px;
    position: absolute;
    top: 130px;
    left: 85px;
    right: 85px;

  }

  .leftBox, .rightBox {
    color: white;
    border-radius: 15px;
  }

  .leftBox {
      height: 500px;
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


