<template>
  <div class="conatiner1">
    <div class="image-container">
      <div class="image"></div>
    </div>

    <div class="popup-image">
      <a @click="handleClose" style="color: white">&times;</a>
      <!-- {{ dataSet }} -->
      {{ dataType }}
      <span
        class="OfferSpan p-3"
        style="
          color: white;
          font-size: 16px;
          font-weight: normal;
          text-decoration: underline;
          float: right;
        "
        >Make an offer</span
      >
      <div v-if="dataType == 'image'">
        <img :src="dataSet" />
      </div>
      <div v-else>
        <iframe src="https://www.youtube.com/embed/tgbNymZ7vqY?autoplay=1&mute=1" class="IframeDive"></iframe>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "modal-vue",
  isActive: "isActive",
  //   inject:['PopupValue'],
  //   isPopup:this.PopupValue,

  props: {
    dataType: {
      type: String,
      default: "",
    },
    dataSet: {
      type: Object,
      default: function () {
        return {};
      },
    },
  },


  mounted() {
    console.log("mounted", this.PopupValue);
  },

  methods: {
    handleClose() {
      console.log("hit ");
      this.$emit("handleClidData", "close");
    },
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
}
.isActive {
  display: none;
}
.container1 {
  position: relative;
  min-height: 100vh;
  background-color: #ddd;
}
.image-container {
  display: flex;
  flex-wrap: wrap;
  gap: 1;
  justify-content: center;
}
.popup-image {
  position: fixed;
  background-color: rgba(0, 0, 0, 0.9);
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  z-index: 100;
}
.popup-image img {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  border: 5px solid #fff;
  border-radius: 5px;
  width: 750px;
  object-fit: cover;
}
.popup-image a {
  position: absolute;
  top: 0;
  left: 0px;
  font-size: 40px;
  font-weight: bolder;
  color: #fff;
  cursor: pointer;
}

@media (max-width: 768px) {
  .popup-image img {
    width: 95%;
    height: auto;
  }
}
</style>
