<template>
  <div>
    <h1 class="aboutBA d-flex justify-content-center align-items-center m-5">Contact Us</h1>
    <div class="d-flex justify-content-around flex-row">
      <div class="w-300 d-flex flex-column">
        <h3>Свежест 42</h3>
        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Vitae cupiditate porro corrupti, magnam delectus perspiciatis libero tenetur expedita quod adipisci sunt itaque aspernatur fuga explicabo nisi repellendus similique esse maiores!</p>
        <a href>
          <i class="fab fa-facebook-square">Facebook</i>
        </a>
      </div>
      <div class="d-flex flex-column">
        <div class="d-flex mt-2 flex-row align-items-center">
          <i class="fas mr-2 fa-map-marker-alt"></i>
          <p>Burgas, Karnobat,</p>
        </div>
        <div class="d-flex mt-2 flex-row align-items-center">
          <i class="fas mr-2 fa-phone-volume"></i>
          <a href="tel:+359889456119">0889 456 119</a>
        </div>
        <div class="d-flex mt-2 flex-row align-items-center">
          <i class="fas mr-2 fa-file-contract"></i>
          <a href>общи условия</a>
        </div>
        <div class="d-flex mt-2 flex-row align-items-center">
          <i class="fas mr-2 fa-user-tie"></i>
          <a href>защита на личните данни</a>
        </div>
      </div>
      <div></div>
    </div>
  </div>
</template>

<style scoped>
.fas,
.fab {
  font-size: 25px;
  color: #3498db;
  transition: 0.2s ease-in-out;
}
.fas:hover,
.fab:hover {
  color: #226b9c;
}
.w-300 {
  width: 300px;
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
</style>