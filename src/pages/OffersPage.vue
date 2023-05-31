<script>
export default {
  name: 'OffersPage',

}
</script>
<template>
    <div class="px-5" id="offers">
        <h3>OFFERTE SPECIALI</h3>
        <div class="d-flex justify-content-center mt-4">
            <div class="col-3">
                <img src="#" alt="#" class="placeholder image">
                    <div>
                        <span class="placeholder p-2">"Sconto"</span>
                        <span class="placeholder p-2">"Prezzo"</span>
                    </div>
            </div>
            <div class="col-3">
                <img src="#" alt="#" class="placeholder image">
                    <div>
                        <span class="placeholder p-2">"Sconto"</span>
                        <span class="placeholder p-2">"Prezzo"</span>
                    </div>
            </div>
            <div class="col-3 pb-4">
                <img src="#" alt="#" class="placeholder image">
                    <div>
                        <span class="placeholder p-2">"Sconto"</span>
                        <span class="placeholder p-2">"Prezzo"</span>
                    </div>
            </div>
        </div>


    </div>
</template>

<style scoped>
#offers{
    background-color:  #0f1014;
}
h3{
    color: white;
}
.placeholder{
    background-color: aqua;
    border: 1px solid;
}
.image{
    height: 200px;
    width: 100%;
}
</style>