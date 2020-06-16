<template lang="html">

  <div class="joke-list" v-if="jokes.length">
    <joke-list-item
      v-for="(joke, index) in jokes"
      :joke="joke"
      :key="index"
    >
    </joke-list-item>
  </div>

</template>

<script>

import JokeListItem from "@/components/JokeListItem";

export default {
  name: "joke-list",
  props: ["jokes"],
  components: {
    "joke-list-item": JokeListItem
  }
};

</script>

<style lang="css" scoped>

</style>