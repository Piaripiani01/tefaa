<template>
    <div class="container-fluid">
        <div class="row py-5">
            <div class="col-lg-6">
                <nuxt-link to="/pengunjung/tambah">
                    <div class="card bg-pengunjung rounded-5">
                        <div class="card-body">
                            <h3 class="text-center" style="margin-top: 80px;">pengunjung</h3>
                        </div>
                    </div>
                </nuxt-link>
            </div>

            <div class="col-lg-6">
                <nuxt-link to="/buku">
                    <div class="card bg-buku rounded-5">
                        <div class="card-body">
                            <h3 class="text-center" style="margin-top: 80px;">cari buku</h3>
                        </div>
                    </div>
                </nuxt-link>
            </div>
        </div>
        <h2>Statistik</h2>
        <div class="row py-5">
            <nuxt-link to="/pengunjung"></nuxt-link>
            <div class="col-lg-6">
                <nuxt-link to="pengunjung/">
                    <div class="card pengunjung rounded-5">
                        <div class="card-body">
                            <h1 class="text-center" style="margin-top: 80px;">{{ visitors.length }} pengunjung</h1>
                        </div>
                    </div>
                </nuxt-link>
            </div>

            <div class="col-lg-6">
                <nuxt-link to="/buku">
                    <div class="card buku rounded-5">
                        <div class="card-body">
                            <h1 class="text-center" style="margin-top: 80px;">{{ books.length }} Buku</h1>
                        </div>
                    </div>
                </nuxt-link>
            </div>
        </div>
    </div>
</template>

<script setup>
const supabase = useSupabaseClient()

const visitors = ref([])

const books = ref([])

const getBook = async () => {
    const { data, error } = await supabase.from('buku').select(`*,kategori(*)`)
    if(data) books.value = data
}

const getPengunjung = async () => {
    const { data, error } = await supabase.from('pengunjung').select(`*, keanggotaan(*), keperluan(*)`)
    if(data) visitors.value = data
}
onMounted(() =>{
    getPengunjung()
    getBook()
})
</script>

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
    background: url('../assets/img/caribuku.jpg') no-repeat center center;
    background-size: cover;
}

.pengunjung {
    background-color: #89B6D6;
}

.buku {
    background-color: #89B6D6;
}

h2 {
    color: white;
    font-family: "Irish Grover", system-ui;
}

h3 {
    color:white;
}

h1 {
    color:black;
}
</style>
