<template>
  <div>
        <!-- Enterprice -->
        <div class="flex flex-clear">
            <div class="flex-box">
                <h3>企业通讯录</h3>
            </div>
            <span>立即创建</span>
        </div>
        
        <!-- List -->
        <div class="me-list">
            <EnterpriveItem v-for="i in Items" :key="i.id" :item="i"></EnterpriveItem>
        </div>
  </div>
</template>

<script>
import EnterpriveItem from './EnterpriceItem'
export default {
    name:'Enterprice',
    components:{EnterpriveItem},
    computed:{
        Items(){
            return JSON.parse(window.localStorage.getItem('Items'))
        }
    }
}
</script>

<style>

</style>