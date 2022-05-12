<template>
  <div class="container">
             <a :href="person.to" class="flex b-line">
                <div class="img-sml">
                    <img :src="person.imgurl" alt="">
                </div>
                <div class="flex-box">
                    <p>{{person.name}}</p>
                    <span>{{person.lastmessage}}</span>
                </div>
                <div class="text">{{person.lastseen}}</div>
            </a>
  </div>
</template>

<script>
export default {
    name:'Personitem',
    props:['person']
}
</script>

<style scoped>
    .container{
        background-color:rgb(237, 241, 244);
        margin-bottom:1px;
    }
</style>