<template>
  <main>
    <div class="container d-grid col-6">
      <h4>Faça seu cadastro</h4>
      <form class="d-grid" @submit.prevent="register">
        <div class="row">
          <div class="form-group col">
            <label for="fullName"
              ><span class="text-danger">*</span>Nome Completo</label
            >
            <input
              class="form-control"
              type="text"
              name="fullName"
              id="fullName"
              required
              v-model="registerForm.fullName"
            />
          </div>
          <div class="form-group col">
            <label for="birthDate"
              ><span class="text-danger">*</span>Data de Nascimento</label
            >
            <input
              class="form-control"
              type="date"
              name="birthDate"
              id="birthDate"
              placeholder="__/__/____"
              required
              v-model="registerForm.birthDate"
            />
          </div>
        </div>

        <div class="">
          <label for="gender"><span class="text-danger">*</span>Gênero</label>
          <input
            class="form-control"
            list="genderDatalistOptions"
            id="gender"
            placeholder="Digite para pesquisar"
            required
            v-model="registerForm.gender"
          />
          <datalist id="genderDatalistOptions">
            <option value="Masculino" />
            <option value="Feminino" />
            <option value="Outro" />
            <option value="Prefiro não informar" />
          </datalist>
        </div>
        <div class="row">
          <div class="form-group col">
            <label for="documentNumber"
              ><span class="text-danger">*</span>CPF</label
            >
            <input
              class="form-control"
              type="text"
              name="documentNumber"
              id="documentNumber"
              placeholder="___.___.___-__"
              required
              v-model="registerForm.documentNumber"
            />
          </div>
          <div class="form-group col">
            <label for="phone"
              ><span class="text-danger">*</span>Telefone</label
            >
            <input
              class="form-control"
              type="text"
              name="phone"
              id="phone"
              placeholder="(__) _____-____"
              required
              v-model="registerForm.phone"
            />
          </div>
        </div>
        <div class="form-group">
          <label for="email"><span class="text-danger">*</span>E-mail</label>
          <input
            class="form-control"
            type="text"
            name="email"
            id="email"
            placeholder="name@example.com"
            required
            v-model="registerForm.email"
          />
        </div>
        <div class="row">
          <div class="form-group col">
            <label for="pwd"
              ><span class="text-danger">*</span>Digite uma senha</label
            >
            <input
              class="form-control"
              type="password"
              name="pwd"
              id="pwd"
              placeholder="********"
              required
              v-model="registerForm.pwd"
            />
          </div>
          <div class="form-group col">
            <label for="pwd2"
              ><span class="text-danger">*</span>Digite a senha novamente</label
            >
            <input
              class="form-control"
              type="password"
              name="pwd2"
              id="pwd2"
              placeholder="********"
              required
              @keydown="checkPassword"
              v-model="registerForm.pwd2"
            />
          </div>
        </div>

        <button class="btn btn-primary btn-submit my-2" type="submit">
          Criar seu cadastro
        </button>
      </form>
    </div>
  </main>
</template>


<script setup lang="ts">
import { IUser } from '../model/IUser'

let registerForm: IUser

function register(): undefined {
  return undefined
}

function checkPassword(): boolean {
  return false
}

  

</script>


<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
