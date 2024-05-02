<template>
  <div class="container-fluid pb-5">
    <div class="row justify-content-center">
      <div class="col-lg-8">
        <h2 class="text-center my-4" style="color: aliceblue;">ISI DATA KUNJUNGAN</h2>
        <form>
          <div class="mb-3">
            <input type="text" class="form-control form-control-lg rounded-5 text-white" placeholder="NAMA..."  />
          </div>
          <div class="mb-3">
            <select class="form-control form-control-lg form-select rounded-5 text-white">
              <option value="">KEANGGOTAAN</option>
              <option value="siswa">SISWA</option>
              <option value="GURU">GURU</option>
              <option value="Staf">Staf</option>
              <option value="Umum">Umum</option>
            </select>
          </div>
          <div class="mb-3">
            <div class="row">
              <div class="col-md-4">
                <select class="form-control form-control-lg form-select rounded-5 text-white mb-2">
                  <option value="">KELAS</option>
                  <option value="X">X</option>
                  <option value="XI">XI</option>
                  <option value="XII">XII</option>
                </select>
              </div>
              <div class="col-md-4">
                <select class="form-control form-control-lg form-select rounded-5 text-white mb-2">
                  <option value="">JURUSAN</option>
                  <option value="PPLG">PPLG</option>
                  <option value="TJKT">TJKT</option>
                  <option value="TSM">TSM</option>
                  <option value="DKV">DKV</option>
                  <option value="TOI">TOI</option>
                </select>
              </div>
              <div class="col-md-4">
                <select class="form-control form-control-lg form-select rounded-5 text-white mb-2">
                  <option value="">TINGKAT</option>
                  <option value="1">1</option>
                  <option value="2">2</option>
                  <option value="3">3</option>
                  <option value="4">4</option>
                </select>
              </div>
            </div>
          </div>
          <div class="mb-4">
            <select class="form-control form-control-lg form-select rounded-5 text-white">
              <option value="">KEPERLUAN</option>
              <option value="baca">baca buku</option>
              <option value="pinjam">pinjam buku</option>
              <option value="kembalikan">kembalikan buku</option>
            </select>
          </div>
          <div class="col-12 d-flex justify-content-center">
            <button type="submit" class="btn btn-dark btn-lg rounded-5 text-white px-5">KIRIM</button>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Inknut+Antiqua:wght@300;400;500;600;700;800;900&display=swap");

form {
  font-family: "Inknut Antiqua", serif;
  font-weight: 500;
  font-style: normal;
}
.container-fluid {
  /* padding: 0;
    margin: 0; */
  background-color: #658694;
}
.form-control {
  /* padding: 0;
    margin: 0; */
  background-color: #89b6d6;
}
button {
  background-color: #55acec;
  align-items: center;
}
</style>
