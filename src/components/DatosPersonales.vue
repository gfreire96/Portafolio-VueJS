<script setup>
const nombre = "Gabriel Freire Parola"
const  bio = "Soy programador y estudiante de física en UNSL y programación en UTN San Rafael. Con un perfil generalista y enfoque en backend, busco integrar conocimientos técnicos para crear soluciones innovadoras."
const residencia = "Mendoza, Argentina"
const telefono = "+54 9 2625-660775"
const redesSociales = [
      {id: 1, name: "github" , src: "src/assets/github_icon.png" , url: ""},
      {id: 2, name: "x" , src: "src/assets/x_icon.png" , url: ""},
      {id: 3, name: "linkedin", src: "src/assets/linkedin_icon.svg", url: ""},
      {id: 3, name: "instagram", src: "src/assets/instagram_icon.svg", url: ""}
      ] 
</script>

<template>
<section class="datos-personales">
  <div class="card">
    <h2>{{ nombre }}</h2>
    <p>{{ bio }}</p>
    <ul class="container-lista"> <!-- Cambia aquí para usar un ul -->
      <li v-for="red in redesSociales" :key="red.id">
        <a :href="red.url">
          <img class="icon-redsocial" :src="red.src" width="24rem" :alt="red.name">
        </a>
      </li>
    </ul>
    <h3>{{ telefono }}</h3>
    <h4> {{ residencia }}</h4>
  </div>
</section>

</template>

<style scoped>
.DatosPersonales {
      display: flex;
      font-size: large;
      text-align: justify;
      line-height: 1.6;
    }
    
.img-perfil{
      margin: 1rem;
      border-radius: 10%;
    }

.container-lista {
  display: flex;           /* Utiliza flexbox para alinear los ítems */
  justify-content: left; /* Centra los ítems horizontalmente */
  list-style: none;       /* Quita los puntos de la lista */
  padding: 0;             /* Elimina el padding por defecto */
  margin: 0;              /* Elimina el margen por defecto */
}

.icon-redsocial {
  margin: 0 5px;         /* Espaciado entre los iconos, puedes ajustar el valor */
}


</style>