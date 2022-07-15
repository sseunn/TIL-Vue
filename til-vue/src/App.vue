<template>
  <div class="menu">
    <a v-for="원룸 in 메뉴들" :key="원룸">{{ 원룸 }}</a>
  </div>
  <img alt="Vue logo" src="./assets/logo.png" />
  <div>
    <h4>{{ products[0] }}</h4>
    <p>{{ price1 }}만원</p>
    <button v-on:click="신고수++">허위매물신고</button>
    <span>신고수 : {{ 신고수 }} </span>
  </div>
  <div>
    <h4>{{ products[1] }}</h4>
    <p>{{ price2 }}만원</p>
  </div>
  <div>
    <h4>{{ products[2] }}</h4>
    <p>{{ price2 }}만원</p>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      price1: 60,
      price2: 70,
      products: ["역삼동원룸", "천호동원룸", "개화동원롬", "마포동원룸"],
      메뉴들: ["Home", "Shop", "About"],
      신고수: 0,
    };
  },
  components: {},
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.menu {
  background: darkslateblue;
  padding: 15px;
  border: 5px;
}
.menu a {
  color: white;
  padding: 10px;
}
</style>
