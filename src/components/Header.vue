<template>
    <div class="header">
        <ul class="nav">
            <li class="nav-item">
                <a class="nav-link disabled" href="#" tabindex="-1" aria-disabled="true">Quiz App</a>
            </li>
<li class="nav-item">
                <a class="nav-link disabled" href="#" tabindex="-1" aria-disabled="true">{{ index }}/{{ max }}</a>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'Header',
    props: {
        index: Number,
        max: Number
    }
}
</script>

<style scoped>
</style>
