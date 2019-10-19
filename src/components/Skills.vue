<template>
  <div class="hello">
    <div class="holder">
      <form @submit.prevent="addSkill">
        <input type="text" placeholder="Enter a skill" v-model="skill">
      </form>

      <ul>
        <transition-group name="list" enter-active-class="animated bounceInUp" leave-active-class="animated bounceOutDown">
          <li v-for="(data, index) in skills" :key='index'>{{ data.skill }}</li>
        </transition-group>
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
      skill: '',
      skills: [
        {"skill": "Vue.js"},
        {"skill": "JavaScript"},
        {"skill": "Frontend"}
      ]
    }
  },
  methods: {
    addSkill() {
      if (this.skill !== '') {
        this.skills.push({skill: this.skill})
        this.skill = '';
      } else {
        alert('Please type into the field before submitting');
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import "https://cdn.jsdelivr.net/npm/animate.css@3.5.1";

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
  input {
    width: calc(100% - 40px);
    border: 0;
    padding: 20px;
    background-color: #323333;
    color: #687f7f;
    font-size: 16px;
  }
</style>
