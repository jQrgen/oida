<template>
  <div class="home">
    <img style="height: 420px" alt="Vue logo" src="../assets/Enlight28.png">
    <HelloWorld msg="Døner Tallrik & DJ Bord"/>
    <iframe allowtransparency="true" scrolling="no" frameborder="no" src="https://w.soundcloud.com/icon/?url=http%3A%2F%2Fsoundcloud.com%2Fuser-688920568-653173414&color=orange_white&size=64" style="width: 64px; height: 64px;"></iframe>
    <h1><vue3-autocounter ref='counter' :startAmount='0' :endAmount='10000000000000000000000' :duration='1000' prefix='$' suffix='USD' separator=',' decimalSeparator='.' :decimals='2' :autoinit='true' @finished='alert(`Counting finished!`)'/>
    </h1>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component'
import HelloWorld from '@/components/HelloWorld.vue' // @ is an alias to /src
import Vue3autocounter from 'vue3-autocounter'

@Options({
  components: {
    HelloWorld,
    'vue3-autocounter': Vue3autocounter
  }
})

export default class Home extends Vue {
  // Declare mounted lifecycle hook
  async setup () {
    console.log('HI')
  }
}
</script>
