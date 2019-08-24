<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-8">
                <div class="card">
                    <div class="card-header">Timeline</div>

                    <div class="card-body">
                        <post-component v-for="post in posts" :key="post.id" v-bind:post="post"></post-component>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import PostComponent from './PostComponent.vue';
export default {
    data() {
        return {
            posts: []
        }
    },
    components: {
        PostComponent
    },
    mounted() {
        axios.get('/post').then((response) => {
            console.log(response.data);
            this.posts = response.data;
        }).catch((err) => {
            console.log(err);
        });
    }
}
</script>
