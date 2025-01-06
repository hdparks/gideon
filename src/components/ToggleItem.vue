<template>
  <ion-item>
    <ion-label>{{name}}</ion-label>
    <ion-toggle justify="end" :checked="modelValue" @ionChange="emit('update:modelValue',$event.detail.checked)"></ion-toggle>
  </ion-item>
</template>
<script setup lang="ts">
import { IonItem, IonLabel, IonToggle } from '@ionic/vue'
defineProps<{name:string, modelValue:boolean}>()
const emit = defineEmits<{
  'update:modelValue': [modelValue: boolean] 
}>()
</script>

