<template>

  <div id="home" :style="{ backgroundImage: `url(${elementos[currentSentence].img})`}">
    <div v-if="!clic">
        <Benving @comenzar="clic = true"></Benving>
    </div>
    <div v-else>
        <Botons @seg-sentence="clickSegSentence" @ant-sentence="clickAntSentence"></Botons>
        <Escena :frases="elementos" :activeSentence="currentSentence"></Escena>
    </div>
  </div>
</template>

<script>
import Escena from './Escena.vue'
import Botons from './Botons.vue'
import Benving from './Benving.vue'



export default {
  name: 'home',
  components: {Escena, Botons, Benving},
  data () {
    return {
      elementos: [
  {txt: "El nostre heroi estava surant per l'espai sideral quan a la llunyania va albirar una nau espacial", img:require("../assets/1.jpg")},

  {txt: "Sentia curiositat per l'interior de la nau i es va posar a inspeccionar-la. Va arribar a una sala amb dues portes.", img:require("../assets/2.jpg")},

  {txt: "L'heroi va decidir travessar la porta que el portava a casa", img:require("../assets/3.jpg")},

  {txt: "Mentrestant, altres heroes no van tenir tanta sort en la seva elecció ...", img:require("../assets/4.jpg")}
      ],
      currentSentence: 0,
      clic: false
    }
  },
  methods:{
        
        clickSegSentence(){
            if (this.currentSentence < this.elementos.length -1){
              this.currentSentence ++;
              // console.log(this.currentSentence);
            }
        },
        clickAntSentence(){
          if (this.currentSentence > 0){
            this.currentSentence--;
            // console.log(this.currentSentence);
            }
        }
  }

}

</script>

<style scoped>
    #home{
        height:100vh;
        background-repeat: no-repeat;
        background-size:cover;
        background-position:bottom;
    }
</style>