<template>
  <div class="black-bg" v-if="모달창열렸니 === true">
    <div class="white-bg">
      <h4>상세페이지임</h4>
      <p>상세페이지 내용임</p>
    </div>
  </div>

  <div class="menu">
    <a v-for="원룸 in 메뉴들" :key="원룸">{{ 원룸 }}</a>
  </div>
  <div>
    <img alt="Vue logo" src="./assets/room0.jpg" class="room-img" />
    <h4>{{ products[0] }}</h4>
    <p>{{ price1 }}만원</p>
    <button v-on:click="신고수[0]++">허위매물신고</button>
    <span>신고수 : {{ 신고수[0] }} </span>
  </div>
  <div>
    <img alt="Vue logo" src="./assets/room1.jpg" class="room-img" />
    <h4>{{ products[1] }}</h4>
    <p>{{ price2 }}만원</p>
    <button v-on:click="신고수[1]++">허위매물신고</button>
    <span>신고수 : {{ 신고수[1] }} </span>
  </div>
  <div>
    <img alt="Vue logo" src="./assets/room2.jpg" class="room-img" />
    <h4>{{ products[2] }}</h4>
    <p>{{ price2 }}만원</p>
    <button v-on:click="신고수[2]++">허위매물신고</button>
    <span>신고수 : {{ 신고수[2] }} </span>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      모달창열렸니: true,
      price1: 60,
      price2: 70,
      products: ["역삼동원룸", "천호동원룸", "개화동원롬", "마포동원룸"],
      메뉴들: ["Home", "Shop", "About"],
      신고수: [0, 0, 0],
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
.room-img {
  width: 100%;
  margin-top: 40px;
}

body {
  margin: 0;
}
div {
  box-sizing: border-box;
}
.black-bg {
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
  position: fixed;
  padding: 20px;
}
.white-bg {
  width: 100%;
  background: white;
  border-radius: 8px;
  padding: 20px;
}
</style>
