<template>
  <div class="morradi">
    <button style="cursor: pointer; font-size: 25em" @click="fade = !fade">Hva?</button>
    <FadeInOut
      entry="center"
      exit="center"
      :duration="800"
      appear
    >
      <div v-if="fade">
        <h1>Pulte hun i går</h1>
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
export default class Home extends Vue {
  public fade = false
}
</script>
