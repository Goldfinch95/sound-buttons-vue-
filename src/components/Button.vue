<!--Caja hijo, aqui solo involucra la propiedad del hijo que proviene de la caja padre-->

<script>
export default {
  props: {
    button: {
      name: {
        type: String,
        required: true,
      },
      img: {
        type: String,
        required: true,
      },
      sound: {
        type: String,
        required: true,
      },
    },
  },
};
</script>

<template>
  <button>
    <img :src="button.img" />
    {{ button.name }}
  </button>
</template>

<style scoped>
button {
  display: flex;
  justify-content: space-around;
  margin: 25px;
  margin-top: 60px;
  padding: 13px;
  background-color: #2b2d31;
  height: 5vh;
  width: 27vw;
  border-radius: 7px;
  font-size: 13px;
  text-align: end;
  border: none;
  color: #fff;
}
button:focus {
  border: 1px solid green;
}

img {
  height: 100%;
}
</style>

<!--import jsonData from "../assets/data.json"; console.log(jsonData);-->
