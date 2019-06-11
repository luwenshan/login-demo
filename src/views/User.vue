<template>
  <div>
    <div class="btn" @click="add()">添加</div>
  </div>
</template>

<script>
export default {
  name: "User",
  methods: {
    add() {
      this.$router.push("/add");
    }
  }
};
</script>

<style lang="scss" scoped>

</style>

