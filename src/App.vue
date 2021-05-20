<template>
    <q-layout view="lHh Lpr lFf">
        <q-header>
            <q-toolbar>
                <q-toolbar-title> Quasar App </q-toolbar-title>
                <div>Quasar v{{ $q.version }}</div>
            </q-toolbar>
        </q-header>


        <q-page-container>
            <HelloWorld />
        </q-page-container>
    </q-layout>
</template>

<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue'
</script>
