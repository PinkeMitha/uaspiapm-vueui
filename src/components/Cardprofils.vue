<template>
<div class="row">
  <div class 
  v-for="(profil, index) in profils" :key="index">
  <div class="card-header"><center>Profile
  </center></div>
  <div class="card">
  <div class="card-body">
     <h5 class="card-title">{{profil.nama}}</h5>
    <h5 class="card-title">{{profil.ttl}}</h5>
    <h5 class="card-title">{{profil.jk}}</h5>
    <h5 class="card-title">{{profil.agama}}</h5>
    <h5 class="card-title">{{profil.alamat}}</h5>
  </div>
  <div class="card-footer text-muted">
           <center> <router-link
              class="btn btn-success"
              :to="{ name: 'Editprofils', params: { id: profil.id } }"
              >Edit</router-link
            >
            </center>
  </div>
</div>
</div>
</div>
</template>

<script>
export default {
    props: ["profils"],
}
</script>

<style>

</style>