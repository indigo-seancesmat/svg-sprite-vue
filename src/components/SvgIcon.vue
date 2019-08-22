<template>
    <svg xmlns="http://www.w3.org/2000/svg"
        :class="['svg-icon', icon]"
        :style="customStyling"
        @mouseover="hovered = true"
        @mouseleave="hovered = false">
        <use xmlns:xlink="http://www.w3.org/1999/xlink"
            :xlink:href="iconPath"></use>
    </svg>
</template>

<script>

export default {
  name: 'SvgIcon',
  props: {
    icon: {
      type: String
    },
    primaryColor: {
      type: String
    },
    secondaryColor: {
      type: String,
      default: 'false'
    },
    hoverPrimeColor: {
      type: String,
      default: 'false'
    },
    hoverSecColor: {
      type: String,
      default: 'false'
    },
    parentHover: {
      type: Boolean,
      default: false
    }
  },
  data () {
    return {
      hovered: false
    }
  },
  computed: {
    customStyling: function () {
      let primeColor
      let secColor
      if (this.primaryColor && this.secondaryColor === 'false') {
        primeColor = this.primaryColor
        secColor = this.primaryColor
      } else if (this.primaryColor && this.secondaryColor) {
        primeColor = this.primaryColor
        secColor = this.secondaryColor
      }
      if ((this.hovered === true || this.parentHover === true) && this.hoverSecColor === 'false') {
        console.log(`%c ${this.hoverSecColor}`, 'color:red')
        primeColor = this.hoverPrimeColor
        secColor = this.hoverPrimeColor
      } else if ((this.hovered === true || this.parentHover === true) && this.hoverSecColor !== 'false') {
        primeColor = this.hoverPrimeColor
        secColor = this.hoverSecColor
      }
      return {
        fill: primeColor,
        color: secColor
      }
    },
    iconPath: function () {
      return `sprite.svg#${this.icon}`
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
.svg-icon {
  transition: color 0.25s linear, fill 0.25s linear;
  cursor: pointer;
}
</style>
