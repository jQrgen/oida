<template>
  <div class="home">
    <HelloWorld msg="Døner Tallrik & DJ Bord"/>
    <br>
    <br>
    <hr>

    <a target="_blank" href="https://soundcloud.com/user-688920568-653173414">
      <button class="button_lol"><span>SOUNDCLOUD</span></button>
      <iframe allowtransparency="true" scrolling="no" frameborder="no" src="https://w.soundcloud.com/icon/?url=http%3A%2F%2Fsoundcloud.com%2Fuser-688920568-653173414&color=orange_white&size=64" style="width: 64px; height: 64px;"></iframe>
    </a>
    <hr>

    <a target="_blank" href="https://t.me/tallrik">
      <button class="button"><span>Follow the fekking Telegram!!!</span>
        <iframe id="webroundbuttonwidget3" file="webroundbuttonwidget" src="https://telegrambutton.com/webroundbuttonwidget.php?chat_id=tallrik&showchatid=true&showmembercount=true&showmembercount=true&color=&pulse=true&textcolor=white&shadowval=&textval=join channel" border="1" style="border:20px;height: 100px;width: 100px;"></iframe>
      </button>
    </a>
    <hr>

    <h1 class="blink_1">NEWS (NYHETER)</h1>
    <b>Breaking: Døner Tallrik & Dj Bord har fått penger fra NAV.</b>

    <p style="font-style: italic">"Dette er stor sak i Trøgstad og mange er glade. Bedre med penger fra staten en brødskive uten servelaten" - Trøgstadværing</p>
    <img style="height: 15em" alt="Vue logo" src="../assets/nyhet1.png">
    <p style="font-style: italic">"Bilde: Kvittering på at vi får spenna (Ikke til å bruke sjæl)</p>

    <br>
    <br>

    <h1>Mining Bitcoins</h1>
    <h2><vue3-autocounter ref='counter' :startAmount='0' :endAmount='10000000000000000000000' :duration='1000' prefix='$' suffix='USD' separator=',' decimalSeparator='.' :decimals='2' :autoinit='true' @finished='alert(`Counting finished!`)'/>
    </h2>

    <div class="lol" id="r1k1" @click="trykk($event, ['r1k2','r3k1'])">3</div>
    <div class="lol"  id="r1k2" @click="trykk($event, ['r1k1','r2k2', 'r1k3'])">2</div>
    <div class="lol"  id="r1k3" @click="trykk($event, ['r1k2','r2k3'])">1</div>

    <div id="r2k1" class="forstPaLinja lol" @click="trykk($event, ['r1k1', 'r2k2', 'r3k1'])">7</div>
    <div class="lol"  id="r2k2" @click="trykk($event, ['r1k2', 'r2k1', 'r2k3', 'r3k2'])"></div>
    <div class="lol"  id="r2k3" @click="trykk($event, ['r1k3', 'r2k2', 'r3k3'])">4</div>

    <div id="r3k1" class="forstPaLinja lol" @click="trykk($event, ['r2k1', 'r3k2'])">8</div>
    <div class="lol"  id="r3k2" @click="trykk($event, ['r3k1', 'r2k2', 'r3k3'])">5</div>
    <div class="lol"  id="r3k3" @click="trykk($event, ['r3k2', 'r2k3'])">6</div>

    <iframe v-on:mouseover="mouseover" id="webroundbuttonwidget2" file="webroundbuttonwidget" src="https://telegrambutton.com/webroundbuttonwidget.php?chat_id=tallrik&showchatid=true&showmembercount=true&showmembercount=true&color=&pulse=true&textcolor=white&shadowval=&textval=join channel" border="1" style="border:20px;height: 100px;width: 100px;"></iframe>

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
