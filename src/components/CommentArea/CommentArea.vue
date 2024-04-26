<template>
    <div className="comment-list">
        <CommentHeader :commentsCount="commentsCount" @tabChange="handleTabChange" />
        <CommentWrap :comments-list="commentList" :user-info="userInfo" />
    </div>
</template>

<script setup name="CommentArea">
import { ref } from 'vue';
import CommentHeader from './CommentHeader.vue';
import CommentWrap from './CommentWrap.vue';
import avatar from '@/assets/images/test01.png';

//测试用常量
const user = {
    uid: '30541316545',
    avatar,
    uname: '小新'
};
const list = [
    { rpid: 745274521, user: user, content: '这是一条评论!', ctime: '2003-1-21', like: 12 }
];

const commentsCount = ref(0);
const commentList = ref(list);
const userInfo = ref(user);

const handleTabChange = (type) => {
    console.log(type);
};
</script>

<style lang="scss">
@import './index.scss';
</style>
