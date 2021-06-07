<template>
    <form action="/search" method="get" id="search-form" class="form">
            <div class="form-group">
              <label for="search-articulo" class="form-label-sm">Artículo</label>
              <input
                type="text"
                name="articulo"
                id="search-articulo"
                class="form-control form-control-sm"
                aria-describedby="articulo-help"
                placeholder="Casa, Carro, etc."
              />
            </div>
            <div class="form-group">
              <label for="search-categoria">Categoría</label>
              <select
                name="categoria"
                id="search-categoria"
                class="custom-select form-control-sm"
              >
                <option value="">Seleccione una categoría...</option>
                <option value="CARRO">CARRO</option>
                <option value="CASA">CASA</option>
                <option value="VARIOS">VARIOS</option>
              </select>
            </div>
            <fieldset>
              <legend>Precio</legend>
              <div class="form-group">
                <input
                  type="number"
                  name="preciobase"
                  id="search-preciobase"
                  class="form-control form-control-sm"
                  placeholder="Desde: $1"
                />
                <input
                  type="number"
                  name="preciotope"
                  id="search-preciotope"
                  class="form-control form-control-sm"
                  placeholder="Hasta: $1,000,000"
                />
              </div>
            </fieldset>
            <div class="form-group">
              <input
                type="submit"
                value="Buscar"
                class="btn btn-primary form-control"
              />
            </div>
          </form>
</template>
<script>
export default {
    name: 'SearchForm',
    setup() {
        
    },
}
</script>