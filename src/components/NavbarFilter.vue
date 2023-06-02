<template>
    <nav class="filter-nav">
        <button @click="filterGuncelle('hepsi')" :class="{active:aktifSekme==='hepsi'}">Bütün Yapılacaklar</button>    
        <button @click="filterGuncelle('tamamlandi')" :class="{active:aktifSekme==='tamamlandi'}">Yapılanlar</button>    
        <button @click="filterGuncelle('yapiliyor')" :class="{active:aktifSekme==='yapiliyor'}">Devam Edenler</button>    
    </nav>
</template>

<script>
export default {
    props: ['aktifSekme'],
    methods: {
        filterGuncelle(durum) {
            this.$emit('filterDurum', durum)
        }
    }
}

</script>

<style>
.filter-nav button{
    background: none;
    border: none;
    color: #0b0b0b;
    outline: none;
    font-size: 12px;
    text-transform: uppercase;
    margin-right: 10px;
    letter-spacing: 1px;
    font-weight: bold;
    cursor: pointer;
}
.filter-nav button.active{
    color: #f91111;
}
</style>