<template>
  <img alt="Vue logo" src="src/assets/logo.png" />
  <HelloWorld :msg="msg" />
  <button @click="setUndefined">set undefined</button>
  <button @click="setObject">set Object</button>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data() {
    return {
      msg: ""
    }
  },
  methods: {
    setUndefined() {
      console.log("undefined");
      this.msg = undefined;
    },
    setObject() {
      console.log("object");
      this.msg = {
        test: "abc",
      };
    },
  },
}
</script>
