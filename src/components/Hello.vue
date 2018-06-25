<template>
        <div>
          <h2>Welcome to my CRUD Test Website </h2>
          <h1>MEVN App</h1>
        <router-link v-bind:to="{ name: 'Posts' }" class="">See all Posts</router-link>
      </div>
</template>

<script>
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
