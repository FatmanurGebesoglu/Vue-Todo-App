<template>
    <div class="yapilacak">
        <div class="baslik">
            <h3 @click="detayGoster= !detayGoster">{{ yapilacak.baslik }}</h3>
            <div class="icon">
                <span class="material-icons">edit</span>
                <span class="material-icons">delete</span>
                <span class="material-icons">done</span>
            </div>
        </div>
        <div v-if="detayGoster" class="detay">
            <p>{{ yapilacak.icerik }}</p>
        </div>
    </div>
</template>

<script>
    export default {
        props: ['yapilacak'],
        data(){
            return {
                detayGoster: false
            }
        },

    }
</script>

<style>
    .yapilacak{
        margin: 20px auto;
        background-color: #F7EDDB;
        padding: 10px 20px;
        border-radius: 15px;
        border: 3px solid #967E76;
        color: #1c1c1b;
    }
    .yapilacak:hover{
        box-shadow: 8px 10px 10px #967E76;
    }
    h3{
        cursor: pointer;
    }
    .baslik{
        display: flex;
        justify-content: space-between;
        align-content: center;
    }
    .material-icons{
        font-size: 25px;
        margin-left: 10px;
        color: #83764F;
        cursor: pointer;
    }
    .material-icons:hover{
        color: #F97B22;
        font-size: 30px;
    }
</style>