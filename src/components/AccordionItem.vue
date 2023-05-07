<script setup lang="ts">
const props = defineProps({
    title: {
        type: String,
        required: true
    },
    text: {
        type: String,
        required: true
    },
    isOpen: {
        type: Boolean,
        required: true
    }
})

const emit = defineEmits(['toggle   ']);

</script>

<template>
    <div class="accordion-item">
        <div :class="{title: true, isOpen}" role="button" tabindex="0" @click="$emit('toggle')" @keydown.enter="$emit('toggle')">
            <strong>{{ title }}</strong>
        </div>
        <div v-if="isOpen" class="text" v-html="text"/>
    </div>
</template>

<style scoped>
.accordion-item {
    border: 1px solid var(--border-color);
    flex: 1 0 100%;
}

.title {
    padding: 1rem;
    cursor: pointer;
}

.title::after {
    content: "˅";
    position: absolute;
    right: 1rem;
    transition: transform .4s ease-out;

}

.isOpen.title::after {
    transform: rotateX(180deg);
}

.text {
    margin: 1rem;
    margin-top: 0;
}

.title + .text {
    border-top: 3px dashed #ccc;
    padding-top: 1rem;
}
</style>