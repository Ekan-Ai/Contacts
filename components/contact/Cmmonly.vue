<template>
  <div>
      <!-- Cmmonly -->
        <div class="flex flex-clear">
            <div class="flex-box">
                <h3>常用联系人</h3>
            </div>
            <span></span>
        </div>
        <!-- PersonItem -->
        <div class="me-list">
            <PersonItem v-for="p in Persons" :key="p.id" :person="p"/>
        </div>
  </div>


</template>

<script>
import PersonItem from './PersonItem'
export default {
    name:'Cmmonly',
    components:{PersonItem},
    computed:{
        Persons(){
            return JSON.parse(window.localStorage.getItem('Persons'))
        }
    }
}
</script>

<style>

</style>