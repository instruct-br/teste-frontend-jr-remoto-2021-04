<template>
  <div class="container">
    <div class="header-table">
      <span class="company-name">Company</span>
      <span class="notShowMobile">Contact Name</span>
      <span class="notShowMobile">E-mail</span>
      <span class="notShowMobile">Phone</span>
      <span class="notShowMobile">Category</span>
    </div>
    <div class="row-table" v-for="company in companys" :key="company.id">
      <span>{{ company.company.name }} </span>
      <span class="onlyMobile">Contact Name </span>
      <span>{{ company.name }}</span>
      <span class="onlyMobile">E-mail </span>
      <span>{{ company.email }} </span>
      <span class="onlyMobile">Phone </span>
      <span>{{ company.phone }} </span>
      <span class="onlyMobile">Category</span>
      <span>{{ company.company.bs }} </span>
    </div>
  </div>
  </div>
  </template>


<script>
export default {
  data() {
    return {
      companys: [],
    }
  },
  async fetch() {
    this.companys = await fetch(
      'https://jsonplaceholder.typicode.com/users'
    ).then((res) => res.json())
  },
}
</script>

<style lang="scss" scoped="true">

body {
  font-family: 'Roboto', sans-serif;
}

.container {
  max-width: 90%;
  margin: 0 auto;
}

// mudar fontes ara o padrao, tentar usar scss, usar variaveis de cores

.notShowMobile {
  @media screen and (max-width: 768px) {
    display: none;
  }
}
.onlyMobile {
  @media screen and (max-width: 768px) {
    font-weight: bold;
  }
  @media screen and (min-width: 769px) {
    display: none;
  }
}
.header-table {
  background: $primary;
  color: $grey;
  padding: 8px;
  border-radius: 4px;
  margin-bottom: 24px;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
  @media screen and (max-width: 768px) {
    grid-template-columns: 1fr;
  }
}
.row-table {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
  border-top: $border-color 1px solid;
  padding: 16px;
  @media screen and (max-width: 768px) {
    grid-template-columns: 1fr;
  }
}
</style>