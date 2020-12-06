<template>
  <div id="app">
    <servicios class="servicios"></servicios>
    <seccion-api>
      <div class="container-fluid">
        </div>

    </seccion-api>

    <div class="container-fluid">
      <div class="row justify-content-center mb-5">
        <div class="col mt-5" v-for="(item, index) of team" :key="index">
          <team-card v-bind:member="item"></team-card>
        </div>
      </div>
    </div>

    <footer-inicial></footer-inicial>
  </div>
</template>

<script>
import FooterInicial from "./components/FooterInicial.vue";
import TeamCard from "./components/TeamCard.vue";
import SeccionApi from "./components/SeccionApi.vue";
import servicios from "./components/servicios.vue";

export default {
  name: "App",
  components: {
    FooterInicial,
    TeamCard,
    SeccionApi,
    servicios,
  },
  data() {
    return {
      team: [
        {
          codigo: 1,
          Nombre: "Richard Antohny Gomez Arcos",
          descripcion: "Estudiante de Ingenieria Mecanica.",
          rol: "Desarrollador FullStack",
          imagen:
            "https://scontent-bog1-1.xx.fbcdn.net/v/t1.0-9/11160673_10202589651340863_5981651415561644205_n.jpg?_nc_cat=105&ccb=2&_nc_sid=174925&_nc_ohc=rdhvXDyu9bQAX9uuJlp&_nc_ht=scontent-bog1-1.xx&oh=166218fb9b5b7603b9b9f87d73c76ba0&oe=5FF24165",
        },
        {
          codigo: 2,
          Nombre: "RAQUEL SOFIA SALAZAR CASTRO",
          descripcion: "Estudiante de Ingenieria Mecatronica.",
          rol: "Desarrollador FullStack",
          imagen:
            "https://scontent.fbog3-1.fna.fbcdn.net/v/t1.0-9/75266189_10220724779732124_3551362127526625280_n.jpg?_nc_cat=103&ccb=2&_nc_sid=09cbfe&_nc_ohc=EHCmTMUVPjYAX-hM_IG&_nc_ht=scontent.fbog3-1.fna&oh=6b96184e96b3be0199f2b147324cf6a9&oe=5FF11785",
        },
        {
          codigo: 3,
          Nombre: "PEDRO GONZÁLEZ HENAO",
          descripcion: "Estudiante de Matematica Pura.",
          rol: "Desarrollador Backend",
          imagen:
            "https://scontent-bog1-1.xx.fbcdn.net/v/t1.0-9/22141316_10213487895087391_1010285333396491664_n.jpg?_nc_cat=107&ccb=2&_nc_sid=09cbfe&_nc_ohc=acdsP7hXyyAAX_PfErW&_nc_ht=scontent-bog1-1.xx&oh=c98c8c0c7a8c9f6bd5c2e77d9024484d&oe=5FF33536",
        },
        {
          codigo: 4,
          Nombre: "JUAN DAVID LAISECA MEDINA",
          descripcion: "Estudiante de Ingenieria de Software.",
          rol: "Desarrollador Frontend",
          imagen: "https://placeimg.com/192/192/people",
        },
      ],
    };
  },
};
</script>
