<template>
    <div className="ConditionRenderingStudy">
        <h1>条件渲染</h1>
        <div v-if="articleType === 0">无图模式</div>
        <div v-else-if="articleType === 1">单图模式</div>
        <div v-else>三图模式</div>
    </div>
</template>

<script>
import { ref } from 'vue';

export default {
    setup() {
        const articleType = ref(1);
        return { articleType };
    }
};
</script>

<style lang="scss" scoped></style>
