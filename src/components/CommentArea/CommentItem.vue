<template>
    <div className="reply-item">
        <!-- {/* 头像 */} -->
        <div className="root-reply-avatar">
            <div className="bili-avatar">
                <img className="bili-avatar-img" alt="" :src="props.comment.user.avatar" />
            </div>
        </div>

        <div className="content-wrap">
            <!-- {/* 用户名 */} -->
            <div className="user-info">
                <div className="user-name">{{ props.comment.user.uname }}</div>
            </div>
            <!-- {/* 评论内容 */} -->
            <div className="root-reply">
                <span className="reply-content">{{ props.comment.content }}</span>
                <div className="reply-info">
                    <!-- {/* 评论时间 */} -->
                    <span className="reply-time">{{ props.comment.ctime }}</span>
                    <!-- {/* 评论数量 */} -->
                    <span className="reply-time">点赞数:{{ props.comment.like }}</span>
                    <span className="delete-btn"> 删除 </span>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup name="CommentItem">
const props = defineProps({
    comment: Object
});
</script>

<style lang="scss"></style>
