<template>
  <div>
    <myheader></myheader><kojima></kojima><kojima></kojima>
    <p v-if="msg.length > 0">
      {{msg}}
    </p>
    <p v-else>
      no text
    </p><kojima></kojima><kojima></kojima><kojima></kojima><kojima></kojima>
    <input type="text" v-model="msg">
    <button @click="clear()">clear</button>
  </div>
  
</template>

<script>
import myheader from './components/myheader'
import kojima from './components/kojima'

export default {
  components: {
    myheader,
    kojima
  },
  data () {
    return {
      msg: 'Hello World!'
    }
  },
  methods: {
    clear () {
      this.msg = ''
    }
  }
}
</script>