<template>
<form action="/search" method="get" id="search-form">
  <div class="form-group">
    <label for="search-articulo" class="form-label-sm">Artículo</label>
    <input
      type="text"
      name="articulo"
      id="search-articulo"
      class="form-control form-control-sm"
      aria-describedby="articulo-help"
      maxlength="50"
      placeholder="Casa, Carro, etc."
      v-model="articulo"
      :state="checkArticulo"
    />
    <small>Mínimo 3 caracteres</small>
  </div>
  <div class="form-group">
    <label for="search-categoria">Categoría</label>
    <select
      name="categoria"
      id="search-categoria"
      class="custom-select form-control-sm"
      v-model="categoria"
    >
      <option value="">Seleccione una categoría...</option>
      <option v-for="categoria in categorias" :key="categoria.id" :value="categoria.name">{{ categoria.name }}</option>
    </select>
  </div>
  <div class="form-group">
    <label>Precio</label>
    <div class="row">
      <div class="col">
        <input
          type="number"
          name="preciobase"
          id="search-preciobase"
          class="form-control form-control-sm"
          v-model="preciobase"
        />
      </div>
      <div class="col">
        <input
          type="number"
          name="preciotope"
          id="search-preciotope"
          class="form-control form-control-sm"
          v-model="preciotope"
        />    
      </div>
    </div>
    
    
  </div>
  <div class="form-group">
    <input type="submit" value="Buscar" class="btn btn-primary form-control" />
  </div>
</form>
</template>
<script>
export default {
    name: 'SearchForm',
    data() {
      return {
        "articulo": "",
        "categoria": "",
        "preciobase": "",
        "preciotope": "",
        "categorias": [
          {
            "id": 1,
            "name": "CARRO"
          },
          {
            "id": 2,
            "name": "CASA"
          },
          {
            "id": 3,
            "name": "VARIOS"
          }
        ]
      }
    },
    computed: {
      checkArticulo() {
        return this.articulo.length > 2 ? true : false
      }
    }
}
</script>