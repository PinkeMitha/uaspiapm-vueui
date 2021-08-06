<template>
<div class="row">
  <div class="col-lg-4 mt-3" 
  v-for="(history, index) in historys" :key="index">
  <div class="card-header"> Histori Pendidikan
  </div>
  <div class="card">
  <div class="card-body">
    <h5 class="card-title">{{history.nama}}</h5>
    <p class="card-text">{{history.tahun}}</p>
    
  </div>
  <div class="card-footer text-muted">
   <center> <router-link
              class="btn btn-success"
              :to="{ name: 'Edithistorys', params: { id: history.id } }"
              >Edit</router-link
            >
            <button
              @click.prevent="historyDelete(history.id)"
              class="btn btn-danger"
            >
              Delete
            </button>
            </center>
  </div>
</div>
</div>
</div>
</template>

<script>
export default {
    props: ["historys"],
}
</script>

<style>

</style>