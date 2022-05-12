<template>
  <div>
      <a :href="item.to" class="flex b-line">
            <div class="img-sml">
                <img :src="item.imgurl" alt="">
            </div>
            <div class="flex-box">
                <p>{{item.title}}</p>
            </div>
            <div class="arrow"></div>
        </a>
  </div>
</template>

<script>
export default {
    name:'EnterpriceItem',
    props:["item"]
}
</script>

<style>

</style>