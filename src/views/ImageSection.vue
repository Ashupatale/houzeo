<template>
  <div class="container">

    <div v-if="isPopup">
      <Modal 
        :data-type="dataType"
        :data-set="dataSet"
        @handleClidData="handleChildData"
       />
    </div>
    <div class="row mt-4">
      <div class="MiddleSection justify-content-between">
        <div class="ImageSection">
          <div class="wrapper" v-for="list in HouseDetails" :key="list.id">
            <div class="left" @click="showModal(list.HallImage)">
              <img :src="list.HallImage" class="Img1" />
            </div>
            <div class="right">
              <div @click="showModal(list.BalconyImage)">
                <img :src="list.BalconyImage" class="Img2" />
              </div>
              <div @click="showModal(list.BedImage)">
                <img :src="list.BedImage" class="Img3" />
                
              </div>
            </div>
          </div>
        </div>

        <div class="ShowingSection col-lg-4 p-3">
          <div class="">
            <h6 class="fw-bold">Schedule a Showing </h6>
          </div>
          <button
            class="w-50 calanderTab"
            v-for="tab in tabs"
            :key="tab"
            @click="selected = tab"
            :class="['tab-btn', { activetab: selected === tab }]"
          >
            {{ tab }}
          </button>
          <component :is="selected" class="tab"></component>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import houseOne from "@/assets/houseOne.jpg";
import houseTwoo from "@/assets/houseTwoo.jpg";

import houseThree from "@/assets/houseThree.jpg";
import Modal from "../views/Modal.vue";
import InPersonShowing from "../views/PersonShowingTab.vue";
import VirtualShowing from "../views/VirtualShowingTab.vue";
export default {
  name: "image-section",
  components: {
    Modal,
    InPersonShowing,
    VirtualShowing,
  },
  data() {
    return {
      isPopup: false,
      dataSet: {},
      dataType: 'image',
      tabs: ["InPersonShowing", "VirtualShowing"],
      selected: "InPersonShowing",
      HouseDetails: [
        {
          houseNumber: 1,
          contactNumber: +918788113725,
          HallImage: houseOne,
          BalconyImage: houseTwoo,
          BedImage: houseThree,
        },
      ],
    };
  },
  created() {
    this.$emit("popup", this.isPopup);
  },
  provide() {
    return {
      PopupValue: this.isPopup,
    };
  },
  methods: {
    showModal(data) {
      this.dataType = 'image'
      this.dataSet = data
      this.isPopup = true;
    },
    handleChildData() {
      this.isPopup = false;
    },
  },
};
</script>

<style>
.ShowingSection {
  height: 409px;
  border: 1px solid #0c090926;
  border-radius: 10px;
}



@media (min-width: 600px) {
  .wrapper {
    display: flex;
    height: 100%;
    
  }
  .wrapper .left {
    flex: 2;
    display: flex;
    flex-direction: column;
    width: 350px;
    border-top-left-radius: 10px;
    border-bottom-left-radius: 10px;
    cursor: pointer;

  }
  .wrapper .left .Img1:hover {
  
    transform: scale(1.1);
  }
  .wrapper .right .Img2:hover {
  
  transform: scale(1.1);
}
.wrapper .right div ~ div .Img3:hover {
  
  transform: scale(1.1);
}
  }
  .wrapper .right {
    flex: 1;
    display: flex;
    flex-direction: column;
    width: 350px;
    border-top-right-radius: 10px;
  }
  .wrapper .right div {
    flex: 2;
    cursor: pointer;
  }
  .wrapper .right div ~ div {
    flex: 2;
    border-bottom-right-radius: 10px;
    cursor: pointer;
  }
  .Img1 {
    height: 100%;
    border-bottom-left-radius: 10px;
    border-top-left-radius: 10px;
    transition: all 1s;

  }
 
  .Img2 {
    height: 95%;
    width: 90%;
    float: right;
    border-top-right-radius: 10px;
    transition: all 1s;

  }
  .Img3 {
    transition: all 1s;

    height: 95%;
    width: 90%;
    float: right;
    margin-top: 5%;
    border-bottom-right-radius: 10px;
  }


.tab-btn {
  padding: 6px 10px;
  cursor: pointer;
  border: 5px solid #f2f2f2;
  background-color: #f2f2f2;
  outline: none;
}

.activetab {
  background-color: #fff;
  font-weight: bold;
}

.tab {
  padding: 10px;
}
.AllPhotos{
  position: absolute;
  bottom:15%;
  right:45%;
  color:black;
  border:1px solid black;
  padding: 3px 10px;
  background-color:white

}

.AllPhotos i{
  color:black;
}

@media (min-width: 769px) {
  .MiddleSection {
    display: flex;
    text-align: start;
    justify-content: start;
    flex-wrap: wrap;
  }
  
}

@media (min-width: 769px) and (max-width: 1199px) {
  .MiddleSection {
    display: block;
    text-align: start;
    justify-content: start;
    flex-wrap: wrap;
  }
  .ShowingSection {
    margin-top: 5%;
  }
  .AllPhotos{
  position: absolute;
  bottom:15%;
  right:45%;
  color:white;
}
}
@media (min-width: 992px) and (max-width: 1199px) {
  .ShowingSection {
    width: 100%;
    margin-top: 5%;
  }

  .AllPhotos{
  position: absolute;
  bottom:15%;
  right:45%;
  color:white;

}
}

@media (max-width: 599px) {
  .Img1,
  .Img2,
  .Img3 {
    width: 100%;
    height: auto;
    margin-bottom: 4%;
  }
 
}
</style>
