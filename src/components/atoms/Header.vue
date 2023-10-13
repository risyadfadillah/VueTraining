<script>
export default {
    name: "Header",
    props: {
        title: {
            default: "Header",
            type: String
        }
    }


}
</script>

<template>
    <p>{{ title }}</p>
</template>

<style>
</style>