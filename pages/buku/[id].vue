<template>
    <div class="content">
      <div class="container py-5">
        <div class="row mb-5">
          <div class="col">
            <div class="card">
              <h2 class="text-center">RINCIAN BUKU</h2>
              <div class="container mt-5">
                <div class="row g-3 justify-content-center">
                  <div class="col-lg-3 col-8">
                    <img class="img-fluid" :src="buku?.cover" alt="">
                  </div>
                  <div class="col-12">
                    <h4>Judul : {{ buku?.judul }}</h4>
                    <h4>Penulis: {{ buku?.penulis }}</h4>
                    <h4>Tahun_terbit: {{ buku?.tahun_terbit }}</h4>
                    <h4>penerbit: {{ buku?.penerbit }}</h4>
                    <h4>Kategori: {{ buku?.kategori_buku?.nama }}</h4>
                    <h4>Rak: {{buku?.rak}}</h4>
                    <p>Deskripsi: {{ buku?.deskripsi }}</p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="row justipy-content-end">
        <div class="text-end">
          <nuxt-link to="/buku" >
            <button type="submit" class="btn justipy-content-center btn-light btn-lg rounded-3 px-5 mb-3 me-5" style="background-color: #5B92BA;">BACK</button>
          </nuxt-link>
        </div>
      </div>
    </div>
</template>

<script setup>
const supabase = useSupabaseClient()
const route = useRoute()
const buku = ref()

const getBookById = async () => {
    const { data, error } = await supabase.from('buku').select(`*, kategori_buku(*)`)
    .eq('id', route.params.id)
    .maybeSingle()
    if(data) buku.value = data
    // data.forEach(book => {
    //         const { data: url } = supabase.storage.from('cover').getPublicUrl(book.cover)
    //         if (url) {
    //             book.cover = url.publicUrl
    //         }
    //     })
}

onMounted(() => {
    getBookById()
})
</script>
  
  <style scoped>
  .content {
    background-color: #8FD6F4;
  }
  
  .card {
    background-color: #5B92BA;
    border-radius: 25px;
  }
  
  h4, h2, p{
    color:aliceblue;
  }
  
  .img-fluid{
    border-radius: 20px;
  }
  </style>

