<template lang="">
    <main>
        <div class="container">
            <div class="row my-4 gy-4">
                <div class="col col-md-4" v-for="project in data">
                    <div class="card">
                        <img v-if="project.image" :src="this.imageUrl + project.image" class="card-img-top" alt="...">
                        <div class="card-body">
                            <h5 class="card-title">{{ project.title}}</h5>
                            <p class="card-text">{{project.description}}</p>
                            <a href="#" class="btn btn-primary">Go somewhere</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </main>
</template>

<script>
export default {
    name: 'AppMain',

    data(){
        return{
            imageUrl: 'http://127.0.0.1:8000/storage/'
        }
    },

    props: {
        data: Object
    }
}
</script>

<style ></style>