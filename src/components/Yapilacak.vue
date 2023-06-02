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
        background-color: #696a6d;
        padding: 10px 20px;
        border-radius: 15px;
        border: 3px solid #e9ace1;
        color: #f7f1e3;
    }
    .yapilacak:hover{
        box-shadow: 8px 10px 10px rgba(2,2,2,0.3);
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
        color: #bfc6d3;
        cursor: pointer;
    }
    .material-icons:hover{
        color: #ea2577;
        font-size: 30px;
    }
</style>