<script>
const API_URL = `http://lvm64075.sit.kmutt.ac.th:8080/api/students`

export default {
  data: () => ({
    date: null
  }),

  created() {
    // fetch on init
    this.fetchData()
  },

  methods: {
    async fetchData() {
      const url = `${API_URL}`
      this.date = await (await fetch(url)).json()
    }
  }
}
</script>

<template>
  <div>
    <h1>Student</h1>

  <p>{{ date }}</p>
  
  </div>
</template>
