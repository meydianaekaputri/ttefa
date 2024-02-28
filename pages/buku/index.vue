<template>
    <div class="container-fluid">
        <div class="row">
            <div class="col-lg-12">
                <h2 class="text-center my-4">BUKU</h2>
                <nuxt-link to="../">
                    <button type="submit" class="btn btn-lg rounded-5 px-5 bg-black text-white" style="floatt: right; margin-bottom: 15px;">KEMBALI</button>
                </nuxt-link>
                <div class="my-3">
                    <input type="search" class="form-control rounded-5" placeholder="Mau baca apa hari ini?">
                </div>
            <div class="my-3 text-muted">menampilkan 3 dari 3</div>
                <div class="row">
                    <div class="col-lg-2">
                        <div class="card mb-3">
                            <nuxt-link to="/buku/des">
                            <div class="card-body">
                                <img src="~/assets/fantasteenrevenge.jpg" class="cover" alt="cover 1">
                            </div>
                        </nuxt-link>
                        </div>
                    </div>   
                    <div class="col-lg-2">
                        <div class="card mb-3">
                            <div class="card-body">
                                <img src="~/assets/fantasteenrevenge.jpg" class="cover" alt="cover 1">
                            </div>
                        </div>
                    </div>   
                    <div class="col-lg-2">
                        <div class="card mb-3">
                            <div class="card-body">
                                <img src="~/assets/fantasteenrevenge.jpg" class="cover" alt="cover 1" >
                            </div>   
                       </div>
                   </div>   
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.card-body {
    width: 276px;
    height: 25em;
    
}
.cover {
    width: 276px;
    height: 25em; 
}
.card.mb-3{
    margin-top: 20px;
    width: 276px;
    height: 25em;
}


</style>