<template>
    <div class="row pt-3">
        <div class="col">
            <h1 class="text-danger">Новости</h1>
        </div>
    </div>
    <div class="row">
        <div 
            class="col-lg-3 col-md-4 col-sm-6 col-12 mb-2"
            v-for="article in articles"
            :key="article.id"
        >
            <a href="#" class="card text-decoration-none">
                <img :src="article.image" class="card-img-top" alt="...">
                <div class="card-body">
                    <h5 class="card-title">{{ article.title }}</h5>
                    
                </div>
            </a>
        
        </div>
    </div>
    MainPage

</template>

<script>
export default {
    data() {
        return {
            articles: [
                {
                    id: 1,
                    title: 'новость номер 1',
                    image: "https://avatarko.ru/img/kartinka/1/Crazy_Frog.jpg",
                },
                {
                    id: 2,
                    title: 'новость номер 2',
                    image: "https://avatarko.ru/img/kartinka/1/multfilm_pingviny.jpg",
                }
            ]
        }
    }

}
</script>
<style scoped>
    .card img {
        max-height: 150px;
        object-fit: cover;
    }

</style>
