<script setup lang="ts">
const name = "login";
</script>
<template>
  <main>
    <div class="container d-grid col-6">
      <h4>Faça seu login</h4>
      <form class="d-grid">
        <div class="form-group">
          <label for="documentNumber">CPF/CNPJ</label>
          <input class="form-control" type="text" name="documentNumber" id="documentNumber">
        </div>
        <div class="form-group">
          <label for="pwd">Senha</label>
          <input class="form-control" type="password" name="pwd" id="pwd"> 
        </div>        

        <button class="btn btn-primary btn-submit my-2" type="submit">Fazer Login</button>
      </form>
      <small>Ainda não tem um cadastro? Registre-se <router-link :to="{ name: 'register' }" class="link-secondary">aqui.</router-link></small>
    </div>
  </main>
</template>

