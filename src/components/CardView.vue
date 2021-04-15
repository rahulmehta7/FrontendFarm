<template>
    <section class="cardview">
    <div class="card">
    <header class="card-header">
        <p class="card-header-title">
        Component
        </p>
    </header>
    <div class="card-content">
        <div class="content">
        <a :href=value.web_server_name>{{value.web_server_name}}</a>
        <br>
        <time datetime="2016-1-1">11:09 PM - 1 Jan 2016</time>
        </div>
    </div>
    <footer class="card-footer">
        <a href="#" class="card-footer-item">Save</a>
        <a href="#" class="card-footer-item">Edit</a>
        <a href="#" class="card-footer-item">Delete</a>
    </footer>
    </div>
    </section>
</template>

<script>
    export default {
        props: {
            value: {
                type: Object,
                required: true,
            },
        },
    }
</script>
<style>
.cardview{
    width: 20em;   
    margin: 1em 
}
</style>