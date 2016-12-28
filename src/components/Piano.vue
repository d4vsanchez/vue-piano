<template>
  <div id="piano">
    <piano-key v-for="tone in tones" :tone="tone"></piano-key>
  </div>
</template>

<script>
import PianoKey from './PianoKey.vue'

export default {
  name: 'piano',
  data () {
    return {
      tones: [
        'C3',
        'C#3',
        'D3',
        'D#3',
        'E3',
        'F3',
        'F#3',
        'G3',
        'G#3',
        'A3',
        'A#3',
        'B3'
      ]
    }
  },
  components: {
    PianoKey
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#piano {
  display: inline-block;
  margin: 0 auto;
}
</style>
