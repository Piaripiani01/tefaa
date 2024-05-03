<template>
  <div class="content">
    <div class="container py-5">
      <div class="row mb-5">
        <div class="col">
          <div class="card">
            <h2 class="text-center">RINCIAN BUKU</h2>
            <div class="container mt-5">
              <div class="row">
                <div class="col-3 p-5">
                  <img class="img-fluid" src="@/assets/img/Y.jpg" alt="" style="width: 250px;">
                </div>
                <div class="col-8">
                  <h4>Judul buku:</h4>
                  <h4>Penulis: Dwi wulan sari</h4>
                  <h4>Tahun terbit: 2020</h4>
                  <h4>Penerbit: Bhuana ilmu populer</h4>
                  <h4>Kategori: novel</h4>
                  <h4>Rak:10</h4>
                  <h4>Deskripsi: Mencintai diam diam, itu yang di rasakan aura terhadap arya, namun hatinya hancur
                    ketika ternyata arya menikah dengan wanita lain. aura memutuskan untuk menjauh dari arya menghilang
                    dan tinggal di rumah neneknya untuk menata kembali hatinya yang hancur.</h4>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="row justipy-content-end">
      <div class="text-end">
        <nuxt-link to="/buku">
          <button type="submit" class="btn justipy-content-center btn-light btn-lg rounded-3 px-5 mb-3 me-5" style="background-color: #5B92BA;">BACK</button>
        </nuxt-link>
      </div>
    </div>
  </div>
</template>
<script setup>
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inknut+Antiqua:wght@300;400;500;600;700;800;900&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Inknut+Antiqua:wght@300;400;500;600;700;800;900&family=Kavoon&display=swap');
.content {
  background-color: #8FD6F4;
}

.card {
  background-color: #5B92BA;
  border-radius: 25px;
}

h4{
  color:aliceblue;
  font-family: "Kavoon", serif;

}

h2{
  color:aliceblue;
  font-family: "Inknut Antiqua", serif;
}

.img-fluid{
  border-radius: 20px;
}
</style>