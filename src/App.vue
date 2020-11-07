<template>
  <div id="app">

    <h1>Would You Rather?</h1>

    <would-you-rather
    v-on:answer-changed="answerChanged"
    v-for="question in questions"
    v-bind:question="question.question"
    v-bind:answer1="question.answer1"
    v-bind:answer2="question.answer2"
    ></would-you-rather>

    <p>You Would Rather...</p>

    <ul>
      <li></li>
      <li></li>
      <li></li>
    </ul>

  </div>
</template>

<script>
import WouldYouRather from './components/WouldYouRather.vue'

export default {
  name: 'App',
  components: {
    WouldYouRather
  },
  data(){
    return {
      questions: [
        {
          id:0,
          question: "Would you rather be a wizard or a superhero?",
          answer1: "wizard",
          answer2: "superhero",
        },
        {
          id:1,
          question: "Would you rather only be able to walk on all fours or only be able to walk sideways like a crab?",
          answer1: "all fours",
          answer2: "like a crab",
        },
        {
          id:2,
          question: "Would you rather start a colony on another planet or be the leader of a small country on Earth?",
          answer1: "colony on another planet",
          answer2: "leader of a small country",
        }
      ],
      answers: []
    }
  },
  methods: {
    answerChanged(choice){
    }
  }
}

</script>

<style>
body {
  background: lightgray;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
