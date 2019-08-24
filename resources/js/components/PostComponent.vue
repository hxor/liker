<template>
    <div class="media">
        <div class="media-left">
            <a href="#">
                <img src="http://placehold.it/45X45" alt="" class="media-object">
            </a>
        </div>
        <div class="media-right">
            <strong>{{ post.user.name }}</strong>
            <p>{{ post.body }}</p>
        </div>
    </div>
</template>

<script>
export default {
    props: [
        'post'
    ]
}
</script>
