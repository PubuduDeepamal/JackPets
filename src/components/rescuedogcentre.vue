<template>
   
    <div id="bcolour">
    <br>
    <div class="section-header text-center mx-auto mb-5 wow fadeInUp"  data-wow-delay="0.1s" style="max-width: 500px;">
          <h2 id="producttittle" class="producttittle">Sherlock Rescue Dog Centre</h2>
          <p>(Do you want to raise these orphaned pets? You can request.)</p>
    </div>
    <div class="container mx-auto max-w-2xl md:py-12 sm:px-6 sm:py-24 lg:max-w-7xl lg:px-8">
      <div class="row row-cols-1 gap-4 gap-lg-5">
        <div v-for="pets in pets" :key="pets.id" class="col mb-4">
          <div class="group hover:scale-105 delay-150 rounded1 shadow1 product-card">
            <div class="overflow-hidden h-60 rounded1-md lg:aspect-none d-flex align-items-center justify-content-center mx-auto group-hover:opacity-75">
              <img :src="pets.imageSrc" :alt="pets.imageAlt" class="img-fluid h-60 object-fit-center" />
            </div>
                <p class="prdoutdetailseliment"> <b>{{ pets.name }}</b></p>
                <button class="btn btn-primary w-100 py-1 px-4 rounded1 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500" id="BuyButton">
                <b> Request</b>
                </button>
          </div>
        </div>
      </div>
    </div>
  <br>
</div>
  </template>
  
  <script>

  import rescuedogcentre from '../assets/json/rescuedogcentre.json'
  
    export default {
        name: "ProductCardMain",
        data(){ 
            return { 
              pets:rescuedogcentre
  
            };
        },
    }
  </script>
  
  <style lang="scss" scoped>
  
  .row-cols-1 > * {
      flex: 275px;
      width: 100%;
  }
  
  #BuyButton{
    background:white;
    border-color: #f0d8b6;
    color: black;
  }
  
  #BuyButton:hover{
      background:#f0d8b6;
      color: black;
      border: black;
  }
  
  .img-fluid {
      padding: 20px;
  }
  
  .prdoutdetailseliment{
    text-align: center;
  }
  
  .w-100 {
      width: 80% !important;
      margin-bottom: 20px;
      margin-left: 10%;
  }
  
  .rounded1 {
      border-radius: 10px;
  }
  
  .shadow1 {
      border: 1px solid #f0d8b6;
  }
  
  .shadow1:hover {
      box-shadow: 0 0.2rem 0.4rem #f0d8b6;
      border: 1px solid #f0d8b6;
  }
  
  #sectioncolour{
    background: #f8f8f8;
  }
  
  .producttittle{
    font-size: 45.8px;
    margin-top: 0px;
    font-weight: bold;
  }
  
  .rounded1{
      background: white;
  }

  #bcolour{
    background: #f8f8f8;
  }
  </style>