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
      <h2>Servicios (desplegados en contenedores LXD y Docker)</h2>
      <div class="home__section__grid">
        <CardComponent
          title="Coolify ❤"
          description="Despliegue automático para mis apps"
          @click="openLink('https://coolify.puntaserver.com')"
        ></CardComponent>
        <CardComponent
          title="PGAdmin"
          description="Panel para bases de datos PostgreSQL"
          @click="openLink('https://pgadmin.puntaserver.com/pgadmin4')"
        ></CardComponent>
        <CardComponent
          title="Minio"
          description="Panel para S3 Storage"
          @click="openLink('https://minio.puntaserver.com')"
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
        <CardComponent
          title="EMT - Front"
          description="Como sería la aplicación de EMT Ticket si fuera una PWA"
          @click="openLink('https://emt.puntaserver.com')"
        ></CardComponent>
        <CardComponent
          title="EMT - Back"
          description="Backend para EMT Ticker, manejo de usuarios, tickets, permisos y más!"
          @click="openLink('https://emt-back.puntaserver.com')"
        ></CardComponent>
        <CardComponent
          title="Mockos - Front (en desarrollo)"
          description="Frontend para mockos, creación de mocks con proyectos, regex y más"
          @click="openLink('https://mockos.puntaserver.com')"
        ></CardComponent>
        <CardComponent
          title="Mockos - Back (en desarrollo)"
          description="Backend para mockos, creación de mocks con proyectos, regex y más"
          @click="openLink('https://mockos-back.puntaserver.com')"
        ></CardComponent>
        <CardComponent
          title="Churritos - Front"
          description="Frontend para churritos, encuestas para saber si pillamos bueñuelos o churros en la ofi"
          @click="openLink('https://churritos.puntaserver.com')"
        ></CardComponent>
        <CardComponent
          title="Churritos - Back"
          description="Backend para churritos, encuestas para saber si pillamos bueñuelos o churros en la ofi"
          @click="openLink('https://churritos-back.puntaserver.com')"
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
