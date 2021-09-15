<template>
    <div class="header container_fluid">
        <div class="container">
            <div class="row justify-content-between">
                <div class="col">
                    <span>Open Hours: Mon - Sat - 9.00 - 18.00</span>
                </div>
                <div class="col">
                    <ul>
                        <li v-for="(contact, i) in hContacts" :key="i"><i :class="hContacts[i]"></i></li>
                    </ul>
                </div>
            </div>
            <div class="row">

            </div>
        </div>
    </div>  
</template>

<script>
export default {
    name: "Header",
    data(){
        return {
            hContacts: ['fas fa-phone-alt', 'fas fa-envelope', 'fab fa-facebook-f', 'fab fa-twitter', 'fab fa-linkedin-in']
        }
    }
}
</script>

<style scoped lang="scss">
ul {
    list-style: none;
}
li {
    display: inline;
    padding: 0 20px;
}

</style>