<script lang="ts">

export default {
  data: function () {
    return {
      cards: [
        {
          image: "/src/assets/prime.png",
          title: "Test title 1",
          text: "Text 1",
          footer: "Footer 1",
        },
        {
          image: "/src/assets/eletronics_amazon.png",
          title: "Test title 2",
          text: "Text 2",
          footer: "Footer 2",
        },
        {
          image: "/src/assets/young_on_phone.png",
          title: "Test title 3",
          text: "Text 3",
          footer: "Footer 3",
        },
      ],
      carouselItems: [
        {
          pathImage: "/src/assets/ebook_amazon_cover.jpg",
          alt: "Consulte o ebook da Amazon",
        },
        {
          pathImage: "/src/assets/amazon_dia_das_maes.jpg",
          alt: "Veja as ofertas para o dia das mães",
        },
      ],
    };
  },
};

// const getImage = (imagePath: string) => {
//   return require(imagePath);
// };
</script>

<template>
  <main class="container">
    <div id="carouselExampleControls" class="carousel slide" data-bs-ride="carousel">
      <div class="carousel-inner">
        <div class="carousel-item active">
          <img
            src="@/assets/alexa_amazon_cover.jpg"
            class="d-block w-100"
            alt="Itens da Alexa"
          />
        </div>
        <div class="carousel-item" v-for="carouselItem in carouselItems">
          <img
            :src="`${carouselItem.pathImage}`"
            class="d-block w-100"
            :alt="`${carouselItem.alt}`"
          />
        </div>
      </div>
      <button
        class="carousel-control-prev"
        type="button"
        data-bs-target="#carouselExampleControls"
        data-bs-slide="prev"
      >
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Anterior</span>
      </button>
      <button
        class="carousel-control-next"
        type="button"
        data-bs-target="#carouselExampleControls"
        data-bs-slide="next"
      >
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Próximo</span>
      </button>
    </div>

    <div
      class="align-items-center row row-cols-1 row-cols-md-3 row-cols-sm-2 text-center justify-content-center row-cols-lg-3"
    >
      <div class="col mb-3 mt-5" v-for="card in cards">
        <div class="card">
          <img :src="`${card.image}`" class="card-img-top rounded" alt="..." />
          <div class="card-body align-items-stretch">
            <h5 class="card-title">Card title</h5>
            <p class="card-text">
              {{ card.text }}
            </p>
          </div>
          <div class="card-footer">
            <small class="text-muted">Last updated 3 mins ago</small>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<style scoped>

</style>