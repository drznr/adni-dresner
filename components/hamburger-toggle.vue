<template>
    <span class="hamburger">
        <input id="menuToggle" type="checkbox" hidden :checked="isMenuOpen" @change="emitMenuState">
        <label for="menuToggle">
            <span>|</span>
        </label>
    </span>
</template>

<script>
export default {
    props: {
        isMenuOpen: {
            type: Boolean,
            default: false
        }
    },
    methods: {
        emitMenuState () {
            this.$emit('menu-toggle')
        }
    }
}
</script>

<style lang="scss">
.hamburger {
  direction: ltr;
  font-size: 30px;
  font-weight: 900;
  transform: rotateZ(90deg);

  label {
    cursor: pointer;
    &::after,
    &::before {
      content: "|";
      display: inline-block;
      margin: 0px 2.5px;
      transition: transform 0.4s linear;
    }
  }

  [type="checkbox"]:checked + label > span {
    opacity: 0;
  }
  [type="checkbox"]:checked + label::before {
    transform: translateX(10px) rotateZ(315deg);
  }
  [type="checkbox"]:checked + label::after {
    transform: translateX(-4px) rotateZ(-315deg);
  }
}
</style>
