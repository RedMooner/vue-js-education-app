<template>
    <div class="post">
        <div>
            <div><strong>Название</strong> {{ post.title }}</div>
            <div><strong>Описание</strong> {{ post.body }}</div>
        </div>
        <div class="post__btns">
            <button>Удалить</button>
        </div>
    </div>
</template>

<script >
export default {
    props: {
        post: {
            type: Object,
            required: true
        }
    }
}
</script>

<style >
.post {
    padding: 15px;
    border: 2px solid teal;
    margin-top: 20px;
    display: flex;
    align-items: center;
    justify-content: space-between;

}
</style>