<template>
    <div class="container-fluid">
        <div class="row content">
            <div class="col-lg-12">
                <nuxt-link to="/index"></nuxt-link>
                <h2 class="text-center my-4">RIWAYAT PENGUNJUNG</h2>
                <div class="row my-3 d-flex justify-content-center">
                    <input type="search" class="col-lg-10 form-control- form-control-lg rounded-5 "placeholder="Search..." style="background-color: #B2CDE1;">
                </div>
                <div class="my-3 text-muted"></div>
                <table class="table table-bordered">
                    <thead>
                        <tr>
                            <td>NO</td>
                            <td>NAMA</td>
                            <td>KATEGORI</td>
                            <td>WAKTU/TANGGAL</td>
                            <td>KEPERLUAN</td>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>1.</td>
                            <td>Pia ripiani</td>
                            <td>siswa</td>
                            <td>08.00/10-04-2024</td>
                            <td>Membaca</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>
    </div>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Irish+Grover&display=swap');
.content{
    background-color: #658694;
}
td {
    color: white;
    border: 1px solid #fff;
    background-color: rgba(255, 255, 255, 0);
}

h2{
    color: white;
    font-family: "Irish Grover", system-ui;
}
</style>