<template>
  <div>
    <h1 class="aboutBA d-flex justify-content-center align-items-center m-5">Pricing</h1>
    <div class="d-flex flex-wrap justify-content-center align-items-center">
      <div class="box d-flex flex-column justify-content-around m-2">
        <h2>Дълбоко почистване</h2>
        <h3>
          <span>3 лв.</span>/m2
        </h3>
        <ul>
          <div class="d-flex flex-row align-items-center">
            <i class="fas mr-2 fa-clipboard-check"></i>
            <li>Lorem, ipsum dolor.</li>
          </div>
        </ul>
        <a href class="btn btn-primary">Read more</a>
      </div>
    </div>
    <h2 class="d-flex justify-content-center align-items-center m-5">За бизнеса</h2>
    <div class="d-flex flex-wrap justify-content-center align-items-center">
      <div class="box d-flex flex-column justify-content-around m-2">
        <h2>Почистване на плочки</h2>
        <h3>
          <span>3 лв.</span>/m2
        </h3>
        <ul>
          <div class="d-flex flex-row align-items-center">
            <i class="fas mr-2 fa-clipboard-check"></i>
            <li>Lorem, ipsum dolor.</li>
          </div>
        </ul>
        <a href class="btn btn-primary">Read more</a>
      </div>
    </div>
    <h2 class="d-flex justify-content-center align-items-center m-5">Отделни пакети</h2>
    <div class="d-flex flex-wrap justify-content-center align-items-center">
      <div class="box d-flex flex-column justify-content-around m-2">
        <h2>Кухня</h2>
        <h3>
          <span>3 лв.</span>/m2
        </h3>
        <ul>
          <div class="d-flex flex-row align-items-center">
            <i class="fas mr-2 fa-clipboard-check"></i>
            <li>Lorem, ipsum dolor.</li>
          </div>
        </ul>
        <a href class="btn btn-primary">Read more</a>
      </div>
    </div>
  </div>
</template>

<style scoped>
.box {
  color: rgb(99, 99, 99);
}
.box .fas {
  color: #3498db;
}
.box ul li {
  list-style-type: none;
}
.box h2 {
  color: #3498db;
}
span {
  color: #3498db;
}
.aboutBA::before {
  margin-right: 5px;
  content: "";
  width: 50px;
  height: 2px;
  background: #3498db;
  display: inline-block;
}
.aboutBA::after {
  margin-left: 5px;
  content: "";
  width: 50px;
  height: 2px;
  background: #3498db;
  display: inline-block;
}
.box {
  padding: 20px;
  width: 300px;
  height: 400px;
  background-color: #f9f9f9;
}
</style>