<template>
<div>
  <main id="main">
    <section id="animal-header" class="animal-header">
      <div class="container" data-aos="fade-up">
        <div class="section-title">
          <h2>관심지역 동행</h2>
          <p>나와 함께 사는 반려동물을 위한</p>
          <br>
          <div class="d-flex justify-content-center">
            <div class="me-3 animal-button"><router-link to="/animalhospital"><div class="animalH"></div></router-link></div>
            <div class="ms-3 animal-button"><router-link to="/animalpharmacy"><div class="animalP"></div></router-link></div>
          </div>
        </div>
      </div>
    </section>
  </main>
  <div id="animal-body" class="animal-body">
    <div class="container-fluid container" data-aos="fade-up">
      <router-view></router-view>
      <!-- default : AnimalChart, 동물병원 클릭시 AnimalDetail-hospital, 동물약국 클릭시 AnimalDetail-hospital-->
    </div>
  </div>
</div>
</template>
<script>
export default {
  name:'Animal', 
}
</script>

<style>
.animal-button:hover{
  opacity: 0.5;
}
.animalH{
  width: 320px;
  height: 120px;
  background: url("/img/hospital_move.png");
  border: 2px solid rgb(235, 235, 235);
}

.animalP{
  width: 320px;
  height: 120px;
  background: url("/img/pharmacy_move.png");
  border: 2px solid rgb(235, 235, 235);
}
</style>