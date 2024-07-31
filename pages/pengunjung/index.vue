<template>
    <div class="container-fluid">
        <div class="row content">
            <div class="col-lg-12">       
                <nuxt-link to="/"></nuxt-link>
                <h2 class="text-center my-4">RIWAYAT PENGUNJUNG</h2>
                <nuxt-link to="/">
                        <i class="bi bi-caret-left-fill fs-1"></i>
                    </nuxt-link>
                <div class="row my-3 d-flex justify-content-center">
                    <input v-model=keyword type="search" class="col-lg-10 form-control- form-control-lg rounded-5 " placeholder="Search..." style="background-color: #B2CDE1;">
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
                        <tr v-for="(visitor,i) in pengunjungFiltered" :key="i">
                            <td>{{ i+1 }}.</td>
                            <td>{{ visitor.nama }}</td>
                            <td>{{ visitor.keanggotaan.nama }}</td>
                            <td>{{ visitor.tanggal }}, {{ visitor.waktu }}</td>
                            <td>{{ visitor.keperluan.nama }}</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>
    </div>
</template>

<script setup>
const supabase = useSupabaseClient()

const visitors = ref([])
const keyword = ref('')

const getPengunjung = async () => {
    const { data, error } = await supabase.from('pengunjung').select(`*, keanggotaan(*), keperluan(*)`)
    if(data) visitors.value = data
}
const pengunjungFiltered = computed(() =>{
    return visitors.value.filter((b) =>{
        return (
            b.nama?.toLowerCase().includes(keyword.value?.toLowerCase()) ||
            b.keanggotaan.nama?.toLowerCase().includes(keyword.value?.toLowerCase())
        )
    } )
})
onMounted(() =>{
    getPengunjung()
})
</script>


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

.bi-caret-left-fill {
    margin-left: 20px;
}
</style>