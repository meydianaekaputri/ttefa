<template>
    <div class="container-fluid">
        <div class="row">
            <div class="col-lg-12">
                <div class="row">
                    <div class="col-lg-2">
                        <div class="card mb-3">
                            <div class="card-body">
                                <img src="~/assets/fantasteenrevenge.jpg" class="cover" alt="cover 1">

                            </div>
                        </div>
                    </div>
                    <div class="col-lg-6">
                        <h1>Fantasteen Revenge</h1>
                        <p>Pengarang               : </p>
                        <p>Negara                  : </p>
                        <p>Bahasa                  : Indonesia</p>
                        <p>Penerbit                : </p>
                        <p>Tahun Terbit            : 2018</p>
                        <p>Halaman                 : </p>
                        <p>Deskripsi               : Keeyara kehilangan kesadaran sesaat setelah secara tidak sengaja bertemu Dewi Kematian. Setelah tersadar ada memori yang hilang dalam ingatannya, dia tidak mengingat Maddy, sahabatnya. Dia kembali ke masa lalu saat kedua orangtuanya masih ada. Di hari kematian orangtuanya, Keeyara sudah mempersiapkan diri, namun ternyata dia salah. Orangtuanya masih hidup, dan dia mulai curiga. Ada yang tidak beres dengan jalan hidupnya. Akhirnya dia tersadar, ternyata selama ini ada rencana jahat yang telah disiapkan untuk melenyapkan keluarga Keeyara. Mampukah Keeyara menyelesaikan misteri yang terjadi dalam hidupnya?</p>
                    </div>
                    <nuxt-link to="../pengunjung">
                            <button type="submit" class="btn btn-lg rounded-5 px-5 bg-black text-white">PINJAM</button>
                        </nuxt-link>
                </div>
            </div>
        </div>
    </div>
</template>
 
<style scoped>

.cover1{
    height: 70px;
    width: 320px;

}

.card.mb-3{
    margin-top: 30px;
    width: 320px;
    height: 70px;
    margin-left: 20px;
}

h1 {
    margin-top: 100px;
    margin-left: 180px;
    margin-bottom: 1px;
}

p {

    margin-left: 180px;
    margin-bottom: 7px;
}
img{
     width: 276px;
    height: 25em;
}
</style>