<!--Caja Padre: aqui se encuentra los diversos botones. debes poner, en este caso, de donde sacas los datos y la funcion-->

<script>
import Button from "./components/Button.vue";
export default {
  data() {
    return {
      buttons: [
        {
          name: "pato",
          img: "src/assets/images/duck.png",
          sound: "src/assets/sounds/quack.mp3",
        },
        {
          name: "corneta",
          img: "src/assets/images/airhorn.png",
          sound: "src/assets/sounds/airhorn.mp3",
        },
        {
          name: "grillo",
          img: "src/assets/images/cricket.png",
          sound: "src/assets/sounds/cricket.mp3",
        },
        {
          name: "aplausos",
          img: "src/assets/images/clap.png",
          sound: "src/assets/sounds/golf_clap.mp3",
        },
        {
          name: "trompeta",
          img: "src/assets/images/trumpet.png",
          sound: "src/assets/sounds/sad_horn.mp3",
        },
        {
          name: "bateria",
          img: "src/assets/images/batery.png",
          sound: "src/assets/sounds/ba_dum_tsss.mp3",
        },
      ],
    };
  },
  methods: {
    playAudio(button) {
      const audio = new Audio(button.sound);
      audio.play();
    },
  },
  components: {
    Button,
  },
};
</script>

<template>
  <div class="box_buttons">
    <div class="button_container">
      <Button
        v-for="button in buttons"
        :key="button.name"
        @click="playAudio(button)"
        :button="button"
      />
    </div>
  </div>
</template>

<style scoped>
.box_buttons {
  display: flex;
  height: auto;
  width: 100%;
  padding: 15px;
  border: none;
  background-color: #111214;
  border-radius: 12px;
  color: #fff;
}
.button_container {
  width: 80vw;
  height: 60vh;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}
</style>
