/* eslint-disable*/
<template>
  <div id="intro">
    <h1>{{ header }}</h1>
    <div class="menu-main">
      <div class="menu-icon-cont">
        <i class="fas fa-bars burger" @click="toggle()"></i>

        <div class="menu-list" v-if="toggleMenu">
          <li class="menu-list-name">
            <p class="menu-list-parag">Cats</p>
          </li>

          <li class="menu-list-name">
            <p class="menu-list-parag">Bears</p>
          </li>

          <li class="menu-list-name">
            <p class="menu-list-parag">Koalas</p>
          </li>
        </div>

      </div>
    </div>


  </div>
</template>

<script>
export default {
  data() {
    return {
      header: 'My favourite animals',
      toggleMenu: false
    }
  },

  methods: {
    toggle() {
      this.toggleMenu = !this.toggleMenu;
    }
  }
}
</script>

<style>
#intro {
  text-align:center; 
  font-family: 'Grandstander', cursive;
}

.menu-main {
  width: 200px;
  height: 300px;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
}

.menu-icon-cont {
  display: flex;
  position: absolute;
  flex-direction: column;
  top: 80px;
}

.burger {
  font-size: 30px;
  display: flex;
  position: relative;
 /*  left: -56px;
  align-self: top; */
}

.menu-list {
  width: 135px;
  list-style-type: none;
  border: 2px solid #753CDF;
  border-radius: 3px;
  position: relative;
  bottom: -25px;
}

.menu-list-name {
  display: flex;
  margin-left: 10px;
  width: 100px;
  height: 50px;
  align-items: center;
  font-family: 'Grandstander', cursive;
}

.menu-list-parag:hover {
  border-bottom: 2px solid #d7c7f5;
  padding-bottom: 2px;
}
</style>




