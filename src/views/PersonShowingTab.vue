<template>
  <div>
    <Splide
      :options="{ rewind: true, perPage: 4 }"
      aria-label="My Favorite Images"
    >
      <SplideSlide class="mt-2">
        <p class="PersonDate" @click="activetab = 1" :class="{activeBtn: activetab === 1}">
            <span class="spanText">Mon</span>
            <span class="number">09</span>
            <span class="spanText">May</span>
        </p>
      </SplideSlide>
      <SplideSlide class="mt-2" >
        <p class="PersonDate"  @click="activetab = 2" :class="{activeBtn: activetab === 2}">
            <span class="spanText">Tue</span>
            <span class="number">10</span>
            <span class="spanText">May</span>
        </p>      </SplideSlide>
      <SplideSlide class="mt-2">
        <p class="PersonDate"  @click="activetab = 3" :class="{activeBtn: activetab === 3}">
            <span class="spanText">Wed</span>
            <span class="number">11</span>
            <span class="spanText">May</span>
        </p>      </SplideSlide>
      <SplideSlide class="mt-2">
         <p class="PersonDate"  @click="activetab = 4" :class="{activeBtn: activetab === 4}">
            <span class="spanText">Thur</span>
            <span class="number">12</span>
            <span class="spanText">May</span>
        </p>
      </SplideSlide>
      <SplideSlide class="mt-2">
         <p class="PersonDate"  @click="activetab = 5" :class="{activeBtn: activetab === 5}">
            <span class="spanText">Fri</span>
            <span class="number">13</span>
            <span class="spanText">May</span>
        </p>
      </SplideSlide>
      <SplideSlide class="mt-2">
         <p class="PersonDate"  @click="activetab = 6" :class="{activeBtn: activetab === 6}">
            <span class="spanText">Sat</span>
            <span class="number">14</span>
            <span class="spanText">May</span>
        </p>
      </SplideSlide>
    </Splide>

    <div>
        <Splide class="SplideTwo"
      :options="{ rewind: true, perPage: 4 }"
      aria-label="My Favorite Images"
    >
      <SplideSlide class="mt-3">
        <p class="PersonTime pt-2">09.30 AM</p>
      </SplideSlide>
      <SplideSlide class="mt-3">
        <p class="PersonTime pt-2">10.00 AM</p>
      </SplideSlide>
      <SplideSlide class="mt-3">
        <p class="PersonTime pt-2">10.30 AM</p>
      </SplideSlide>
      <SplideSlide class="mt-3">
        <p class="PersonTime pt-2">11.00 AM</p>
      </SplideSlide>
      <SplideSlide class="mt-3">
        <p class="PersonTime pt-2">11.30 AM</p>
      </SplideSlide>
      <SplideSlide class="mt-3">
        <p class="PersonTime pt-2">12.00 AM</p>
      </SplideSlide>
    </Splide>
    </div>

    <div>
        <button class="form-btn w-100" type="submit" >Schedule Showing</button>
    </div>
    <div>
        <p class="spanText mt-3">It’s free, with no obligation - cancel anytime All times <br/> in EDT</p>

    </div>
  </div>
</template>

<script>
import '@splidejs/vue-splide/css';

// or other themes


// or only core styles
import '@splidejs/vue-splide/css/core';
import { Splide, SplideSlide } from '@splidejs/vue-splide';
export default {
    name:'person-vue',
    components: {
    Splide,
    SplideSlide,
  },
  data(){
    return{
      activetab:1,
      activeButton: 'button1'
    }
  },

  
    
  
  
  
}
</script>

<style>
.PersonDate{
    border: 1px solid #00000033;
    height:100px;
    border-radius: 10px;
    margin-right:10%;
    padding: 8px;
    cursor: pointer;

}
.activeBtn{
  border:1px solid black;
  background-color: #EBEBF0;
}
.PersonDate:hover{
  border:1px solid black;
}
.PersonTime:hover{
  border:1px solid black;
}
.PersonDate span{
    display:block;
    justify-content: center;
    text-align: center;
}
.number{
    font-size: 25px;
}
.spanText{
    font-size: 12px;
    color:#717171;


}
.PersonTime{
    border: 1px solid #00000033;
    height:36px;
    border-radius: 10px;
    margin-right:10%; 
    font-size: 14px;
    padding: 5px;
    cursor: pointer;
}

.SplideTwo .splide__arrow--prev {
    display: none;
}
.SplideTwo .splide__arrow--next {
   width: 24px;
   height: 24px;
   right:-0.5em
}
.splide__arrow--prev {
    left: -1em;
}
.splide__arrow--next {
    right: -1em;
}
.splide__arrow{
    background:#fff;
    border:1px solid #00000033;
}
.splide__arrow:hover{
    background: rgb(236, 233, 233)
}
@media (max-width: 991px) {
    .PersonTime{
        padding:1px;
        text-align: center;
    }
}
</style>