<template>
  <div class="alert alert-info">
    <p v-on:click="doAction">{{ answer }}</p>
    <p>{{ message }}</p>
  </div>
</template>

<script>
export default {
  name: "Answer",
  props: {
    answer: String,
  },
  data() {
    return {
      message: "",
    };
  },
  methods: {
    doAction() {
      if (this.answer === "回答2") {
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