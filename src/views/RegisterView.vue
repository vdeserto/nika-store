<template>
    <main>
        <div class="container d-grid col-6">
            <h4>Faça seu cadastro</h4>
            <form class="d-grid">
                <div class="form-group">
                    <label for="fullName">Nome Completo</label>
                    <input class="form-control" type="text" name="fullName" id="fullName">
                </div>

                <div class="form-group">
                    <label for="gender">Gênero</label>
                    <select class="form-select d-grid" aria-label="Gênero">
                        <option selected>Selecione...</option>
                        <option value="1">Masculino</option>
                        <option value="2">Feminino</option>
                        <option value="3">Outro</option>
                        <option value="4">Prefiro não informar</option>
                    </select>
                </div>
                <div class="form-group">
                    <label for="documentNumber">CPF/CNPJ</label>
                    <input class="form-control" type="text" name="documentNumber" id="documentNumber">
                </div>
                <div class="form-group">
                    <label for="pwd">Digite uma senha</label>
                    <input class="form-control" type="password" name="pwd" id="pwd">
                </div>
                <div class="form-group">
                    <label for="pwd2">Digite a senha novamente</label>
                    <input class="form-control" type="password" name="pwd2" id="pwd2">
                </div>

                <button class="btn btn-primary btn-submit my-2" type="submit">Fazer Login</button>
            </form>
            <small>Ainda não tem um cadastro? Registre-se <router-link :to="{ name: 'register' }"
                    class="link-secondary">aqui.</router-link></small>
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
  