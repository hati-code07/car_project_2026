<template>
<v-app>
<v-navigation-drawer app v-model="drawer">

    <!-- Первый блок - Заголовок -->
    <v-list-item>
      <v-list-item-content>
        <v-list-item-title class="title">
          КИПУ
        </v-list-item-title>
        <v-list-item-subtitle>
          Учебный проект
        </v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item>

    <!-- Разделитель -->
    <v-divider></v-divider>

    <!-- Навигационный список -->
    <v-list dense>
      <!-- Первый пункт меню -->
      <v-list-item>
        <template v-slot:prepend>
          <v-icon icon="mdi-cake-variant"></v-icon>
        </template>
        <v-list-item-title>Link One</v-list-item-title>
      </v-list-item>

      <!-- Второй пункт меню -->
      <v-list-item>
        <template v-slot:prepend>
          <v-icon icon="mdi-home"></v-icon>
        </template>
        <v-list-item-title>Главная</v-list-item-title>
      </v-list-item>

      <!-- Третий пункт меню -->
      <v-list-item>
        <template v-slot:prepend>
          <v-icon icon="mdi-account"></v-icon>
        </template>
        <v-list-item-title>Профиль</v-list-item-title>
      </v-list-item>

      <!-- Добавьте свои пункты меню -->
    </v-list>
</v-navigation-drawer>
<v-app-bar app dark color="primary">
<v-app-bar-nav-icon  @click="drawer = !drawer"></v-app-bar-nav-icon>
<v-spacer></v-spacer>
<v-toolbar-items class="hidden-sm-and-down">
<v-btn>
    <v-icon
    start
    icon="mdi-cake-variant"
    ></v-icon>
    Link One
</v-btn>
<v-btn>Link Two</v-btn>
<v-btn>Link Three</v-btn>
</v-toolbar-items>
</v-app-bar>
<v-main>
</v-main>
</v-app>
</template>


<script>
export default {
 data() {
    return {
      drawer: false,
    }
  }

}
</script>
