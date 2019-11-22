<template>
  <div class="d-flex back align-items-center justify-content-center">
    <div
      style="border: none; display: flex;
  flex-direction: column;
  width: fit-content;
  background: rgba(66, 66, 78, 0.24) !important;
  border-radius: 30px !important;
  justify-content: center;"
      class="card"
    >
      <div class="card-header" style="border-radius: 30px 30px 0px 0px; border: none;">
        <div class="row justify-content-center">
          <span
            style="color: rgba(255,255,255,.74); font-size: 17px;"
            class="mx-auto font-Mont my-2"
          >LOGIN CUSTOMIZADO</span>
        </div>
      </div>

      <div style="flex-direction: column;" class="card-body d-flex">
        <md-field>
          <label style="margin-left:2rem">E-mail</label>
          <md-icon>
            <img src="../assets/Subtraction4.svg" />
          </md-icon>
          <md-input></md-input>
        </md-field>
        <md-field :md-toggle-password="false">
          <label style="margin-left:2rem">Senha</label>
          <md-icon>
            <img src="../assets/Cadeado.svg" />
          </md-icon>
          <md-input type="password"></md-input>
        </md-field>
        <div class="row mx-0 align-items-center">
          <md-checkbox v-model="boolean">Lembrar-me</md-checkbox>
          <md-button style="margin-left: 35px; text-transform: none; font-style: italic; margin-bottom: .5rem; color: rgba(255,255,255,.64)">Esqueceu a senha?</md-button>
        </div>
        <div class="row mx-0 justify-content-center">
          <md-button id="loginBtn" class="md-raised">Login</md-button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    boolean: false
  })
};
</script>

<style>
.back {
  height: 100vh;
  background: url("../assets/Group1.png");
  background-size: cover;
}
.md-focused label {
  margin-left: 0px !important;
  color: white !important;
}
.md-has-value label {
  margin-left: 0px !important;
}
.md-focused .md-input {
  color: white !important;
  -webkit-text-fill-color: white !important;
}
.md-checkbox .md-checkbox-label {
  margin: 0px 0px .15rem 0px !important;
  color: rgba(255, 255, 255, .64);
}
.md-checkbox-container {
  background: rgba(46, 46, 54, .44);
  border-radius: 3px !important;
  border-color: transparent !important;
}
.md-checkbox .md-checkbox-container:before {
    width: 0px !important;
    height: 0px !important;
}
.md-checked .md-checkbox-container{
  background: rgba(46, 46, 54, .8) !important;
}
.md-checkbox {
    margin: 0 !important;
}
.md-button:active, .md-button:hover {
  color: white !important;
}
.md-checkbox.md-checked label{
  color: white !important;
}
.md-checkbox .md-checkbox-container:after {
    opacity: 1 !important;
    border: 2px solid rgba(255,255,255,.42) !important;
    border-top: 0 !important;
    border-left: 0 !important;
    transform: rotate(45deg) scale3D(1,1,1) !important;
    transition: .4s cubic-bezier(.25,.8,.25,1) !important;
}
.md-checkbox.md-checked .md-checkbox-container:after {
    opacity: 1 !important;
    border: 2px solid white !important;
    border-top: 0 !important;
    border-left: 0 !important;
    transform: rotate(45deg) scale3D(1,1,1) !important;
    transition: .4s cubic-bezier(.25,.8,.25,1) !important;
}
.md-button.md-raised {
  width: 168px;
  height: 43px;
}
</style>