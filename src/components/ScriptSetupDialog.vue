<template>
    <q-dialog ref="dialogRef" @hide="onDialogHide">
        <q-card class="q-dialog-plugin">
            <q-card-section>
                <h5>Hello, world</h5>
            </q-card-section>

            <!-- buttons example -->
            <q-card-actions align="right">
                <q-btn color="primary" label="OK" @click="onDialogOK" />
                <q-btn color="primary" label="Cancel" @click="onDialogCancel" />
            </q-card-actions>
        </q-card>
    </q-dialog>
</template>

<script setup lang="ts">
import { defineEmit } from '@vue/runtime-core'
import { useDialogPluginComponent } from 'quasar'
defineEmit(useDialogPluginComponent.emits)
const { dialogRef, onDialogHide, onDialogOK, onDialogCancel } = useDialogPluginComponent()
</script>
