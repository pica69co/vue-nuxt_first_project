<template>
  <div>
    <nuxt-link to="/jokes" class="back">Back To Home</nuxt-link>

    <div class="jokeId">
      <h2>{{ joke }}</h2>
    </div>

    <hr class="separator" />
    <small>Joke ID: {{ $route.params.id }}</small>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      joke: {},
    };
  },
  async created() {
    const config = {
      headers: {
        Accept: "application/json",
      },
    };

    try {
      const res = await axios.get(
        `https://icanhazdadjoke.com/j/${this.$route.params.id}`,
        config
      );

      this.joke = res.data.joke;
    } catch (err) {
      console.log(err);
    }
  },
  head() {
    return {
      title: this.joke,
      meta: [
        {
          hid: "description",
          name: "description",
          content: "Best place for corny dad jokes",
        },
      ],
    };
  },
};
</script>

<style>
.jokeId {
  padding: 1rem;
  margin: 1rem;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
}
.back {
  padding: 1rem 2rem;
  margin: 1rem;
  top: 3px;
  border: 1px solid #ccc;
  border-radius: 4px;
  cursor: pointer;
}
</style>
