
<template>
  <div>
    <video-player  class="video-player-box"
                   :options="playerOptions"
                   :playsinline="false"

                   @play="onPlayerPlay($event)"
                   @pause="onPlayerPause($event)">
    </video-player>
  </div>
</template>
<script>
  import 'video.js/dist/video-js.css'

  import { videoPlayer } from 'vue-video-player'

  export default {
    data() {
      return {
        playerOptions: {
          // videojs options
          sources: [{
            type: "video/mp4",
            src: "https://cdn.theguardian.tv/webM/2015/07/20/150716YesMen_synd_768k_vp8.webm"
          }],
        }
      }
    },
    components: {
      videoPlayer
    },
    methods: {
      // listen event
      onPlayerPlay(player) {
        // console.log('player play!', player)
      },
      onPlayerPause(player) {
        // console.log('player pause!', player)
      },
      // ...player event

      // or listen state event
      playerStateChanged(playerCurrentState) {
        // console.log('player current update state', playerCurrentState)
      },

    }
  }
</script>
