<template>
  <form @submit.prevent="onsubmit">
    <input
      type="text"
      name="search"
      v-model="text"
      id="search"
      placeholder="Search Jokes..."
    />
    <input type="submit" value="Search" class="searchButton" />
  </form>
</template>

<script>
export default {
  name: "SearchJokes",
  data() {
    return {
      text: "",
    };
  },
  methods: {
    onsubmit() {
      this.$emit("search-text", this.text);
      this.text = "";
    },
  },
};
</script>
<style>
.searchButton {
  background: #333050;
  color: #fff;
  border-radius: 20%;
  padding: 0.5rem;
  cursor: pointer;
}
</style>
