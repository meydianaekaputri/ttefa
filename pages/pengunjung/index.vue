 <template>
    <div class="container-fluid">
        <div class="row">
            <div class="col-lg-12">
                <h2 class="ext-center my-14">RIWAYAT KUNJUNGAN</h2>
                <nuxt-link to="../">
                    <button type="submit" class="btn btn-lg rounded-5 px-5 bg-black text-white" style="floatt: right; margin-bottom: 15px;">KEMBALI</button>
                </nuxt-link>
                <div class="my-3">
                    <input type="search" class="form-control form-control-lg rounded-5" placeholder="Filter...">           
                </div>
                <div class="my-3 text-muted">menampilkan 1 dari 1</div>
                <table class="table">
                    <thead>
                        <tr>
                            <td>#</td>
                            <td>NAMA</td>
                            <td>KEANGGOTAAN</td>
                            <td>WAKTU</td>
                            <td>KEPERLUAN</td>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>1.</td>
                            <td>Meydiana</td>
                            <td>Siswa</td>
                            <td>26 Februari 2024, 23.31.00</td>
                            <td>Baca</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>
    </div>
 </template>
 <style scoped>
.ext-center.my-14{
    text-align: center;
}
</style>