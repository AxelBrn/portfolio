<template>
  <div 
    class="burger flex justify-center align-center"
    :class="getClass"
  >
      <div class="bar" />
  </div>
</template>

<script>
export default {
  props: {
    value: {
      type: Boolean,
      required: true,
    }
  },
  computed: {
    getClass: function() {
      if(this.value) {
        return "is-open"
      }
      return ""
    }
  }
}
</script>

<style lang="scss" scoped>
  .burger {
    transition: all 500ms;
    width: 30px;
    height: 30px;
  }

  .bar, .bar::before, .bar::after {
      position: absolute;
      width: 17.5px;
      height: 1.5px;
      background-color: whitesmoke;
      transition: all 500ms;
  }

  .bar::before, .bar::after {
    content: "";
    display: block;
  }

  .bar::before {
    margin-top: -6px;
  }

  .bar::after {
    margin-top: 6px;
    height: 1.2px;
  }

  .burger.is-open {
    /* L'animation */
    .bar {
      background: transparent;
    }
    .bar::before {
      margin-top: 0px;
      -moz-transform: rotate(-45deg);
      -ms-transform: rotate(-45deg);
      -webkit-transform: rotate(-45deg);
      transform: rotate(-45deg);
    }
    .bar::after {
      margin-top: 0px;
      -moz-transform: rotate(45deg);
      -ms-transform: rotate(45deg);
      -webkit-transform: rotate(45deg);
      transform: rotate(45deg);
    }
  }
</style>