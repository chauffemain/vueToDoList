<template>
  <div class="hello">
    {{ name }}
    {{ btnState ? "The button is disabled" : "The button is active" }}
    <div class="holder">
      <ul>
        <li v-for="(data, index) in skills" :key="index">
          {{ index }}. {{ data.skill }}
        </li>
      </ul>
    </div>
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
      btnState: true,
      skills: [{ skill: "Vue" }, { skill: "Frontend dev" }]
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
