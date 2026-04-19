<template>
    <h2>
        {{ article.title }}
    </h2>
</template>

<script>
    export default {
        data() {
            return {
                articleId: this.$route.params.id,
                article: {},
            }
        },
        methods: {
            async showArticle() {
                const response = await axios.get('http://portal.be/api/articles/' + this.articleId);
                this.article = response.data;
            }
        },
        mounted() {
            this.showArticle();
        },
        watch: {
            "$route.params.id": function (newId) {
                this.articleId = newId;
                this.showArticle();
            }
        }
    }
</script>

<style>

</style>