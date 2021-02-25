<template>
  <div class="hello">
    <div class="shuru" contenteditable="true" ref="msg" @input="changeText">
    </div>
    <div class="shuchu" v-html="text"></div>
  </div>
</template>

<script>
export default {
  name: "index",
  data() {
    return {
      text: "",
    };
  },
  methods: {
    changeText(event) {
        this.text = event.currentTarget.innerText
    //   this.$emit("input", this.$el.innerHTML);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hello {
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: space-around;
}
.shuru {
  width: 40%;
  height: 90vh;
  border: 1px solid #ccc;
  margin-top: 20px;
  background: #36363667;
}
.shuchu {
  width: 50%;
  height: 90vh;
  border: 1px solid #ccc;
  margin-top: 20px;
}
</style>
