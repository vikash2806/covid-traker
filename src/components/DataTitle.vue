<template>
  <div class='text-center'>
      <h2 class="">{{text}}</h2>
      <div class='title mt-3 mb-10'>
          {{timestamp}}
      </div>
  </div>
</template>

<script>
import moment from 'moment'
export default {
    name: "DataTitle",
    props: ['text','dataDate'],
    computed: {
        timestamp: function() {
            return moment(this.dataDate).format('MMMM Do YYYY, h:mm:s a')
        }
    }
}
</script>

<style>

</style>