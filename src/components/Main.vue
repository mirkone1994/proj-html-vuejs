<template>
  <div class="container-fluid">
    <div class="container">
      <div class="row mt-10 mb-10">
        <div class="col-7">
          <span class="d-block txt-green fw-bold">WHO WE ARE</span>
          <span class="d-block my-3 fs-1 fw-bold"
            ><span id="excellence" class="txt-green bg-lightgreen"
              ><i class="far fa-gem"></i> Excellence</span
            >
            in Transport</span
          >
          <p>
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dolores
            veniam cumque labore iusto deleniti. Sed exercitationem, quo
            tenetur, reiciendis, deleniti perferendis ex aliquam expedita earum
            dolor assumenda doloremque quaerat temporibus.
          </p>
          <p>
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Enim
            maxime repellat necessitatibus dolorum fuga a eius alias, voluptas
            veritatis ipsa numquam aut cupiditate, recusandae placeat facere,
            laboriosam impedit eveniet est?
          </p>
          <p id="pBordered" class="fst-italic ps-5">
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Atque
            error odio praesentium provident quia unde molestias est doloremque
            at in architecto aliquam labore eveniet possimus dignissimos,
            incidunt repudiandae repellat soluta.
          </p>
          <p>
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Hic
            excepturi accusamus dicta veritatis vero?
          </p>
          <ul>
            <li v-for="(lorem, i) in lorems" :key="i">{{ lorems[i] }}</li>
          </ul>
        </div>
        <div class="col-5">
          <span class="d-block fs-4 fw-bold ps-4">Veichle Types</span>
          <div
            v-for="vehicle in vehicles"
            :key="vehicle.id"
            class="container vehicle-card my-4"
          >
            <div class="row">
              <div class="col-3">
                <img
                  class="truck img-fluid bg-lightgreen p-2"
                  src="../img/truck-1.png"
                  alt=""
                />
              </div>
              <div class="col">
                <span class="fs-4 fw-bold">{{ vehicle.name }}</span
                ><br />
                <span> {{ vehicle.weight }}</span>
              </div>
            </div>
            <hr class="my-4 w-75" />
          </div>
          <span class="d-block ps-4 fs-4 fw-bold">Certifications</span>
          <img
            class="img-fluid certificate ps-4 my-3"
            src="../img/certificate.png"
            alt=""
          /><img
            class="img-fluid certificate ps-4 my-3"
            src="../img/certificate.png"
            alt=""
          />
        </div>
      </div>
    </div>
    <div class="container-fluid bg-black py-5 text-light">
        <div class="container py-5">
            <span class="d-block txt-green mb-4">ROAD TRANSPORT</span>
            <h2 class="mb-4 fw-bold">Main <span class="bg-darkgreen p-1">Services</span></h2>
            <div class="row">
                <div class="col-7">
                    <p>With all of this expertise and capability comes an unrivalled commitent to customer service. We will work hard to understand your needs in order to develop a productive, long-term partnership.</p>
                </div>
                <div class="col-5 d-flex justify-content-end align-items-center">
                    <span id="SA">SEE ALL</span>
                </div>
            </div>
            <div class="row justify-content-between">
                <div v-for="service in services" :key="service.id" class="col-3 services-card">
                    <i class="fas fa-arrow-right fs-4 txt-green"></i>
                    <i class="icon fs-5 mt-5 mb-4 px-3 rounded-circle txt-green bg-darkgreen" :class="service.img"></i>
                    <span class="d-block px-3">{{service.name}}</span>
                    <p class="my-4 mb-5 px-3">{{service.overview}}</p>
                </div>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Main",
  data() {
    return {
      lorems: [
        "Lorem ipsum dolor sit amet",
        "Consectetur adipiscing elit",
        "Integer in pretium nisl atiquet",
        "Facilisis in pretium nisl aliquet",
        "Dapibus hendrerit maurius curabitur",
      ],
      vehicles: [
        {
          name: "Light",
          weight: "Max weight 1200kg",
          id: 1,
        },
        {
          name: "Medium",
          weight: "Max weight 6000kg",
          id: 2,
        },
        {
          name: "Heavy",
          weight: "Max weight 24000kg",
          id: 3,
        },
      ],
      services: [
          {
              img: "fas fa-truck-loading",
              name: "Technology",
              overview: "We are continually focused on developing technology solutions adapted to our client's needs.",
              id: 1
          },
          {
              img: "fas fa-temperature-low",
              name: "Refer Cargo",
              overview: "Regular and frequent monitoring from the recipt of the loaded container to final destionation.",
              id: 2
          },
          {
              img: "fas fa-boxes",
              name: "Dry Cargo",
              overview: "We work with most types of dry cargo, from valuable cargo ti the most dangerous requiring care.",
              id: 3
          }
      ]
    };
  },
};
</script>

<style scoped lang="scss">
.bg-lightgreen {
  background-color: #daeced;
}
.bg-darkgreen {
    background-color: #0e272d;
}
#excellence {
  padding: 5px;
}
.txt-green {
  color: #058283;
}
#pBordered {
  border-left: 4px solid #daeced;
}
ul {
  padding-left: 15px;
}
.truck {
  width: 100px;
}
.certificate {
  width: 150px;
}
#SA {
  border: 1px solid #058283;
  padding: 10px 15px;
  border-radius: 3px;
}
.services-card {
    background-color: #19191f;
    border-radius: 10px;
    position: relative;
}
.icon {
    padding: 18px;
    margin-left: 15px;
}
.fa-arrow-right {
    position: absolute;
    top: 50px;
    right: 50px;
}
</style>