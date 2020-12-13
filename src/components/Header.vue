<template>
  <nav>
    <div class="flex row max-size">
      <div class="w-25 flex align-center justify-center"> Axel BRIONNE</div>
      <div class="menu mx w-75 max-size flex row align-center justify-spacing" :class="getClass" @click="() => isOpen = false">
        <a class="nav-mobile" href="/#presentation">Présentation</a>
        <a class="nav-mobile bg-light" href="/#parcours">Parcours</a>
        <a class="nav-mobile" href="/#competences">Compétences</a>
        <a class="nav-mobile bg-light" href="/#projets">Projets</a>
        <a class="nav-mobile" href="/#contact">Contact</a>
      </div>
      <div class="burger absolute mr-20 align-self-center" @click="()=> {isOpen = !isOpen}">
        <ButtonBurger 
          :value="isOpen"
        />
      </div>
    </div>
  </nav>
</template>

<script>
import ButtonBurger from '@/components/ButtonBurger'

export default {
  components: { ButtonBurger },
  data() {
    return {
      isOpen: false,
    }
  },
  computed: { 
    getClass: function() {
      if(this.isOpen) {
        return "is-active"
      }
      return ""
    }
  }
}
</script>

<style scoped>
    nav {
        height: 60px;
        background-color: #1F2235;
        color: whitesmoke;
        top: 0;
        width: 100%;
    }
</style>