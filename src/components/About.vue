<template>
  <div class>
    <h1 class="d-flex justify-content-center align-items-center m-5 aboutBA">About</h1>
    <div class="d-flex mr-5 flex-row">
      <div>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Deserunt voluptatum aliquid voluptatem cum dolores ratione. Veniam voluptatem ex impedit a!</p>
        <div class="d-flex mt-4 flex-row">
          <i class="fas mr-3 fa-check-double"></i>
          <p>Lorem ipsum dolor sit amet.</p>
        </div>
        <div class="d-flex flex-row">
          <i class="fas mr-3 fa-check-double"></i>
          <p>Lorem ipsum dolor sit ametdas.</p>
        </div>
        <div class="d-flex flex-row">
          <i class="fas mr-3 fa-check-double"></i>
          <p>Lorem ipsum dolor sit amet tis.</p>
        </div>
      </div>
      <div>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Deserunt voluptatum aliquid voluptatem cum dolores ratione. Veniam voluptatem ex impedit a!</p>
        <img class="mb-3 imageRound" src="@/assets/Svejest42.jpg" alt />
        <a href class="btn btn-outline-primary">Read more</a>
      </div>
    </div>
  </div>
</template>

<style scoped>
.imageRound {
  border-radius: 5px;
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
.fas {
  color: #3498db;
}
</style>