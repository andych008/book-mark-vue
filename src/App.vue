<style scoped>
  @import './styles/common.css';
</style>
<template>
  <div>
    <loading :loading.sync="isLoading"></loading>
    <router-view></router-view>
  </div>
</template>
<script>
  import Loading from './components/loading.vue'

  export default {
    components: {
      'loading': Loading
    },
    data () {
      return {
        isLoading: true,
      }
    },
    mounted () {
      setTimeout(() => {
      }, 2000)
      this.isLoading = false
    },
    beforeDestroy () {

    },
    methods: {

    }
  }
</script>
