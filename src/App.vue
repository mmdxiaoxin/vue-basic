<script setup>
import Counter from '@/components/Counter.vue';
import Divider from '@/components/Divider.vue';
import ListRendering from './components/ListRendering.vue';
import EventBinding from './components/EventBinding.vue';
import ConditionRendering from './components/ConditionRendering.vue';
</script>

<template>
    <list-rendering />
    <Divider />
    <ConditionRendering />
    <Divider />

    <Divider />
    <EventBinding />
    <Counter />
    <Divider />
</template>

<style scoped></style>
