<script setup lang="ts">
import { ref } from "vue";

const mobile = () => (window.innerWidth <= 768 ? "pe-1" : "pe-3");
</script>

<style lang="scss" scoped></style>

<template>
  <div>
    <div>
      <header>
        <!-- Fixed navbar -->
        <nav :class="`navbar navbar-expand-md navbar-dark fixed-top bg-dark ${mobile()}`">
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
            <div class="collapse navbar-collapse" id="navbarCollapse">
              <ul class="navbar-nav me-auto mb-2 mb-md-0">
                <li class="nav-item">
                  <a class="nav-link active" aria-current="page" href="#">Home</a>
                </li>
              </ul>
              <div class="navbar-nav nav-fill col">
                <form class="d-flex">
                  <input
                    class="form-control me-2 col-6"
                    type="search"
                    placeholder=""
                    aria-label="Buscar"
                  />
                  <button class="btn btn-outline-success" type="submit">Buscar</button>
                </form>
              </div>
              <div class="navbar">
                <ul class="navbar-nav mx-auto">
                  <router-link :to="{ name: 'login' }" class="nav-link">
                    <div>Olá, Faça seu login</div>
                  </router-link>
                  <li class="nav-item">
                    <router-link :to="{ name: 'home' }" class="nav-link">
                      Devoluções e Pedidos
                    </router-link>
                  </li>
                  <router-link :to="{ name: 'home' }" class="nav-link d-flex">
                    <div class="nav-item">
                      <picture>
                        <source
                          srcset="/src/assets/cart.png"
                          media="(min-width: 140px)"
                        />
                        <img src="/src/assets/cart.png" alt="..." width="24" />
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
