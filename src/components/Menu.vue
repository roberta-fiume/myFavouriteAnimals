/* eslint-disable*/
<template>
  <div id="intro">
    
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
    <div class="menu-main-images-cont">
      <h1>{{ header }}</h1>
      <MainImages/>
    </div>
  </div>
</template>

<script>
import MainImages from "../components/MainImages.vue"


export default {
   components: {
    MainImages
  },
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
  display: flex;
  flex-direction: row; 
  justify-content: flex-start;
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
  justify-content: space-between;
  top: 80px;
  border: 2px solid blue;
}

.menu-icon-menu-list-cont {
   display: flex;
   flex-direction: column;
   border: 2px solid yellow;
}

.burger {
  width: 0;
  font-size: 30px;
  display: flex;
  position: relative;
 /*  left: -56px;
  align-self: top; */
}

.menu-list {
  width: 135px;
  list-style-type: none;
  border: 2px solid #7E3FF2;
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

.menu-main-images-cont {
  display: flex;
  flex-direction: column;
  border: 2px solid lightsalmon;
}
</style>




