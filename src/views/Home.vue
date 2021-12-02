<template>
  <div class="home">
    <HelloWorld msg="O I D A"/>
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

  mounted () {
    const plugin = document.createElement('script')
    plugin.setAttribute(
      'src',
      'https://unpkg.com/embeddable-nfts/dist/nft-card.min.js'
    )
    plugin.async = true
    document.head.appendChild(plugin)
  }

  public async trykk (event: Event, neighbourIds: Array<string>) {
    const tagElement = event?.target as Element
    neighbourIds.forEach(neighbourId => {
      const neighbourElement = document.getElementById(neighbourId)
      if (neighbourElement?.innerHTML === '' && tagElement !== null) {
        console.log('SETTING: ' + tagElement.innerHTML)
        neighbourElement.innerHTML = tagElement.innerHTML
        tagElement.innerHTML = ''
      }
    })
  }

  public mouseover (event: Event) {
    const hackyLink = document.createElement('a')
    hackyLink.target = '_blank'
    hackyLink.href = 'https://t.me/tallrik'
    hackyLink.click()
    window.alert('Its a trap!')
  }
}
</script>

<style>
  .button {
    display: inline-block;
    border-radius: 4px;
    background-color: #f4511e;
    border: none;
    color: #FFFFFF;
    text-align: center;
    font-size: 5em;
    transition: all 0.5s;
    cursor: pointer;
    margin: 5px;
  }

  .button_lol {
    display: inline-block;
    border-radius: 4px;
    background-color: #f4511e;
    border: none;
    color: #FFFFFF;
    text-align: center;
    font-size: 5em;
    transition: all 0.5s;
    cursor: pointer;
    margin: 5px;
  }

  .button span {
    cursor: pointer;
    display: inline-block;
    position: relative;
    transition: 0.5s;
  }

  .button_lol span {
    cursor: pointer;
    display: inline-block;
    position: relative;
    transition: 0.5s;
  }

  .button span:after {
    content: '\00bb';
    position: absolute;
    opacity: 0;
    top: 0;
    right: -20px;
    transition: 0.5s;
  }

  .button_lol span:after {
    content: '\00bb';
    position: absolute;
    opacity: 0;
    top: 0;
    right: -20px;
    transition: 0.5s;
  }

  .button:hover span {
    padding-right: 4em;
  }

  .button_lol:hover span {
    padding-right: 6em;
  }

  .button_lol:hover span:after {
    opacity: 1;
    right: 0;
  }

  .button:hover span:after {
    opacity: 1;
    right: 0;
  }
  .lol {
      background-color: pink;
      padding: 10px;
      margin: 10px;
      border: solid green 2px;
      width: 30px;
      height: 30px;
      float: left;
      cursor: pointer;
      font-size: x-large;
    }

  .forstPaLinja {
    clear: left !important;
  }

  .blink_1{
    animation: blink 3s infinite;
  }
  @keyframes blink{
    0% {
      background: red;
    }
    20% {
      background: green;
    }
    40% {
      background: yellow;
    }
    60% {
      background: blue;
    }
    80% {
      background: orange;
    }
    100% {
      background: red;
    }
  }

  @-webkit-keyframes blink{
    0% {
      background: red;
    }
    20% {
      background: green;
    }
    40% {
      background: yellow;
    }
    60% {
      background: blue;
    }
    80% {
      background: orange;
    }
    100% {
      background: red;
    }
  }
</style>
