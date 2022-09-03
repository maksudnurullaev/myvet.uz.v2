<template>
  <!-- view-login-->
  <div class="container">
    <div>
      <h1>Вход</h1>
      <form>
        <div class="mb-3">
          <label for="exampleInputEmail1" class="form-label">Email адрес</label>
          <input
            type="email"
            class="form-control"
            id="exampleInputEmail1"
            aria-describedby="emailHelp"
          />
          <div id="emailHelp" class="form-text">
            Мы никогда не будем делиться вашими персональными данными с кем-либо
            еще.
          </div>
        </div>
        <div class="mb-3">
          <label for="exampleInputPassword1" class="form-label">Пароль</label>
          <input
            type="password"
            class="form-control"
            id="exampleInputPassword1"
          />
        </div>
        <div class="mb-3 form-check">
          <input type="checkbox" class="form-check-input" id="exampleCheck1" />
          <label class="form-check-label" for="exampleCheck1"
            >Оставаться на сайте</label
          >
        </div>
        <button type="submit" class="btn btn-primary">Войти</button>
      </form>
    </div>
  </div>
</template>
