<template>
  <div id="app" class="continer mx-auto mt-4" style="width:300px">
    
    <!--クイズ用のコンポーネントを呼び出して書く-->
    <Quiz title="Quiz" v-bind:quiz="mondai" />
    <Answer v-bind:answer="kotae.A" />
    <Answer v-bind:answer="kotae.B" />
    <Answer v-bind:answer="kotae.C" />
    <Answer v-bind:answer="kotae.D" />
  </div>
</template>
<script>
import Quiz from "./components/Quiz.vue";
import Answer from "./components/Answer.vue";

export default {
  name: "App",
  components: {
    Quiz,
    Answer,
  },
  data(){
    return{
      mondai:"テスト",
      kotae:{
      A:"回答1",
      B:"回答2",
      C:"回答3",
      D:"回答4"
      }
    }
  }
};
</script>

