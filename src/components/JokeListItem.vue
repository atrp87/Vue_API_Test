<template lang="html">
  <div>
    <p>{{ joke.quoteText }}</p>
    <p>{{ joke.quoteAuthor }}</p>
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