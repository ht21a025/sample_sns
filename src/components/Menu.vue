<template>
  <div class="ui secondary pointing green inverted massive menu">
    <!-- 基本的なコンテンツはここに記載する -->
    <router-link active-class="active" class="item" exact to="/">Home</router-link>
    <router-link active-class="active" class="item" to="/user">User</router-link>
    <router-link active-class="active" class="item" to="/profile">Profile</router-link>
    <div class="right menu">
      <a @click="logout" class="item">Logout</a>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Menu',

  computed: {
    // 計算した結果を変数として利用したいときはここに記述する
  },

  methods: {
    // Vue.jsで使う関数はここで記述する
    // user() {
    //   this.$router.push({ name: 'User'});
    // }
    
    logout() {
      window.localStorage.clear();
      this.$router.push({ name: 'Login' });
    }
  },
}
</script>

<style scoped>
/* このコンポーネントだけに適用するCSSはここに記述する */
</style>
