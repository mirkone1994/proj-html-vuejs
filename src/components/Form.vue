<template>
  <form class="row g-3">
    <div class="col-md-6">
      <input type="text" class="form-control" placeholder="Name" />
    </div>
    <div class="col-md-6">
      <input
        type="email"
        class="form-control"
        id="inputEmail4"
        placeholder="Email"
      />
    </div>
    <div class="col-md-6">
      <input type="number" class="form-control" placeholder="Phone" />
    </div>
    <div class="col-md-6">
      <select id="inputState" class="form-select">
        <option selected>More Info</option>
        <option>...</option>
      </select>
    </div>
    <div class="mb-3">
      <textarea
        class="form-control"
        id="exampleFormControlTextarea1"
        rows="6"
        placeholder="Message"
      ></textarea>
    </div>
    <div class="col-12">
      <button type="submit" class="btn bg-green text-light">SEND</button>
    </div>
  </form>
</template>

<script>
export default {
  name: "Form",
};
</script>

<style scoped lang="scss">
</style>