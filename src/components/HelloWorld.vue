<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
  </div>

  <h2>Performances (off-chain)</h2>
  <hr>

  <br>
  <iframe width="100%" height="450" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/playlists/1322369266&color=%23ff5500&auto_play=true&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true"></iframe><div style="font-size: 10px; color: #cccccc;line-break: anywhere;word-break: normal;overflow: hidden;white-space: nowrap;text-overflow: ellipsis; font-family: Interstate,Lucida Grande,Lucida Sans Unicode,Lucida Sans,Garuda,Verdana,Tahoma,sans-serif;font-weight: 100;"><a href="https://soundcloud.com/jqrgen" title="jQrgen" target="_blank" style="color: #cccccc; text-decoration: none;">jQrgen</a> · <a href="https://soundcloud.com/jqrgen/sets/doener-tallrik-dj-bord" title="Döner Tallrik &amp; Dj Bord" target="_blank" style="color: #cccccc; text-decoration: none;">Döner Tallrik &amp; Dj Bord</a></div>
  <br>
  <br>

  <h2>Døner NFT 4 sale (Til salgs)</h2>
  <hr>
  <p><i>See <a href="https://opensea.io/assets/0x495f947276749ce646f68ac8c248420045cb7b5e/82846146539956530579045854039281485655757396760242173571066962143559188217857">OpenSea</a></i></p>
  <nft-card
    contractAddress="0x495f947276749ce646f68ac8c248420045cb7b5e"
    tokenId="82846146539956530579045854039281485655757396760242173571066962143559188217857">
  </nft-card>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component'

@Options({
  props: {
    msg: String
  }
})
export default class HelloWorld extends Vue {
  msg!: string

  mounted () {
    const plugin = document.createElement('script')
    plugin.setAttribute(
      'src',
      'https://unpkg.com/embeddable-nfts/dist/nft-card.min.js'
    )
    plugin.async = true
    document.head.appendChild(plugin)
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
