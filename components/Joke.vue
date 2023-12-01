<template>
  <nuxt-link :to="'jokes/' + id">
    <div class="joke">
      <p>{{ joke }}</p>
    </div>
  </nuxt-link>
</template>

<script>
export default {
  name: "Joke",
  props: ["joke", "id"],
};
</script>

<style>
.joke {
  padding: 1rem;
  margin: 1rem;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
  cursor: pointer;
}
.joke:hover {
  background: #f4f4f4;
  color: #000;
}
</style>
