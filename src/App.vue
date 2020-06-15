<template>
  <img alt="Vue logo" src="src/assets/logo.png" />
  <caseA :msg="msg" />
  <button @click="setUndefined">set undefined</button>
  <button @click="setObject">set Object</button>
</template>

<script>
import caseA from './components/caseA.vue'

export default {
  name: 'App',
  components: {
    caseA
  },
  data() {
    return {
      msg: "test",
    }
  },
  methods: {
    setUndefined() {
      console.log("undefined");
      this.msg = undefined;
    },
    setObject() {
      console.log("object");
      // this.msg = {
      //   test: "abc",
      // };
      this.msg = Number(4444);
    },
  },
}
</script>
