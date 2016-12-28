<template>
  <div class="key"
       v-bind:class="isMajor"
       @click.stop="sound(tone)">
    <p>{{ tone }}</p>
  </div>
</template>

<script>
import Tone from 'tone'

var synth = new Tone.Synth().toMaster()

export default {
  name: 'piano-key',
  props: {
    tone: {
      type: String,
      required: true
    }
  },
  data () {
    return {
    }
  },
  computed: {
    isMajor: function () {
      return {
        major: this.tone.includes('#')
      }
    }
  },
  methods: {
    sound: function (tone) {
      synth.triggerAttackRelease(tone, '8n')
    }
  }
}
</script>

<style scoped>
.key {
  border: 1px solid #CCCCCC;
  float: left;
  height: 250px;
  width: 80px;
  position: relative;
  z-index: 1;
}

.key p {
  bottom: 0;
  color: black;
  cursor: default;
  font-size: 11px;
  text-align: center;
  position: absolute;
  width: 100%;

  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.key.major {
  background: #000000;
  border: none;
  height: 180px;
  width: 50px;
  margin-left: -27px;
  position: relative;
  z-index: 2;
}

.key.major p {
  color: #FFFFFF;
}

.key.major + .key {
  margin-left: -25px;
}
</style>
