<template>
  <div>
    Home
    <div>
      Board List: 
      <div v-if="loading">Loading...</div>
      <div v-else>
        <div v-for="b in boards" :key=b.id>
          <pre>{{b}}</pre>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { board } from '../api/index.js'

export default {
  data() {
    return {
      loading: false,
      boards: '',
      error: ''
    }
  },
  created() {
    this.fetchData()
  },
  methods: {
    fetchData() {
      this.loading = true
      board.fetch()
        .then(res => {
          this.boards = res
        })
        .finally(_=> {
          this.loading = false
        })
    }
  }
}
</script>

<style>

</style>
