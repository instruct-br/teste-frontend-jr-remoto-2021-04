<template>
  <div>
    <select name="">
      <option v-for="lead in leads" :key="lead.id" value="">
        {{ lead.username }}
      </option>
    </select>
  </div>
</template>

<script>
export default {
  data() {
    return {
      leads: null,
    }
  },
  created() {
    this.getLeads()
  },
  methods: {
    getLeads() {
      fetch('https://jsonplaceholder.typicode.com/users')
        .then((response) => response.json())
        .then((response) => {
          this.leads = response
        })
    },
  },
}
</script>

<style></style>
