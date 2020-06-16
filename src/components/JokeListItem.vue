<template lang="html">
  <div>
    <p>{{ joke.quote }}</p>
  </div>
</template>

<script>

export default {
  name: "joke-list-item",
  props: ["joke"],
}

</script>

<style lang="css" scoped>

</style>