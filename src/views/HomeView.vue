<script setup lang="ts">
import CardComponent from "@/components/CardComponent.vue";
function openLink(url: string) {
  window.open(url, "_blank");
}
</script>

<template>
  <div class="home">
    <div class="home__header">
      <span>Puntaserver</span>
    </div>
    <div class="home__body">
      <h1>Bienvenido a Puntaserver!</h1>
      <p>
        Puntaserver es un servidor hecho con ❤️ en la Punta. Por favor, evita
        sobrecargarlo con peticiones innecesarias. Si algo no va bien envíame un
        correo a "admin@puntaserver.com"
      </p>
    </div>
    <div class="home__section">
      <h2>Servicios (desplegados en contenedores LXD)</h2>
      <div class="home__section__grid">
        <CardComponent
          title="Coolify ❤"
          description="Despliegue automático para mis apps"
          @click="openLink('https://coolify.puntaserver.com')"
        ></CardComponent>
        <CardComponent
          title="Mattermost"
          description="Control de progreso de tareas"
          @click="openLink('https://mattermost.puntaserver.com')"
        ></CardComponent>
        <CardComponent
          title="PGAdmin"
          description="Panel para bases de datos PostgreSQL"
          @click="openLink('https://pgadmin.puntaserver.com/pgadmin4')"
        ></CardComponent>
        <CardComponent
          title="Passbolt"
          description="Administrador de contraseñas"
          @click="openLink('https://passbolt.puntaserver.com')"
        ></CardComponent>
      </div>
    </div>
    <div class="home__section">
      <h2>Aplicaciones (desplegadas con Coolify y Docker)</h2>
      <div class="home__section__grid">
        <CardComponent
          title="ISS"
          description="Aplicacion desarrollada (en compañia de mis compis de Mdona) para Space Apps Challenge 2022 organizado por NASA"
          @click="openLink('https://iss.puntaserver.com')"
        ></CardComponent>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.home {
  font-family: roboto-flex, serif;
  &__header {
    padding: 12px;
  }
  &__body,
  &__section {
    padding: 40px;
  }
  &__section {
    &__grid {
      display: flex;
      flex-wrap: wrap;
      row-gap: 45px;
      column-gap: 45px;
    }
  }
}
</style>
