 <template>
    <div class="container-fluid">
        <div class="row">
            <div class="col-lg-12">
                <h2 class="ext-center my-14">RIWAYAT KUNJUNGAN</h2>
                <nuxt-link to="../">
                    <button type="submit" class="btn btn-lg rounded-5 px-5 bg-black text-white" style="float: right; margin-bottom: 15px;">KEMBALI</button>
                </nuxt-link>
                <div class="my-3">
                    <form @submit.prevent="getpengunjung">
                    <input type="search" class="form-control form-control-lg rounded-5" placeholder="Filter...">   
                    </form>        
                </div>
                <div class="my-3 text-muted">menampilkan 1 dari 1</div>
                <table class="table">
                    <thead>
                        <tr>
                            <td>No</td>
                            <td>NAMA</td>
                            <td>KEANGGOTAAN</td>
                            <td>WAKTU</td>
                            <td>KEPERLUAN</td>
                        </tr>
                        <tr v-for="(visitor,id) in visitors" :key="i">
                            <td>{{ i+1 }}.</td>
                            <td>{{ visitor.nama }}</td>
                            <td>{{ visitor.keanggotaan.nama }}</td>
                            <td>{{ visitor.tanggal }},{{ visitor.waktu}}</td>
                            <td>{{ visitor.keperluan.nama }}</td>
                        </tr>
                    </thead>
                </table>
            </div>
        </div>
    </div>
 </template>

 <script setup>
 const supabase = useSupabaseClient()

 const visitors = ref([])

 const getPengunjung = async () => {
    const {data, error} = await supabase.from('pengunjung').select('*, keanggotaan(*), keperluan(*)')
    if(data) visitors.value = data
 }
 onMounted(()=> {
    getPengunjung()
 })
</script>

 <style scoped>
.ext-center.my-14{
    text-align: center;
}
</style>
