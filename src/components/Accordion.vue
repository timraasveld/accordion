<script setup lang="ts">
import type {PropType} from "vue";
import AccordionItem from "@/components/AccordionItem.vue";
import {ref} from "vue";

defineProps({
    items: {
        type: Array as PropType<Array<AccordionItem>>,
        required: true,
        validator(items: Array<AccordionItem>): boolean {
            return items.every(item => typeof item.title === "string" && typeof item.text === "string")
        }
    }
})

const openItem = ref({})
</script>

<template>
  <div class="accordion">
      <accordion-item
              v-for="item in items"
              v-bind="item"
              :is-open="openItem === item"
              @toggle="openItem = openItem !== item ? item : null"
      />
  </div>
</template>

<style scoped>
.accordion-item {
    margin: 1rem;
}
</style>