<template>
  <div>
    <ul>
      <li
        class="item"
        v-for="(item, index) in pageList"
        :key="index"
        v-on:click="select(index)"
        v-bind:class="{ selected: index == selectIndex}"
      >
        <p class="title">{{item.title}}</p>
        <p class="content">{{item.content}}</p>
      </li>
    </ul>
  </div>
</template>

<script>
import store from "@/store";
export default {
  name: "List",
  store,
  data() {
    return {
      selectIndex: -1
    };
  },
  methods: {
    select(index) {
      if (this.selectIndex == index) {
        this.selectIndex = -1;
      } else {
        this.selectIndex = index;
      }
    }
  },
  computed: {
    pageList() {
      return store.state.list;
    }
  }
};
</script>

<style scoped>
.item {
  display: block;
  width: 94%;
  margin: 20px auto;
  padding: 15px;
  background-color: lightgrey;
  border-radius: 3px;
}
.title {
  font-size: 18px;
  font-weight: bold;
}
.content {
  margin-top: 10px;
}
.selected{
  background-color: green;
  color: white;
}
</style>


