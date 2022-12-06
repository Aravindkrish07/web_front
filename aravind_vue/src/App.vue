<template>
  <div class="container">
    <!-- #3 must use the component-->
    <Header siteName="Top 5 Anime" 
      authorName=" by Aravind Kumar Dhamodharan"/>

    <Companybox :companies="companies"  />

  </div>
</template>

<script>
//import Header and Companybox

import Header from './components/Header.vue'
import Companybox from './components/Companybox.vue'

export default {
  name: 'App',
  components: {
    // 2 register the component 
    Header,
    Companybox
  },
  data(){
    return {
      companies: []
    }
  },
  methods: {

// promises

  async fetchBooks(){
      const res = await fetch('http://localhost:8367/companies')
      const data = await res.json()
      console.log(data.companies)
      return data.companies
  }


},
  async created(){
    this.companies = await this.fetchCompanies()
}
}
</script>



<style>

@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Montserrat', sans-serif;
}
.container {
  max-width: 1000px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 5px;
}

div{
  margin-bottom: 0.5em;
}



</style>


