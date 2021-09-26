<template>
  <div class="home">
    <img style="height: 420px" alt="Vue logo" src="../assets/Enlight28.png">
    <HelloWorld msg="Døner Tallrik & DJ Bord"/>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component'
import HelloWorld from '@/components/HelloWorld.vue' // @ is an alias to /src

@Options({
  components: {
    HelloWorld
  }
})
export default class Home extends Vue {}
</script>
