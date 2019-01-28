<template>
  <div class="hello">
    {{ name }}

    <button v-on:click="changeName" v-bind:disabled="btnState">
      Change Name
    </button>
  </div>
</template>

<script>
export default {
  name: "Skills",
  data() {
    return {
      //properties and values
      name: "Owner",
      msg: "Welcome to Your Vue.js App",
      btnState: true
    };
  }
};
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
