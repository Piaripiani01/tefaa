<template>
    <div class="container-fluid">
        <div class="row py-5">
            <div class="col-lg-6">
            <nuxt-link to="/pengunjung/tambah">
                <div class="card bg-pengunjung rounded-5">
                    <div class="card-body">
                        <h2>pengunjung</h2>
                    </div>
                </div>
            </nuxt-link>
            </div>

            <div class="col-lg-6">
                <nuxt-link to="/buku">
                <div class="card bg-buku rounded-5">
                    <div class="card-body">
                        <h2>cari buku</h2>
                    </div>
                </div>
                </nuxt-link>
            </div>
        </div>
        <h2>Statistik</h2>
        <div class="row py-5">
            <nuxt-link to="/pengunjung/index"></nuxt-link>
            <div class="col-lg-6">
                <nuxt-link to="pengunjung/">
                <div class="card pengunjung rounded-5">
                    <div class="card-body">
                        <h1 class="mt-5">Riwayat pengunjung</h1>
                    </div>
                </div>
                </nuxt-link>
            </div>

            <div class="col-lg-6">
                <nuxt-link to="/buku">
                <div class="card buku rounded-5">
                    <div class="card-body">
                        <h1 class="mt-5">5 Buku</h1>
                    </div>
                </div>
                </nuxt-link>
            </div>
        </div>
    </div>
</template>

<style scoped>
.container-fluid {
    /* padding: 0;
    margin: 0; */
    background-color: #658694;
}
.card {
    height: 250px;
    box-shadow: 1px 1px 10px hsl(0, 0%, 100%)
}
.card.bg-pengunjung {
    background-image: url('../assets/img/pengunjung.jpeg');
    background-repeat: no-repeat;
    background-position: center center;
    background-size: cover;
}
.card.bg-buku {
    background: url('../assets/img/cari buku.jpg') no-repeat center center;
    background-size: cover;
}

.pengunjung {
    background-color: #89B6D6;
}
.buku {
    background-color: #89B6D6;
}

h2{
    color: white;
    font-family: "Irish Grover", system-ui;
}
</style>
