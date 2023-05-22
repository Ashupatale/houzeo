<template>
  <div class="container">
    <div v-if="isPopup">
      <Modal 
        :data-type="dataType"
        :data-set="dataSet"
        @handleClidData="handleChildData"
       />
    </div>
    <div class="mt-4 MainDiv mb-4">
      <div class="DescriptionDiv col-lg-7">
        <div class="d-flex" style="justify-content: space-between">
          <div class="d-flex">
            <span class="d-flex span">
              <span><i class="fa-solid fa-eye"></i></span>
              <span>2.3k</span>
            </span>
            <span class="d-flex span">
              <span><i class="fa-regular fa-heart"></i></span>
              <span>2.3k</span>
            </span>
          </div>
          <div class="d-flex">
            <span class="spanDot mt-1"></span>
            <span class="spansale">For Sale</span>
          </div>
        </div>
        <hr />
        <div>
          <div class="Description">
            <span class="fw-bold">Description</span>
            <p class="mt-2">
              Welcome home to this beautiful center hall Colonial located in
              desirable North Caldwell! This house is the epitome of old-world
              charm meets modern-day living. The first floor boasts an open
              floorplan, including a welcoming foyer and a spacious living room
              for entertaining. The eat-in kitchen exudes modern elegance with a
              marble backsplash, white cabinetry…
            </p>

            <hr />

            <div>
              <span class="fw-bold">Property Details</span>
              <hr />
              <div>
                <table class="tableDiv">
                  <tr></tr>
                  <tr>
                    <td class="tableRow p-2">Type</td>
                    <td class="tableData">Single Family</td>
                  </tr>
                  <tr>
                    <td class="tableRow p-2">Status</td>
                    <td class="tableData">Single Family</td>
                  </tr>
                  <tr>
                    <td class="tableRow p-2">Days on Market</td>
                    <td class="tableData">5</td>
                  </tr>
                  <tr>
                    <td class="tableRow p-2">Open House</td>
                    <td class="tableData">Not Scheduled</td>
                  </tr>
                  <tr>
                    <td class="tableRow p-2">County</td>
                    <td class="tableData">Lincoln</td>
                  </tr>
                  <tr>
                    <td class="tableRow p-2">MLS Name</td>
                    <td class="tableData">Montana Regional MLS</td>
                  </tr>
                  <tr>
                    <td class="tableRow p-2">MLS Number</td>
                    <td class="tableData">22208962</td>
                  </tr>
                </table>
                <hr />

                <table>
                  <tr></tr>
                  <tr>
                    <td class="tableRow p-2">Year Built</td>
                    <td class="tableDataTwo">2002</td>
                  </tr>
                  <tr>
                    <td class="tableRow p-2">Finished Area</td>
                    <td class="tableDataTwo">1,837 sqft.</td>
                  </tr>
                  <tr>
                    <td class="tableRow p-2">Lot Size</td>
                    <td class="tableDataTwo">0.18 acres</td>
                  </tr>
                  <tr>
                    <td class="tableRow p-2">Basement</td>
                    <td class="tableDataTwo">600 sq.ft.</td>
                  </tr>
                  <tr>
                    <td class="tableRow p-2">No. of Stories</td>
                    <td class="tableDataTwo">2</td>
                  </tr>
                  <tr>
                    <td class="tableRow p-2">HOA Fees</td>
                    <td class="tableDataTwo">$110</td>
                  </tr>
                  <tr>
                    <td class="tableRow p-2">Buyer Agent <br />Commission</td>
                    <td class="tableDataTwo">2%</td>
                  </tr>
                </table>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="RealStoriesDiv col-lg-4">
        <div class="p-2">
            <h6 class="fw-bold">Real People. Real Stories.</h6>
            <p>See how buyers & sellers across America are saving on commission using Houzeo technology</p>
            <div class="d-flex">
                <div>
                  <div  @click="showModal('https://www.youtube.com/embed/tgbNymZ7vqY?autoplay=1&mute=1')">
                    <iframe src="https://www.youtube.com/embed/tgbNymZ7vqY?autoplay=1&mute=1" class="IframeDive"></iframe>
                    <p class="userName">Jared Goldfarb
                        <span class="userPosition">Crestone, CO</span>

                    </p>
                  </div>
                  </div>
                <div>
                    <iframe src="https://www.youtube.com/embed/tgbNymZ7vqY?autoplay=1&mute=1" class="IframeDive"></iframe>
                    <p class="userName">Jared Goldfarb
                        <span class="userPosition">Crestone, CO</span>

                    </p>
                </div>
                <div>
                    <iframe src="https://www.youtube.com/embed/tgbNymZ7vqY?autoplay=1&mute=1" class="IframeDive"></iframe>
                    <p class="userName">Jared Goldfarb
                        <span class="userPosition">Crestone, CO</span>

                    </p>
                </div>
            </div>

            <div class="d-flex">
                <div>
                    <iframe src="https://www.youtube.com/embed/tgbNymZ7vqY?autoplay=1&mute=1" class="IframeDive"></iframe>
                    <p class="userName">Jared Goldfarb
                        <span class="userPosition">Crestone, CO</span>

                    </p>
                  </div>
                <div>
                    <iframe src="https://www.youtube.com/embed/tgbNymZ7vqY?autoplay=1&mute=1" class="IframeDive"></iframe>
                    <p class="userName">Jared Goldfarb
                        <span class="userPosition">Crestone, CO</span>

                    </p>
                </div>
                <div>
                    <iframe src="https://www.youtube.com/embed/tgbNymZ7vqY?autoplay=1&mute=1" class="IframeDive"></iframe>
                    <p class="userName">Jared Goldfarb
                        <span class="userPosition">Crestone, CO</span>

                    </p>
                </div>
                
            </div>
            <a href="" class="viewText"> View All Stories</a>

        </div>

      </div>
      
    </div>
  </div>
</template> 

<script>    
import Modal from '@/views/Modal.vue'
export default {
  name: "realStories-vue",
  components: {
    Modal
  },
  data() {
    return {
      isPopup: false,
      dataSet: {},
      dataType: 'video',
    };
  },
  methods: {
    showModal(data) {
      this.dataType = 'video'
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
.viewText{
  color:black;
  float:right;
  font-size: 14px;
}
.Span {
  background-color: #ebebf0;
  width: 90px;
  height: 38px;
  border-radius: 8px;
  text-align: center;
  justify-content: space-evenly;
  cursor: pointer;
}
.DescriptionDiv {
  height: auto;
  border-radius: 10px;
  padding: 10px;
}
.Description span {
  font-size: 20px;
}
.Description p {
  font-size: 16px;
}

.spansale {
  font-size: 14px;
  font-weight: bold;
}

.GreenDot {
  background-color: #00b67b;
  font-size: 1px;
  width: 12px;
  height: 12px;
  border-radius: 3px;
}
.spansale {
  font-size: 14px;
  font-weight: bold;
}
.RealStoriesDiv {
  border: 1px solid #00000026;
  height: 500px;
  border-radius: 10px;
  padding: 10px;
  
}
.MainDiv {
  display: flex;
  justify-content: space-between;
}
.span {
  background-color: #ebebf0;
  margin-left: 10%;
  padding: 5px 12px;
  border-radius: 5px;
}
.tableRow {
  background-color: #fafafc;
  font-weight:bold;
}
.tableData {
  padding-left: 20%;
}
.tableDataTwo {
  padding-left: 40%;
}
.spanDot {
  background-color: #00b67b;
  padding: 5px;
  height: 10px;
}
.viewAll{
    font-size: 14px;
    text-decoration: underline;
    color:black;
    float: right;
}
.IframeDive{
    height: 100px;
    width:100px;
    margin-left:3%;
    border-radius:5px;
}
.userName{
    font-size: 12px;
    text-align: center;
    font-weight: bold;
}
.userPosition{
    font-size:10px;
    color:#e9e0e0;
    text-align: center;

}
@media (max-width: 1024px) {
  .MainDiv {
    display: block;
  }
  .RealStoriesDiv{
    justify-content: center;
    text-align: center;

    height:auto;
  }
  .RealStoriesDiv .d-flex{
     justify-content: center;
    text-align: center;
  }
} 

@media (min-width: 992px) and (max-width: 1199px) {  
  .RealStoriesDiv {
    width: 100%;
    margin-top: 5%;
  }
  .DescriptionDiv {
    width: 100%;
    margin-top: 5%;
  }
}
</style>
