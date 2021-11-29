<template>
  <div class="row my-5">

    <div class="col-2">
        <p class="text-end pt-2">Ricerca per: </p>
    </div>
    <div class="col-2">
        <select class="form-select" >
          <option value="" selected>Autore</option>
          <option value="">Titolo</option>
        </select>
    </div>
    <div class="col-6">
      <input type="text" class="form-control" placeholder="Cosa devi cercare?">
    </div>
    
    <div class="col-1">
      <button class="btn btn-info">Cerca</button>
    </div>
    <div class="col-1">
      <button class="btn btn-warning">Reset</button>
    </div>

  </div>
</template>

<script>
export default {
  name: 'Search'
}
</script>

<style>

</style>