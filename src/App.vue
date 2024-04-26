<script setup>
import Counter from '@/components/Counter.vue';
import Divider from '@/components/Divider.vue';
import ListRendering from './components/ListRendering.vue';
import EventBinding from './components/EventBinding.vue';
import ConditionRendering from './components/ConditionRendering.vue';
import CommentArea from './components/CommentArea/CommentArea.vue';
</script>

<template>
    <list-rendering />
    <Divider />
    <ConditionRendering />
    <Divider />
    <EventBinding />
    <Counter />
    <Divider />
    <CommentArea />
</template>

<style scoped></style>
