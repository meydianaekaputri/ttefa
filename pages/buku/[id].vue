<template>
    <div>
      <h2 class="text-start my-4">{{ buku.judul }}</h2>
      <div class="row">
        <div class="col-md-3">
          <div class="card">
            <div class="card-body">
              <span v-if="buku.cover"><img :src="buku.cover" :alt="buku.judul" class="cover"></span>
              <span v-else>
                <img
                  src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/3f/Placeholder_view_vector.svg/681px-Placeholder_view_vector.svg.png"
                  :alt="buku.judul"
                  class="cover"></span>
            </div>
          </div>
        </div>
        <div class="col-md-6">
          <ul class="list-group list-group-flush">
            <li class="list-group-item">penulis : {{ buku.penulis }}</li>
            <li class="list-group-item">tahun terbit : {{ buku.tahun_terbit }}</li>
            <li class="list-group-item">penerbit : {{ buku.penerbit }}</li>
            <li class="list-group-item">deskripsi : {{ buku.deskripsi }}</li>
          </ul>
        </div>
      </div>
      <NuxtLink to="/buku">
        <button type="submit" class="btn btn-lg rounded-5 px-5">Kembali</button>
      </NuxtLink>
    </div>
  </template>
  
  <script setup>
  const supabase = useSupabaseClient()
  const route = useRoute()
  const buku = ref([])
  
  const getBukuById = async () => {
    const { data, error } = await supabase.from('buku').select(`*, kategori(*)`)
      .eq('id', route.params.id)
    if (data) buku.value = data[0]
  }
  
  onMounted(() => {
    getBukuById()
  })
  </script>
  
  <style scoped>
  .btn {
    background-color: burlywood;
    position: fixed;
    bottom: 30px;
    right: 30px;
  }
  
  .cover {
    width: 100%;
  }
  </style>

