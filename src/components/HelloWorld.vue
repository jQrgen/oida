<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
  </div>

  <h2>Music</h2>
  <hr>

  <br>
  <iframe width="100%" height="166" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/924059545&color=%23ff5500&auto_play=true&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true"></iframe><div style="font-size: 10px; color: #cccccc;line-break: anywhere;word-break: normal;overflow: hidden;white-space: nowrap;text-overflow: ellipsis; font-family: Interstate,Lucida Grande,Lucida Sans Unicode,Lucida Sans,Garuda,Verdana,Tahoma,sans-serif;font-weight: 100;"><a href="https://soundcloud.com/oidamusic" title="OIDA" target="_blank" style="color: #cccccc; text-decoration: none;">OIDA</a> · <a href="https://soundcloud.com/oidamusic/dampskip" title="ROLF SAITOTI - DAMPSKIP" target="_blank" style="color: #cccccc; text-decoration: none;">ROLF SAITOTI - DAMPSKIP</a></div>  <br>
  <iframe width="100%" height="166" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/908710864&color=%23ff5500&auto_play=true&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true"></iframe><div style="font-size: 10px; color: #cccccc;line-break: anywhere;word-break: normal;overflow: hidden;white-space: nowrap;text-overflow: ellipsis; font-family: Interstate,Lucida Grande,Lucida Sans Unicode,Lucida Sans,Garuda,Verdana,Tahoma,sans-serif;font-weight: 100;"><a href="https://soundcloud.com/oidamusic" title="OIDA" target="_blank" style="color: #cccccc; text-decoration: none;">OIDA</a> · <a href="https://soundcloud.com/oidamusic/trist" title="GRIM PIL, FEJL &amp; DALER - TRIST" target="_blank" style="color: #cccccc; text-decoration: none;">GRIM PIL, FEJL &amp; DALER - TRIST</a></div>
  <iframe width="100%" height="166" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/918614806&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true"></iframe><div style="font-size: 10px; color: #cccccc;line-break: anywhere;word-break: normal;overflow: hidden;white-space: nowrap;text-overflow: ellipsis; font-family: Interstate,Lucida Grande,Lucida Sans Unicode,Lucida Sans,Garuda,Verdana,Tahoma,sans-serif;font-weight: 100;"><a href="https://soundcloud.com/oidamusic" title="OIDA" target="_blank" style="color: #cccccc; text-decoration: none;">OIDA</a> · <a href="https://soundcloud.com/oidamusic/this-feeling-deep-club" title="TIMMY AKA - THIS FEELING" target="_blank" style="color: #cccccc; text-decoration: none;">TIMMY AKA - THIS FEELING</a></div>
  <br>
  <iframe width="100%" height="450" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/playlists/1151522213&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true"></iframe><div style="font-size: 10px; color: #cccccc;line-break: anywhere;word-break: normal;overflow: hidden;white-space: nowrap;text-overflow: ellipsis; font-family: Interstate,Lucida Grande,Lucida Sans Unicode,Lucida Sans,Garuda,Verdana,Tahoma,sans-serif;font-weight: 100;"><a href="https://soundcloud.com/oidamusic" title="OIDA" target="_blank" style="color: #cccccc; text-decoration: none;">OIDA</a> · <a href="https://soundcloud.com/oidamusic/sets/dnceprty-nyhavna" title="DNCEPRTY @NYHAVNA" target="_blank" style="color: #cccccc; text-decoration: none;">DNCEPRTY @NYHAVNA</a></div>
  <iframe width="100%" height="450" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/playlists/1150631102&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true"></iframe><div style="font-size: 10px; color: #cccccc;line-break: anywhere;word-break: normal;overflow: hidden;white-space: nowrap;text-overflow: ellipsis; font-family: Interstate,Lucida Grande,Lucida Sans Unicode,Lucida Sans,Garuda,Verdana,Tahoma,sans-serif;font-weight: 100;"><a href="https://soundcloud.com/oidamusic" title="OIDA" target="_blank" style="color: #cccccc; text-decoration: none;">OIDA</a> · <a href="https://soundcloud.com/oidamusic/sets/mixed-in-the-basement" title="MIXED BY ANNHANI" target="_blank" style="color: #cccccc; text-decoration: none;">MIXED BY ANNHANI</a></div>
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
