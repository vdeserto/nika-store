<template>
  <main>
    <div class="container d-grid col-6">
      <h4>Faça seu cadastro</h4>
      <form class="d-grid">
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
          />
        </div>
        <div class="form-group">
          <label for="pwd"
            ><span class="text-danger">*</span>Digite uma senha</label
          >
          <input class="form-control" type="password" name="pwd" id="pwd" />
        </div>
        <div class="form-group">
          <label for="pwd2"
            ><span class="text-danger">*</span>Digite a senha novamente</label
          >
          <input class="form-control" type="password" name="pwd2" id="pwd2" />
        </div>

        <button class="btn btn-primary btn-submit my-2" type="submit">
          Criar seu cadastro
        </button>
      </form>
    </div>
  </main>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
