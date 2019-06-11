<template>
  <div id="app">
    <router-view />
  </div>
</template>

<style lang="scss">
* {
  padding: 0;
  margin: 0;
}

.btn {
  display: block;
  width: 200px;
  height: 40px;
  line-height: 40px;
  margin: 0 auto;
  margin-top: 20px;
  border-radius: 3px;
  text-align: center;
  color: #fff;
  background-color: #3498db;
  cursor: pointer;
}
.btn:hover {
  background-color: #1c8ad4;
}
</style>
