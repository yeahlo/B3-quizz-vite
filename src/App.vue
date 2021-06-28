<template>
 <Question @answer="onAnswer" label="question ?" :answers="[{label: 'answer 1'},{label: 'answer 2'},{label: 'answer 3'} ]"/>
</template>

<script>
import Question from "./components/Question.vue";
export default {
  components: {Question},
  mounted() {
  },
  methods : {
    onAnswer(index) {
      console.log('index', index);
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
