<template>
<div class="row justify-around">
  <div class="col-3" v-for="audio in audios" :key="audio">
    <button   @click="play(audio.som)" class="key_board">
    {{audio.name}}
  </button>
  </div>


</div>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'KeyBoard',
  methods:{
 play(sound) {
  var audio = new Audio(`../audios/${sound}.mp3`);
  audio.play();
}
  },
  data() {
    return {
      audios: [
        {
      name:"ele gosta",
      som: 'ele_gosta',
    },
    {
      name:"abuuura",
      som: 'aburaburaa',
    },
    {
      name:"ai gostei",
      som: 'ai_gostei',
    },
    {
      name:"ai mamãe",
      som: 'ai_mamae',
    },
    {
      name:"meu deus",
      som: 'ai_meu_deus',
    },
     {
      name:"ata",
      som: 'ata',
    },
     {
      name:"ai",
      som: 'ai',
    },
     {
      name:"aiaiaai",
      som: 'aiaiaaaaiai',
    },
     {
      name:"potencia",
      som: 'aooowpotencia',
    },
     {
      name:"atumalaca",
      som: 'atumalaca',
    },
     {
      name:"cavalo",
      som: 'cavalo',
    },
     {
      name:"chega",
      som: 'chega',
    },
     {
      name:"dança gatinho",
      som: 'danca_gatinho',
    },
     {
      name:"demaais",
      som: 'demaaais',
    },
     {
      name:"é brincadeira",
      som: 'e_brincadeira',
    },
     {
      name:"elastico",
      som: 'elastico',
    },
     {
      name:"error",
      som: 'erro',
    },
     {
      name:"fico bão não",
      som: 'fico_bao_nao',
    },
     {
      name:"galinha",
      som: 'galinha',
    },
     {
      name:"iiihaaa",
      som: 'iiiihaa',
    },
     {
      name:"sem graça",
      som: 'mas_que_cara_sem',
    },
     {
      name:"que papelão",
      som: 'que_papelao',
    },
     {
      name:"soco",
      som: 'soco',
    },
     {
      name:"muah",
      som: 'muah',
    },
     {
      name:"não",
      som: 'não',
    },
     {
      name:"okay okay",
      som: 'okok',
    },
     {
      name:"pare",
      som: 'pare',
    },
     {
      name:"que isso meu filho",
      som: 'que_isso_meu_filho_calma',
    },
     {
      name:"então ta bom",
      som: 'tao_ta_bom',
    },
     {
      name:"tome",
      som: 'tome',
    },
     {
      name:"tum",
      som: 'tum',
    },
     {
      name:"uui",
      som: 'uuui',
    },
     {
      name:"vamo dança",
      som: 'vamo_danca',
    },
     {
      name:"xii",
      som: 'xiiii',
    },
     {
      name:"cavalo 2",
      som: 'cavalo2',
    },
     {
      name:"cavalo 3",
      som: 'cavalo3',
    },

      ]
    }
  }
})
</script>
<style scoped>
 .key_board {
  text-transform: capitalize;
  margin: 10px;
  border: none;
  outline: none;
  color: rgb(0, 0, 0);
  background: #f5f5f5;
  cursor: pointer;
  position: relative;
  z-index: 0;
  height: 70px;
  width: 80px;
  border-radius: 40px;
}
.key_board:before {
  content: "";
  background: linear-gradient(
    45deg,
    #ff0000,
    #ff7300,
    #fffb00,
    #48ff00,
    #00ffd5,
    #002bff,
    #7a00ff,
    #ff00c8,
    #ff0000
  );
  position: absolute;
  top: -2px;
  left: -2px;
  background-size: 400%;
  z-index: -1;
  filter: blur(5px);
  -webkit-filter: blur(5px);
  width: calc(100% + 4px);
  height: calc(100% + 4px);
  animation: glowing-key_board 35s linear infinite;
  transition: opacity 0.3s ease-in-out;
  border-radius: 20px;
}

@keyframes glowing-key_board {
  0% {
    background-position: 0 0;
  }
  50% {
    background-position: 400% 0;
  }
  100% {
    background-position: 0 0;
  }
}

.key_board:after {
  z-index: -1;
  content: "";
  position: absolute;
  width: 100%;
  height: 100%;
  background: #ffffff;
  left: 0;
  top: 0;
  border-radius: 24px;
}

</style>
