<template>
  <div class="container">
    <div class="row">
      <div class="col">
        <span class="d-block">WHO WE ARE</span>
        <span class="d-block"
          ><span><i class="far fa-gem"></i> Excellence</span> in Transport</span
        >
        <p>
          Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dolores
          veniam cumque labore iusto deleniti. Sed exercitationem, quo tenetur,
          reiciendis, deleniti perferendis ex aliquam expedita earum dolor
          assumenda doloremque quaerat temporibus.
        </p>
        <p>
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Enim maxime
          repellat necessitatibus dolorum fuga a eius alias, voluptas veritatis
          ipsa numquam aut cupiditate, recusandae placeat facere, laboriosam
          impedit eveniet est?
        </p>
        <p>
          Lorem ipsum, dolor sit amet consectetur adipisicing elit. Atque error
          odio praesentium provident quia unde molestias est doloremque at in
          architecto aliquam labore eveniet possimus dignissimos, incidunt
          repudiandae repellat soluta.
        </p>
        <p>
          Lorem ipsum, dolor sit amet consectetur adipisicing elit. Hic
          excepturi accusamus dicta veritatis vero?
        </p>
        <ul>
          <li v-for="(lorem, i) in lorems" :key="i">{{ lorems[i] }}</li>
        </ul>
      </div>
      <div class="col">
        <span class="d-block">Veichle Types</span>
        <div v-for="vehicle in vehicles" :key="vehicle.id" class="vehicle-card my-5">
            <img class="truck img-fluid" src="../img/truck-1.png" alt="">
            <span>{{vehicle.name}}</span>
            <span> {{vehicle.weight}}</span>
        </div>
        <span class="d-block">Certifications</span>
        <img class="img-fluid certificate" src="../img/certificate.png" alt=""><img class="img-fluid certificate" src="../img/certificate.png" alt="">
      </div>
    </div>
  </div>
</template>

<script>
export default {
name: "Main",
data(){
    return{
        lorems: ["Lorem ipsum dolor sit amet", "Consectetur adipiscing elit", "Integer in pretium nisl atiquet", "Dapibus hendrerit maurius curabitur"],
        vehicles: [
            {
                name: "Light",
                weight: "Max weight 1200kg",
                id: 1
            },
            {
                name: "Medium",
                weight: "Max weight 6000kg",
                id: 2
            },
            {
                name: "Heavy",
                weight: "Max weight 24000kg",
                id: 3,
            }
        ],
    }
}
}
</script>

<style scoped lang="scss">
.truck{
    width: 75px;
}
.certificate{
    width: 100px;
}

</style>