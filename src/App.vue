<script setup>
import { perguntas } from './assets/db.vue'
</script>

<template>
  <div id="navegador">
    <nav>
      <div><img src="favicon.png" alt="" width="50px" /></div>
      <div>
        <h2>Inicio</h2>
      </div>
      <div>
        <h2>Quiz Biologia</h2>
      </div>
      <div>
        <h2>Pontuação:</h2>
      </div>
      <div>
        <h2>User</h2>
      </div>
    </nav>
  </div>
  <div id="topo">
    <div id="area-perguntas">
      <div id="pergunta" v-for="(pergunta, index) in perguntas" :key="pergunta.name">
        {{ pergunta.titulo }}
        <div id="pergunta" v-for="(resposta, index) in pergunta.repostas" :key="resposta.name">
          {{ resposta.letra }} - {{ resposta.texto }}
        </div>
      </div>
     
      <div><button>Enviar</button></div>
    </div>
  </div>
</template>

<style scoped>
nav {
  background-color: #04acd6;
}
nav > div > h2 {
  text-align: center;
  color: rgb(0, 0, 0);
}
button {
  border-radius: 20px;
  background-color: #04acd6;
  border-color: rgb(255, 255, 255);
  color: white;
  font-size: 25px;
}
body {
  background-color: #10eedf5d;
}
#area-perguntas {
  border-color: #04acd6;
  border-style: solid;
  background-color: #04acd694;
  margin: 20px;
  border-radius: 10px;
  width: 800px;
  font-size: 25px;
}
#pergunta {
  color: rgb(0, 0, 0);
  margin: 10px;
  text-align: left;
}
#alternativas {
  color: rgb(0, 0, 0);
  margin: 10px;
  text-align: left;
}
nav {
  display: flex;
  gap: 10%;
  align-items: center;
}
nav > div > img {
  margin-left: 10px;
}

#topo {
  text-align: -webkit-center;
}
</style>
