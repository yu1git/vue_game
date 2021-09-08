<template>
  <div id="app" class="continer mx-auto mt-4" style="width:300px">
    <!--<HelloWorld title="Hello" message="※これは、Vue3のサンプルプロジェクトです。"></HelloWorld>
    <GoodBye title="Bye" message="サンプル" comment="sample"></GoodBye>-->
    <!--クイズ用のコンポーネントを呼び出して書く-->
    <Quiz title="Quiz" v-bind:quiz="mondai" />
    <Answer answer="回答1" a2="回答2" a3="回答3" a4="回答4" />
    <Answer answer="回答使いまわし"></Answer>
    <Answer v-bind:answer="kotae.A"></Answer>
    <Answer v-bind:answer="kotae.B"></Answer>
  </div>
</template>
<script>
// import HelloWorld from "./components/HelloWorld.vue";
// import GoodBye from "./components/GoodBye.vue";
import Quiz from "./components/Quiz.vue";
import Answer from "./components/Answer.vue";

export default {
  name: "App",
  components: {
    // HelloWorld,
    // GoodBye,
    Quiz,
    Answer,
  },
  data(){
    return{
      mondai:"テスト",
      kotae:{
      A:"変数",
      B:"変数2",
      }
    }
  }
};
</script>

