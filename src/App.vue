<template>
  <img alt="Vue logo" src="src/assets/logo.png" />
  <caseA :msg="msg" />
  <caseB :msg="msg" />
  <button @click="setUndefined">set undefined</button>
  <button @click="setObject">set Object</button>
</template>

<script>
import caseA from './components/caseA.vue'
import caseB from "./components/caseB.vue";

export default {
  name: 'App',
  components: {
    caseA,
    caseB,
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
      this.msg = {
        test: "abc",
      };
    },
  },
}
</script>
