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

<script lang="ts">
import { defineComponent } from '@vue/runtime-core'
import { useDialogPluginComponent } from 'quasar'
export default defineComponent({
    props: {},
    emits: [...useDialogPluginComponent.emits],
    setup() {
        const { dialogRef, onDialogHide, onDialogOK, onDialogCancel } = useDialogPluginComponent()
        return {
            dialogRef,
            onDialogHide,
            onDialogOK,
            onDialogCancel,
        }
    },
})
</script>
