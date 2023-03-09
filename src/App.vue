<template>
  <div>
    <first_component />
    <LifeCycle />
    <Pessoa />
  </div>
  
</template>


<script>
  import first_component from './components/first_component.vue'
  import LifeCycle from './components/LifeCycle.vue'
  import Pessoa from './components/Pessoa.vue'

  export default{
    name: 'App',
    components:{
      first_component,
      LifeCycle,
      Pessoa
    }
  }
</script>