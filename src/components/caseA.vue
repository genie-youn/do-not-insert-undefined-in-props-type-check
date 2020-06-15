<template>
  <h1>{{ msg }}</h1>
</template>

<script>
export default {
  props: {
    msg: {
      type: [String, undefined],
      required: true,
    }
  },
}
</script>
