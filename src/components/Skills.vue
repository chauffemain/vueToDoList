<template>
  <div class="hello">
    <div class="holder">
      <ul>
        <li v-for="(data, index) in skills" :key="index">
          {{ index }}. {{ data.skill }}
        </li>
      </ul>
    </div>
    <div>
      <p v-if="skills.length >= 1">You have more than one skill</p>
      <p v-else>You have one or less skills</p>
    </div>

    <div v-bind:class="{ alert: showAlert, 'another-Class': showClass }"></div>
  </div>
</template>

<script>
export default {
  name: "Skills",
  data() {
    return {
      //properties and values
      skills: [{ skill: "Vue" }, { skill: "Frontend dev" }],

      showAlert: true,
      showClass: true
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped src="./Skills.css">
,
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
