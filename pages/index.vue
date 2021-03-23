<template>
  <div class="leads">
    <Logo />
    <!-- <Logo dark-background /> -->
    <div class="list_container">
      <h1 class="leads__title">Leads</h1>
      <ul>
        <li v-for="lead in leads" :key="lead.id">
          {{ lead.username }}
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  async asyncData({ $http }) {
    const leads = await $http.$get('https://jsonplaceholder.typicode.com/users')
    return { leads }
  },
}
</script>

<style lang="css" scoped="true">
.leads__title {
  margin: 1.4rem 0;
  padding: 1.4rem 0;
  font-weight: 300;
}
.list_container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-top: 1px solid lightgray;
}
li {
  list-style: none;
  margin: 1.4rem;
}
</style>
