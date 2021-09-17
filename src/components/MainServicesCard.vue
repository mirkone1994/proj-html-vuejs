<template>
  <div class="row justify-content-between">
          <div
            v-for="service in services"
            :key="service.id"
            class="col-3 services-card"
          >
            <i class="fas fa-arrow-right fs-4 txt-green"></i>
            <i
              class="
                icon
                fs-5
                mt-5
                mb-4
                px-3
                rounded-circle
                txt-green
                bg-darkgreen
              "
              :class="service.img"
            ></i>
            <span class="d-block px-3">{{ service.name }}</span>
            <p class="my-4 mb-5 px-3">{{ service.overview }}</p>
          </div>
        </div>
</template>

<script>
export default {
    name: "MainServicesCard",
    data(){
      return {
        services: [
        {
          img: "fas fa-truck-loading",
          name: "Technology",
          overview:
            "We are continually focused on developing technology solutions adapted to our client's needs.",
          id: 1,
        },
        {
          img: "fas fa-temperature-low",
          name: "Refer Cargo",
          overview:
            "Regular and frequent monitoring from the recipt of the loaded container to final destionation.",
          id: 2,
        },
        {
          img: "fas fa-boxes",
          name: "Dry Cargo",
          overview:
            "We work with most types of dry cargo, from valuable cargo ti the most dangerous requiring care.",
          id: 3,
        },
      ],
      }
    }

}
</script>

<style>
.icon {
  padding: 18px;
  margin-left: 15px;
}
.fa-arrow-right {
  position: absolute;
  top: 50px;
  right: 50px;
}
.services-card {
  background-color: #19191f;
  border-radius: 10px;
  position: relative;
}

</style>