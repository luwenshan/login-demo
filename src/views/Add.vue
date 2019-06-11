<template>
  <div>
    <p>标题</p>
    <input type="text" v-model="title">
    <p>内容</p>
    <input type="text" v-model="content">
    <div class="btn" @click="add()">添加</div>
  </div>
</template>

<script>
import store from "@/store";
export default {
  name: "Add",
  store,
  data() {
    return {
      title: "",
      content: ""
    };
  },
  methods: {
    add() {
      if (this.title != "" && this.content != "") {
        store.commit("addItem", {
          title: this.title,
          content: this.content
        });
        this.title = "";
        this.content = "";
        this.$router.push("/home/list");
      } else {
        alert("标题内容不能为空！");
      }
    }
  }
};
</script>

