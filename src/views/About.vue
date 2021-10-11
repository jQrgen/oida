<template>
  <div class="morradi">
    <button style="cursor: pointer; font-size: 10em" @click="fade = !fade">Hva?</button>
    <FadeInOut
      entry="center"
      exit="center"
      :duration="800"
      appear
    >
      <div class="blink" v-if="fade">
        <h1 style="cursor: pointer; font-size: 5em">Pulte morra di i går</h1>
      </div>
    </FadeInOut>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component'
import { FadeInOut } from 'vue3-transitions'

@Options({
  components: {
    FadeInOut
  }
})
export default class About extends Vue {
  public fade = false
}
</script>

<style>
.blink{
  padding: 3em;
  animation: blink 0.5s infinite;
}
@keyframes blink{
  0% {
    background: red;
  }
  50% {
    background: #ffffff;
  }
  100% {
    background: red;
  }
}

@-webkit-keyframes blink{
  0% {
    background: red;
  }
  50% {
    background: #ffffff;
  }
  100% {
    background: red;
  }
}
</style>
