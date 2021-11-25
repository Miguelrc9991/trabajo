<template>
    <div class="container mt-5">
        <h1 class="display-1">Reproductor Video</h1>
        <div id="yt" align="center">
            
            <label for="idvideo">
                Pega aquí la ID del video que quieras mostrar:
            </label>
            <input type="text" id="idvideo" v-model="video" placeholder="Ejemplo: ZEFrbP7wYZU" value="ZEFrbP7wYZU" class="form-control input-lg">
          <hr>
          <iframe v-bind:src="url + video"
            v-bind:class="responsive"
             v-bind:width="ancho"  
              v-bind:height="alto"
               v-bind:frameborder="borde"
                v-bind:allowFullscreen="pcompleta"

            >
            </iframe>
            <p class="txt_videoactual">
                Se está reproduciendo : <kbd> {{this.video}}</kbd>
            </p>
        </div>
    </div>
</template>
<script>
export default {
  name: 'Galeria',
  props: {
    
  },
  data(){
      return{

            responsive: "embed-responsive-item",
      ancho: "100%",
      alto : "500",
      url: "https://www.youtube.com/embed/",
      video:"ZEFrbP7wYZU",
      borde : 0,
      pccompleta:null 
      }
    
  }
}
</script>
<style scoped>

</style>