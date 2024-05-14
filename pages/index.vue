<template>
  <div class="container-fluid">
    <div class="row my-5">
      <div class="col-lg-6">
        <nuxt-link to="/pengunjung/tambah">
          <div class="card bg-pengunjung rounded-5">
            <div class="card-body">
              <h2>Pengunjung</h2>
            </div>
          </div>
        </nuxt-link>
      </div>

      <div class="col-lg-6">
        <nuxt-link to="/buku">
          <div class="card bg-buku rounded-5">
            <div class="card-body">
              <h2>Cari Buku</h2>
            </div>
          </div>
        </nuxt-link>
      </div>
    </div>
  </div>
   <h1 class="statistik">STATISTIK</h1>

   <div class="container-fluid">
      <div class="row my-5">
         <div class="col-lg-6">
           <nuxt-link to="/pengunjung">
             <div class="card bg-warning rounded-5">
               <div class="card-body">
                 <h3 class="font"> {{ jumlahhpengunjung}} pengunjung</h3>
               </div>
             </div>
          </nuxt-link>
       </div>


       <div class="col-lg-6">
         <nuxt-link to="/buku">
           <div class="card bg-success rounded-5">
             <div class="card-body">
               <h4 class="font"> {{ jumlahbuku }} buku</h4>
             </div>
           </div>
         </nuxt-link>
       </div>
     </div>
     <Chart/>
  </div>
</template>


<script setup>
const supabase = useSupabaseClient();
const jumlahpengunjung = ref (0);
const jumlahbuku = ref (0);


async function ambiljumlahpengunjung() {
    const { data,error, count} = await supabase
    .from("pengunjung")
    .select("*", {count: 'exact'});
    if (count) jumlahpengunjung.value = count;
}
async function ambiljumlahbuku() {
    const { data,error, count} = await supabase
    .from("buku")
    .select("*", {count: 'exact'});
    if (count) jumlahbuku.value = count;
}


onMounted(() => {
    ambiljumlahpengunjung();
    ambiljumlahbuku();
})
</script>



<style scoped>
.card {
    height: 250px;
    box-shadow: 1px 1px 10px #424242;
}

.card.bg-pengunjung {
  background-image: url('../assets/bg-home-kunjungan.jpeg');
  background-repeat: no-repeat;
  background-position: center center;
  background-size: cover;
}

.card.bg-buku {
  background-image: url('../assets/bg-home-cari-buku.jpg');
  background-repeat: no-repeat;
  background-position: center center;
  background-size: cover;
}
h2{
  color: black;
  font: arial;
}
h1{
  color: black;
}

h3 {
  color: black;
  font-size: 55px;
  text-align: center;
  margin: 40px;
}

h4 {
  color: black;
  font-size: 65px;
  text-align: center;
  margin: 40px;
}

.card.bg-buku {
  margin-top: 3%;
}

.card.bg-success {
  margin-top: 3%;
}
.card.bg-warning {
  margin-top: 3%;
}
.card.bg-pengunjung {
  margin-top: 3%;
}


</style>