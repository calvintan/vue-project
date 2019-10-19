<template>
  <div class="hello">
    <div class="holder">
      <ul>
        <li v-for="(data, index) in skills" :key='index'>{{ data.skill }}</li>
      </ul>

      <p>These are your skills.</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Skills',
  data() {
    return {
      skills: [
        {"skill": "Vue.js"},
        {"skill": "JavaScript"},
        {"skill": "Frontend"}
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  ul {
    margin: 0;
    padding: 0;
    list-style-type: none;
  }
  ul li {
    padding: 20px;
    background-color: #e0edf4;
    border-left: 5px solid #3eb3f6;
    margin-bottom: 2px;
    color: #3e5252;
  }
  p {
    text-align: center;
    padding: 30px;
    color: #aaa;
  }
  .container {
    box-shadow: 0 0 40px lightgray;
  }
</style>
