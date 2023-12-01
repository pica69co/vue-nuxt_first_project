<template>
  <header class="header">
    <h1 class="title">Dad jokes</h1>
    <ul>
      <li>
        <nuxt-link to="/"> Home </nuxt-link>
      </li>
      <li>
        <nuxt-link to="/jokes"> Jokes </nuxt-link>
      </li>
      <li>
        <nuxt-link to="/about"> About </nuxt-link>
      </li>
    </ul>
  </header>
</template>
<script>
export default { name: "AppHeader" };
</script>

<style>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 1rem;
  padding-bottom: 1rem;
  border-bottom: 1px dotted #ccc;
  background-color: #f5f5f5;
  padding: 20px;
  text-align: center;
}
.header .title {
  margin: 0;
  font-size: 3rem;
  font-weight: 500;
  color: #526488;
}
.header ul {
  display: flex;
  justify-content: space-between;
  align-items: center;
  list-style: none;
  margin: 0;
  padding: 0;
}
.header a {
  display: inline-block;
  padding: 0.5rem 1rem;
  background: #333;
  color: #fff;
  margin-right: 0.5rem;
}
</style>
