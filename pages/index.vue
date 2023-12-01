<template>
  <div>
    <h2 class="title">
      Welcome to the <span class="span">Best</span> corny Dad Jokes app on the
      web
    </h2>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: "Welcome To Dad Jokes",
      meta: [
        {
          hid: "description",
          name: "description",
          content: "Best place for corny jokes",
        },
      ],
    };
  },
};
</script>
<style>
.title {
  text-align: center;
  font-size: 2rem;
  color: #33305080;
  font-weight: bold;
}
.span {
  color: blue;
  font-size: 2.5rem;
}
</style>
