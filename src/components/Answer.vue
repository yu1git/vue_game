<template>
  <div class="alert alert-info">
    <p v-on:click="doAction">{{ answer }}</p>
    <!--<button class="btn-info mt-2" v-on:click="doAction">{{ a2 }}</button>
    <button class="btn-info mt-2" v-on:click="doAction">{{ a3 }}</button>
    <button class="btn-info mt-2" v-on:click="doAction">{{ a4 }}</button>-->
    <p>{{ message }}</p>
  </div>
</template>

<script>
export default {
  name: "Answer",
  props: {
    answer: String,
    a2: String,
    a3: String,
    a4: String,
  },
  data() {
    return {
      message: "",
    };
  },
  methods: {
    doAction() {
      if (this.answer === "回答使いまわし") {
        console.log(this.answer);
        this.message = "正解！";
        //this.answer='正解！';はエラー。propsの値を直接変更はできない
      } else {
        this.message = "不正解";
      }
    },
  },
};
</script>