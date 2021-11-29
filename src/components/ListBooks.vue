<template>
  <div>
    <Search />
    <h2>Chiave di ricerca: author - Eco</h2>
    <table class="table table-striped my-5">
      <thead>
        <tr>
          <th scope="col">#</th>
          <th scope="col">Autore</th>
          <th scope="col">Titolo</th>
          <th scope="col">Anno di pubblicazione</th>
          <th scope="col">Anno ultima edizione</th>
          <th scope="col">ISBN ultima edizione</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th scope="row">1</th>
          <td> ... </td>
          <td> ... </td>
          <td> ... </td>
          <td> ... </td>
          <td> ... </td>
        </tr>
      </tbody>
  </table>
  </div>
</template>

<script>

import axios from 'axios';
import Search from './Search'

export default {
  name: 'ListBooks',
  components: {
    Search
  },
  methods:{
    getApi(){
      // chiamata da rendere dinamica
      axios.get('http://openlibrary.org/search.json?author=eco')
      .then(r =>{
        console.log(r.data);
      })
      .catch( e => {
        console.log(e);
      })
    }
  },
  mounted(){
    // mounted serve ora per lanciare subito la chiamata ma poi verrà tolto
    this.getApi();
  }
}
</script>

<style>

</style>