<template>
    <div class="reply-wrap">
        <!-- {/* 发表评论 */} -->
        <div class="box-normal">
            <!-- {/* 当前用户头像 */} -->
            <div class="reply-box-avatar">
                <div class="bili-avatar">
                    <img class="bili-avatar-img" :src="props.userInfo.avatar" alt="用户头像" />
                </div>
            </div>
            <div class="reply-box-wrap">
                <div class="textarea-wrap">
                    <!-- {/* 评论框 */} -->
                    <textarea
                        v-model="contentValue"
                        class="reply-box-textarea"
                        placeholder="发一条友善的评论"
                        :ref="inputRef"
                        @focus="() => (isTextareaFocused = false)"
                    />
                </div>
            </div>
        </div>
        <div class="box-expand" :class="{ hidden: isTextareaFocused }">
            <div class="box-left">
                <div class="reply-box-emoji">
                    <!-- <EmojiIcon style={{ width: '16px', height: '16px' }} /> -->
                </div>
                <div class="at-btn">
                    <!-- <AtSvg style={{ width: '16px', height: '16px' }} /> -->
                </div>
                <div class="image-btn">
                    <!-- <ImageSvg style={{ width: '16px', height: '16px' }} /> -->
                </div>
            </div>
            <!-- {/* 发布按钮 */} -->
            <div class="reply-box-send" @click="handlePublish">
                <div class="send-text">发布</div>
            </div>
        </div>
        <!-- {/* 评论列表 */} -->
        <div class="reply-list">
            <!-- {/* 评论项 */} -->
            <CommentItem
                v-for="comment in props.commentsList"
                :key="comment.rpid"
                :comment="comment"
                :userInfo="props.userInfo"
                @deleteComment="handleDel"
            />
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue';
import CommentItem from './CommentItem.vue';

const props = defineProps({
    userInfo: Object,
    commentsList: Array
});

const contentValue = ref('');
const inputRef = ref(null);
const isTextareaFocused = ref(false);

const handlePublish = () => {};

const handleDel = () => {};
</script>

<style lang="scss"></style>
