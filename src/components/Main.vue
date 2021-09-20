<template>
  <div class="container-fluid resetp">
    <div class="container mt-10 mb-10">
      <div class="row py-5">
        <div class="col-7">
          <span class="d-block txt-green fw-bold">WHO WE ARE</span>
          <span class="d-block my-3 fs-1 fw-bold"
            ><span class="txt-green bg-lightgreen p-1"
              ><i class="far fa-gem"></i> Excellence</span
            >
            in Transport</span
          >
          <Lorem />
          <Lorem />
          <Lorem id="pBordered" class="fst-italic ps-5"></Lorem>
          <p>
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Hic
            excepturi accusamus dicta veritatis vero?
          </p>
          <ul>
            <li class="listyle" v-for="(lorem, i) in lorems" :key="i">
              {{ lorems[i] }}
            </li>
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
    <div class="container-fluid bg-darkblue py-5 text-light">
      <div class="container py-5">
        <span class="d-block fw-bold txt-green mb-4">ROAD TRANSPORT</span>
        <h2 class="mb-4 fw-bold">
          Main <span class="bg-darkgreen p-1">Services</span>
        </h2>
        <div class="row">
          <div class="col-7">
            <p class="txt-silver">
              With all of this expertise and capability comes an unrivalled
              commitent to customer service. We will work hard to understand
              your needs in order to develop a productive, long-term
              partnership.
            </p>
          </div>
          <div class="col-5 d-flex justify-content-end align-items-center">
            <span id="SA"><a class="text-light" href="">SEE ALL</a></span>
          </div>
        </div>
        <MainServicesCard />
      </div>
    </div>
    <div id="mainlogi" class="container-fluid text-center py-5 pr">
      <span class="d-block txt-green fw-bold my-4"
        >HOW IT WORK IN PRACTICE</span
      >
      <h2 class="my-4 fw-bold">
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
            >0{{ procedure.id }}</span
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
    <Feedback />
  </div>
</template>

<script>
import Lorem from "./Lorem.vue";
import MainServicesCard from "./MainServicesCard.vue";
import Feedback from "./Feedback.vue";
export default {
  name: "Main",
  components: {
    Lorem,
    MainServicesCard,
    Feedback,
  },
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
    };
  },
};
</script>

<style scoped lang="scss">
@import "../scss/style.scss";
//position
a {
  text-decoration: none;
}
.resetp {
  padding-right: 0;
  padding-left: 0;
}
.pa {
  position: absolute;
  top: 270px;
  left: 50.5%;
  transform: translateX(-50%);
}
ul {
  padding-left: 15px;
}
.iNumber {
  width: 25px;
  margin: auto;
}

//style
.listyle {
  list-style: disc;
}
#pBordered {
  border-left: 4px solid $light-green;
}
.truck {
  width: 100px;
}
.certificate {
  width: 150px;
}
#SA {
  border: 1px solid $green;
  padding: 10px 15px;
  border-radius: 3px;
}

#mainlogi {
  height: 600px;
}
.nLine {
  border: 2px solid $dark-green;
  color: $dark-green;
}
#mainbg {
  background-image: url(../img/bg-10.jpg);
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
}
</style>