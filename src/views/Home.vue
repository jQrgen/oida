<template>
  <div class="home">
    <img style="height: 420px" alt="Vue logo" src="../assets/Enlight28.png">
    <a target="_blank" href="https://t.me/tallrik">
      <button class="button" style="vertical-align:middle"><span>Joine the fekking telegram </span></button>
    </a>
    <iframe id="webroundbuttonwidget2" file="webroundbuttonwidget" src="https://telegrambutton.com/webroundbuttonwidget.php?chat_id=tallrik&showchatid=true&showmembercount=true&showmembercount=true&color=&pulse=true&textcolor=white&shadowval=&textval=join channel" border="1" style="border:20px;height: 100px;width: 100px;"></iframe>
    <HelloWorld msg="Døner Tallrik & DJ Bord"/>
    <div class="lol" id="r1k1" @click="trykk($event, ['r1k2','r3k1'])">3</div>
    <div class="lol"  id="r1k2" @click="trykk($event, ['r1k1','r2k2', 'r1k3'])">2</div>
    <div class="lol"  id="r1k3" @click="trykk($event, ['r1k2','r2k3'])">1</div>

    <div id="r2k1" class="forstPaLinja lol" @click="trykk(this, ['r1k1', 'r2k2', 'r3k1'])">7</div>
    <div class="lol"  id="r2k2" @click="trykk($event, ['r1k2', 'r2k1', 'r2k3', 'r3k2'])"></div>
    <div class="lol"  id="r2k3" @click="trykk($event, ['r1k3', 'r2k2', 'r3k3'])">4</div>

    <div id="r3k1" class="forstPaLinja lol" @click="trykk(this, ['r2k1', 'r3k2'])">8</div>
    <div class="lol"  id="r3k2" @click="trykk($event, ['r3k1', 'r2k2', 'r3k3'])">5</div>
    <div class="lol"  id="r3k3" @click="trykk($event, ['r3k2', 'r2k3'])">6</div>

    <iframe allowtransparency="true" scrolling="no" frameborder="no" src="https://w.soundcloud.com/icon/?url=http%3A%2F%2Fsoundcloud.com%2Fuser-688920568-653173414&color=orange_white&size=64" style="width: 64px; height: 64px;"></iframe>
    <iframe width="100%" height="450" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/playlists/1322369266&color=%23ff5500&auto_play=true&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true"></iframe><div style="font-size: 10px; color: #cccccc;line-break: anywhere;word-break: normal;overflow: hidden;white-space: nowrap;text-overflow: ellipsis; font-family: Interstate,Lucida Grande,Lucida Sans Unicode,Lucida Sans,Garuda,Verdana,Tahoma,sans-serif;font-weight: 100;"><a href="https://soundcloud.com/jqrgen" title="jQrgen" target="_blank" style="color: #cccccc; text-decoration: none;">jQrgen</a> · <a href="https://soundcloud.com/jqrgen/sets/doener-tallrik-dj-bord" title="Döner Tallrik &amp; Dj Bord" target="_blank" style="color: #cccccc; text-decoration: none;">Döner Tallrik &amp; Dj Bord</a></div>
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
    font-size: 28px;
    padding: 20px;
    width: 200px;
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

  .button span:after {
    content: '\00bb';
    position: absolute;
    opacity: 0;
    top: 0;
    right: -20px;
    transition: 0.5s;
  }

  .button:hover span {
    padding-right: 25px;
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
</style>
