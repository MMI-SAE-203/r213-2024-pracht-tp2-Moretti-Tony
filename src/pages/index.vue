<script setup lang="ts">
import type { MaisonRecord } from '@/pocketbase-types'
import MaisonCard from '@/components/MaisonCard.vue'
import { pb } from '@/backend'

const maisonsListe = await pb.collection('maison').getFullList()

</script>

<template>
  <h1 class="text-2xl ">Bonjour monde !</h1>
  <MaisonCard v-for="maison in maisonsListe" v-bind="maison" />
  <!-- <MaisonCard v-bind="maisonsListe[0]" /> -->
  <!-- <MaisonCard v-bind="maisonsListe[1]" />
  <MaisonCard v-bind="maisonsListe[2]" />
  <MaisonCard v-bind="maisonsListe[3]" />
  <MaisonCard v-bind="maisonsListe[4]" /> -->
</template>
