<template>
  <div class="leads">
    <Logo />
    <!-- <Logo dark-background /> -->
    <h1 class="leads__title">Leads</h1>
    <p v-for="lead in leads" :key="lead.id">{{ lead.company.bs }}</p>
    <div class="search_container">
      <h3>Buscar por nome</h3>
      <InputSearch />
    </div>
    <div class="list_container">
      <div v-for="lead in leads" :key="lead.id" class="card">
        <h2>{{ lead.name }}</h2>
        <h3>Usuário: {{ lead.username }}</h3>
        <p>Empresa: {{ lead.company.name }}</p>
        <p>
          Website: <a href="{ lead.website }">{{ lead.website }}</a>
        </p>
        <address>
          <p>
            <a href="mailto:{ lead.email }">{{ lead.email }}</a>
          </p>
          <p>
            <a href="`tel:${ lead.phone }">{{ lead.phone }}</a>
          </p>
          <p>Rua: {{ lead.address.street }}, {{ lead.address.suite }}</p>
          <p>Cidade: {{ lead.address.city }}</p>
          <p>CEP: {{ lead.address.zipcode }}</p>
        </address>
      </div>
    </div>
  </div>
</template>

<script>
import InputSearch from '@/components/InputSearch'
export default {
  components: {
    InputSearch,
  },
  async asyncData({ $http }) {
    const leads = await $http.$get('https://jsonplaceholder.typicode.com/users')
    return { leads }
  },
}
</script>

<style lang="css" scoped="true">
.leads {
  background: rgb(251, 248, 248);
  padding: 2rem;
}
.search_container {
  margin: 0 0 2rem 0;
}
.leads__title {
  margin: 1.4rem 0;
  padding: 1.4rem 0;
  font-weight: 300;
  text-align: center;
}
.list_container {
  display: grid;
  grid-template-columns: 2fr 2fr 2fr;
  gap: 3rem;
  border-top: 1px solid lightgray;
  padding-top: 3rem;
}
.card {
  text-align: start;
  border: 1px solid lightgray;
  border-radius: 5px;
  box-shadow: 2px 2px 2px gray;
  padding: 2rem 2rem 2rem 3rem;
}
.card p {
  margin: 1rem;
}
address {
  margin-top: 1rem;
}
a {
  text-decoration: none;
}
</style>
