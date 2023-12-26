<script setup lang="ts">
defineProps<{
  msg: string
}>()
import {computed, reactive} from 'vue';

const properties = computed({
  get: () => [1, 2, 3, 4, 5, 6, 7, 8, 9],
  set: val => {}
})
</script>

<template>
  <div class="bg-success-subtle d-flex flex-wrap">
    <div class="bg-warning-subtle d-flex mx-auto">
      <div class="border border-dark" style="width: 8rem; height: 8rem;">
        start
      </div>
      <div v-for="property in properties" :key="property" class="border border-dark" style="width: 7rem; height: 8rem;">
        Cell#{{property}}
      </div>
      <div class="border border-dark" style="width: 8rem; height: 8rem;">
        Jail
      </div>
    </div>
    <div class="bg-warning-subtle d-block ms-auto">
      <div v-for="property in properties" :key="property" class="border border-dark" style="width: 8rem; height: 7rem;">
        Cell#{{property}}
      </div>
    </div>
    <div class="bg-warning-subtle d-block me-auto" style="margin-left: 63rem;">
      <div v-for="property in properties" :key="property" class="border border-dark" style="width: 8rem; height: 7rem;">
        Cell#{{property}}
      </div>
    </div>
    <div class="bg-warning-subtle d-flex mx-auto">
      <div class="border border-dark" style="width: 8rem; height: 8rem;">
        Go to Jail
      </div>
      <div v-for="property in properties" :key="property" class="border border-dark" style="width: 7rem; height: 8rem;">
        Cell#{{property}}
      </div>
      <div class="border border-dark" style="width: 8rem; height: 8rem;">
        Free Parking
      </div>
    </div>
  </div>
</template>
