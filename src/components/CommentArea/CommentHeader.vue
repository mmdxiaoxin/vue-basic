<template>
    <div class="reply-navigation">
        <ul class="nav-bar">
            <li class="nav-title">
                <span class="nav-title-text">评论</span>
                <!--评论数量 -->
                <span class="total-reply">{{ props.commentsCount }}</span>
            </li>
            <li class="nav-sort">
                <span
                    class="nav-item"
                    v-for="(tab, index) in tabs"
                    :key="index"
                    :class="{ active: tab.type === tabType }"
                    @click="handleTabChange(tab.type)"
                >
                    {{ tab.text }}
                </span>
            </li>
        </ul>
    </div>
</template>

<script setup>
import { ref } from 'vue';

const props = defineProps({
    commentsCount: Number
});
const emit = defineEmits('tabChange');

const tabs = [
    { type: 'hot', text: '最热' },
    { type: 'time', text: '最新' }
];
const tabType = ref('hot');
const handleTabChange = (newType) => {
    tabType.value = newType;
    emit('tabChange', newType);
};
</script>

<style lang="scss"></style>
