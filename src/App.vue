<template>
    <div id="list-info" v-if="jokes.length">
      <joke-list :jokes="jokes"></joke-list>
    </div>
  
</template>

<script>

import JokeList from "@/components/JokeList";

export default {
  name: "app",
  components: {
    "joke-list": JokeList,
  },
  

  data() {
    return {
      jokes: [],
      selectedJoke: null
    };
  },

   mounted() {
      fetch("https://quote-garden.herokuapp.com/api/v2/quotes/")
        .then(res => res.json())
        .then(data => this.jokes = data.quotes)
        .catch(error => console.log(error))
  },
}
</script>

<style lang="css" scoped>

</style>