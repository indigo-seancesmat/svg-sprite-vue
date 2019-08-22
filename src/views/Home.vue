<template>
    <div class="home">
        <div>
            <h1>Travel</h1>
            <SvgIcon icon="travel--boat"
                primaryColor="#333"
                hoverSecColor="#eb4034" />
            <SvgIcon icon="travel--camera"
                primaryColor="#333"
                secondaryColor="#eb4034"
                hoverPrimeColor="#111"
                hoverSecColor="#cc352b" />
            <SvgIcon icon="travel--luggage"
                primaryColor="#333"
                secondaryColor="#eb4034"
                hoverPrimeColor="#111"
                hoverSecColor="#cc352b" />
            <SvgIcon icon="travel--map"
                primaryColor="#333"
                secondaryColor="#eb4034"
                hoverPrimeColor="#111"
                hoverSecColor="#cc352b" />
            <SvgIcon icon="travel--sunscreen"
                primaryColor="#333"
                secondaryColor="#eb4034"
                hoverPrimeColor="#111"
                hoverSecColor="#cc352b" />
        </div>
        <div>
            <h1>Gaming</h1>
            <SvgIcon icon="gaming--mouse"
                primaryColor="#333"
                secondaryColor="#eb4034"
                hoverPrimeColor="#1A5276"
                hoverSecColor="#cc352b" />
            <SvgIcon icon="gaming--n64"
                primaryColor="#333"
                secondaryColor="#eb4034"
                hoverPrimeColor="#1A5276"
                hoverSecColor="#cc352b" />
            <SvgIcon icon="gaming--ogn-controller"
                primaryColor="#333"
                secondaryColor="#eb4034"
                hoverPrimeColor="#1A5276"
                hoverSecColor="#cc352b" />
            <SvgIcon icon="gaming--ogn"
                primaryColor="#333"
                secondaryColor="#eb4034"
                hoverPrimeColor="#1A5276"
                hoverSecColor="#cc352b" />
            <SvgIcon icon="gaming--xbox"
                primaryColor="#333"
                secondaryColor="#eb4034"
                hoverPrimeColor="#1A5276"
                hoverSecColor="#cc352b" />
        </div>
        <div>
            <h1>Microsoft</h1>
            <SvgIcon icon="microsoft--logo" />
            <SvgIcon icon="microsoft--graphs" />
            <SvgIcon icon="microsoft--linegraph" />
            <SvgIcon icon="microsoft--thumbprint" />
        </div>
    </div>
</template>

<script>
// @ is an alias to /src
import SvgIcon from '@/components/SvgIcon.vue'

export default {
  name: 'home',
  components: {
    SvgIcon
  }
}
</script>
<style lang="scss">
.home {
    div {
        margin-top: 200px;
        &:first-of-type {
            margin-top: 0;
        }
    }
}
</style>
