<template>
  <index-view></index-view>
</template>

<script>
import _ from 'lodash';
import $ from 'jquery';
import IndexView from './summary/index.vue';

export default {
  name: "MainView",
  props: {
    global: Object
  },
  components:{
    IndexView
  },
  data() {
    return {
        
    }
  },
  methods: {
    
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

  
</style>
