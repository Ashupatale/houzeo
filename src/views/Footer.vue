<template>
  <div class="">
    <div class="footer">
        <div class="container footerContent">
            <img src="@/assets/Logo.svg"/>
            <p class="copyrightText mt-3">Copyright ©2021 Houzeo Corp.All rights reserved.</p>

        </div>
    </div>
  </div>
</template>

<script>
export default {
    name:'footer-vue'
}
</script>

<style>
.footer{
    height: 70px;
    background-color:#F2F2F5;
}
.copyrightText{
    font-size: 10px;
    float:right;
}
.footerContent{
}
</style>