// Fetching image from randomuser api and displaying it
<script>
const TheWelcome = {
  data() {
    return {
      image: "https://randomuser.me/api/portrails/men/10.jpg",
    };
  },
};
//Fetch api
 function fetchapi() {
  async function fetchText() {
    let response = await fetch("https://randomuser.me/api/");
    let data = await response.json();
    console.log(data);
    fetchText();
  }
}
// calling async function
</script>
<template>
  <div>
    <img src="https://randomuser.me/api/portraits/men/19.jpg" />
    <!-- calling async function in onclick -->
    <button
      v-on:click="
        {
          fetchapi();
        }
      "
    >
      Click
    </button>
  </div>
</template>
<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Courier+Prime&family=Maven+Pro&family=Mulish:wght@300&family=Open+Sans&display=swap");

img {
  border-radius: 50%;
  height: 220px;
}
button {
  position: absolute;
  transform: translate(50%, 120%);
  background: rgb(36, 34, 34);
  color: hsla(160, 100%, 37%, 1);
  border: none;
  font-size: 30px;
  padding: 15px 80px;
  font-family: "Maven Pro", sans-serif;
}
</style>
