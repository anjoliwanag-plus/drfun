<template>
    <v-app-bar color="primary" density="compact">
        <template v-slot:prepend>
            <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
            <v-toolbar-title>Dr. Fun</v-toolbar-title>

        </template>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" temporary>
        <v-list-item prepend-avatar="https://randomuser.me/api/portraits/men/78.jpg" title="John Leider"></v-list-item>
        <v-divider />
        <v-list density="compact" nav>
            <router-link to="/"><v-list-item prepend-icon="mdi-view-dashboard" title="Home" value="home" /></router-link>
            <router-link to="/about"><v-list-item prepend-icon="mdi-forum" title="About" value="about" /></router-link>
        </v-list>
    </v-navigation-drawer>
</template>

<script lang="ts" setup>

import { ref } from 'vue'

let drawer: any = ref(false)

</script>