<template>
  <div class="container-fluid">
    <div class="container">
      <div class="row py-5">
        <div class="col-7">
          <span class="d-block txt-green fw-bold">WHO WE ARE</span>
          <span class="d-block my-3 fs-1 fw-bold"
            ><span class="txt-green bg-lightgreen p-1"
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
        <h2 class="mb-4 fw-bold">
          Main <span class="bg-darkgreen p-1">Services</span>
        </h2>
        <div class="row">
          <div class="col-7">
            <p>
              With all of this expertise and capability comes an unrivalled
              commitent to customer service. We will work hard to understand
              your needs in order to develop a productive, long-term
              partnership.
            </p>
          </div>
          <div class="col-5 d-flex justify-content-end align-items-center">
            <span id="SA">SEE ALL</span>
          </div>
        </div>
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
      </div>
    </div>
    <div id="mainlogi" class="container-fluid text-center py-5 pr">
      <span class="d-block txt-green fw-bold my-4"
        >HOW IT WORK IN PRACTICE</span
      >
      <h2 class="my-4">
        <span class="bg-lightgreen txt-green p-1 fw-bold">Logistical</span>
        Procedure
      </h2>
      <p class="my-4">
        We work with innovative methodologies to ensure that the entire delivery
        process is done from <br />
        start to finish as planned
      </p>
      <hr class="mt-5 nLine" />
      <div class="row pa justify-content-around w-100">
        <div
          v-for="procedure in procedures"
          :key="procedure.id"
          class="mb-5 col-2 logistics-card text-center"
        >
          <span
            class="d-block iNumber rounded-circle bg-lightgreen txt-green mb-5"
            >{{ procedure.id }}</span
          >
          <span class="d-block fs-3 fw-bold mb-5">{{ procedure.name }}</span>
          <span class="d-block mb-5">{{ procedure.overview }}</span>
        </div>
      </div>
    </div>
    <div id="mainbg" class="container-fluid text-center text-light">
      <div class="container">
        <span class="d-block pt-10 mb-3 txt-green fw-bold"
          >WHAT ARE WE DOING</span
        >
        <h2 class="mb-5 fw-bold">
          <span class="bg-darkgreen p-1">Results</span> in Numbers
        </h2>
        <div class="row justify-content-around">
          <div
            v-for="result in results"
            :key="result.id"
            class="col-2 mt-5 mb-10"
          >
            <span class="d-block txt-green fs-3 fw-bold">{{
              result.numbers
            }}</span>
            <span class="d-block fw-bold">{{ result.type }}</span>
          </div>
        </div>
      </div>
    </div>
    <div class="container-fluid bg-black py-5 text-center text-light">
      <div class="container py-5">
        <span class="d-block txt-green fw-bold mb-4">CUSTOMER TESTIMONIALS</span>
        <h2 class="mb-4 fw-bold">
          Trusted <span class="bg-darkgreen p-1">Feedback</span>
        </h2>
            <p>
              We work intesively in search of ideals that can add up in the lives of our customers. This is what <br>moves us and we are grateful for the recognition.
            </p>
        </div>
        <div class="row justify-content-evenly">
          <div
            v-for="feedback in feedbakcs"
            :key="feedback.id"
            class="col-2 services-card text-start mb-5"
          >
            <img class="w-50 px-3 pt-4 filtered" :src="feedback.img" alt="">
            <p class="my-3 px-3">{{ feedback.overview }}</p>
            <span class="d-block px-3 pb-4">{{ feedback.lorem }}</span>
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
      procedures: [
        {
          id: 1,
          name: "Collection of Information",
          overview: "Lorem ipsum dolor sit arnet consectetur",
        },
        {
          id: 2,
          name: "Service Invoice Sending",
          overview: "Lorem ipsum dolor sit arnet consectetur",
        },
        {
          id: 3,
          name: "Withdrawal of Cargo",
          overview: "Lorem ipsum dolor sit arnet consectetur",
        },
        {
          id: 4,
          name: "Transport Customer Order",
          overview: "Lorem ipsum dolor sit arnet consectetur",
        },
        {
          id: 5,
          name: "Successful Delivery",
          overview: "Lorem ipsum dolor sit arnet consectetur",
        },
      ],
      results: [
        {
          id: 1,
          numbers: 128,
          type: "Certifications",
        },
        {
          id: 2,
          numbers: 230,
          type: "Employees",
        },
        {
          id: 3,
          numbers: 517,
          type: "Customers",
        },
        {
          id: 4,
          numbers: 94,
          type: "Countries Served",
        },
      ],
      feedbakcs: [
        {
          img: require("@/img/logo-1.png"),
          lorem: "Lorem ipsum dolor sit armet, consectetur adipiscing elit.",
          overview:
            "Praesent volutpat justo sit amet elementum malesuada. Praesent sagittis augue justo, in accumsan orci rhoncus at pellentesque.",
          id: 1,
        },
        {
          img: require("@/img/logo-2.png"),
          lorem: "Lorem ipsum dolor sit armet, consectetur adipiscing elit.",
          overview:
            "Praesent volutpat justo sit amet elementum malesuada. Praesent sagittis augue justo, in accumsan orci rhoncus at pellentesque.",
          id: 2,
        },
        {
          img: require("@/img/logo-3.png"),
          lorem: "Lorem ipsum dolor sit armet, consectetur adipiscing elit.",
          overview:
            "Praesent volutpat justo sit amet elementum malesuada. Praesent sagittis augue justo, in accumsan orci rhoncus at pellentesque.",
          id: 3,
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../scss/style.scss";
.pt-10 {
  padding-top: 100px;
}
.bg-almostgreen {
  background-color: #eef4ed;
}
.pr {
  position: relative;
}
.pa {
  position: absolute;
  top: 270px;
  left: 50.5%;
  transform: translateX(-50%);
}
.bg-lightgreen {
  background-color: $light-green;
}
.bg-darkgreen {
  background-color: #0e272d;
}
.txt-green {
  color: $dark-green;
}
.txt-lightgreen {
  color: $light-green;
}
#pBordered {
  border-left: 4px solid $light-green;
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
  border: 1px solid $dark-green;
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
#mainlogi {
  height: 600px;
}
.nLine {
  border: 2px solid $dark-green;
  color: $dark-green;
}
.iNumber {
  width: 25px;
  margin: auto;
}
.fa-arrow-right {
  position: absolute;
  top: 50px;
  right: 50px;
}
#mainbg {
  background-image: url(../img/bg-10.jpg);
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
}
.filtered {
  filter: invert(100%);
}
</style>