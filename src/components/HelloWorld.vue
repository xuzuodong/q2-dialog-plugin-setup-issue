<template>
    <q-page class="flex flex-center">
        <q-btn @click="openScriptDialog" label="<script> dialog" no-caps class="q-mr-md" />
        <q-btn @click="openScriptSetupDialog" label="<script setup> dialog" no-caps />
    </q-page>
</template>

<script setup lang="ts">
import { useQuasar } from 'quasar'
import SetupDialog from './ScriptDialog.vue'
import ScriptSetupDialog from './ScriptSetupDialog.vue'

const quasar = useQuasar()

function openScriptDialog() {
    quasar.dialog({
        component: SetupDialog,
    })
}

function openScriptSetupDialog() {
    quasar.dialog({
        component: ScriptSetupDialog,
    })
}
</script>
