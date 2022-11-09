<script setup lang="ts">
import { ref } from "vue";

const mobile = () => (window.innerWidth <= 768 ? "pe-1" : "pe-3");
</script>

<style lang="css" scoped>
select.form-select {
    display: none;
  }
.nav-link {
  width: max-content;
}
#navbar{
  margin-bottom: 7.5%;
}
@media (min-width: 768px) and (max-width: 991px){
  #navbarCollapse > .navbar {
    /* flex-direction: column;
    align-items: start; */
    font-size: smaller;
    flex-wrap: nowrap;
  }
  .navbar-nav {
    width: 100%;
  }
  #navbar{
    margin-bottom: 10%;
  }
}
@media (min-width: 480px) and (max-width: 767px) {
  .navbar-nav {
    justify-content: center;
    width: 100%;
  }
  #btnDepartmentsDropDown{
    display: none;
  }
  #navbar{
    margin-bottom: 15%;
  }
}
@media (max-width: 479px) {
  div.navbar-nav {
    width: 100%;
  }
  #btnDepartmentsDropDown{
    display: none;
  }
  #navbar{
    margin-bottom: 20%;
  }
}
</style>

<template>
  <div id="navbar">
    <div>
      <header>
        <!-- Fixed navbar -->
        <nav
          :class="`navbar navbar-expand-md navbar-dark fixed-top bg-dark ${mobile()}`"
        >
          <div :class="`container-fluid ${mobile()}`">
            <router-link class="navbar-brand" :to="{ name: 'home' }">
              <img src="@/assets/nika_store.svg" width="48" />
              Nika Store
            </router-link>
            <button
              class="navbar-toggler"
              type="button"
              data-bs-toggle="collapse"
              data-bs-target="#navbarCollapse"
              aria-controls="navbarCollapse"
              aria-expanded="false"
              aria-label="Toggle navigation"
            >
              <span class="navbar-toggler-icon"></span>
            </button>
            <div
              class="collapse navbar-collapse justify-content-center"
              id="navbarCollapse"
            >
              <div class="navbar">
                <div class="navbar-nav">
                  <form class="input-group d-flex">
                    <button
                      id="btnDepartmentsDropDown"
                      class="btn btn-secondary dropdown-toggle"
                      type="button"
                      data-bs-toggle="dropdown"
                      aria-expanded="false"
                    >
                      Todos
                    </button>
                    <ul class="dropdown-menu">
                      <li>
                        <a
                          class="dropdown-item"
                          href="#"
                          v-for="categoria in categorias"
                          >{{ categoria.title }}
                        </a>
                      </li>
                    </ul>
                    <input
                      class="form-control"
                      type="search"
                      placeholder=""
                      aria-label="Buscar"
                    />
                    <button class="btn btn-outline-secondary" type="submit">
                      Buscar
                    </button>
                  </form>
                </div>
              
                <ul class="navbar-nav">
                  <li class="nav-item align-items-center d-flex">
                      <select
                        class="form-select form-select-sm ml-4"
                        aria-label="Selecionar categoria"
                        @change="handleSelectCategory($event)"
                      >
                        <option selected>Categorias</option>
                        <option v-for="categoria in categorias" :key="categoria.id">
                          {{ categoria.title }}
                        </option>
                      </select>
                  </li>
                  <li class="nav-item">
                    <router-link :to="{ name: 'login' }" class="nav-link">
                      <div>Olá, Faça seu login</div>
                    </router-link>
                  </li>
                  <li class="nav-item">
                    <router-link :to="{ name: 'home' }" class="nav-link">
                      Devoluções e Pedidos
                    </router-link>
                  </li>
                  <router-link :to="{ name: 'home' }" class="nav-link d-flex">
                    <div class="nav-item">
                      <picture>
                        <source
                          srcset="../assets/cart.png"
                          media="(min-width: 140px)"
                        />
                        <img src="../assets/cart.png" alt="..." width="24" />
                      </picture>
                    </div>
                    <div>Carrinho</div>
                  </router-link>
                </ul>
              </div>
            </div>
          </div>
        </nav>
      </header>
    </div>
  </div>
</template>

<script lang="ts">
export default {
  data() {
    return {
      categorias: [
        { id: 163214, title: "Todos os Departamentos" },
        { id: 235673, title: "Apps e Jogos" },
        { id: 167647, title: "Automotivo" },
        { id: 627344, title: "CD e Vinil" },
        { id: 176525, title: "Livros" },
        { id: 774342,title: "Computadores e Informática" },
      ],
    };
  },
  methods:{
    handleSelectCategory(event: Event){
      return 1;
    }
  }
};
</script>

<style lang="css">
  select.form-select {
    display: none;
  }
@media (min-width: 768px) {
  #navbarCollapse > .navbar {
    /* flex-direction: column;
    align-items: start; */
    font-size: smaller;
    flex-wrap: nowrap;
  }
  .navbar-nav {
    width: 100%;
  }
}
@media (min-width: 480px) and (max-width: 767px) {
  .navbar-nav {
    justify-content: center;
    width: 100%;
  }
  #btnDepartmentsDropDown{
    display: none;
  }
}
@media (max-width: 479px) {
  div.navbar-nav {
    width: 100%;
  }
  #btnDepartmentsDropDown{
    display: none;
  }
}
</style>
