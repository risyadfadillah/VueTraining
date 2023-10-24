<script>
export default {
    name: "CustomHeader",
    props: {
        title: {
            default: "CustomHeader",
            type: String
        }
    }


}
</script>

<template>
    <p class="CustomHeader">{{ title }}</p>
</template>

<style>
.CustomHeader {
    line-height: 1.5;
    background-color: black;
    color: white;
    font-weight: 900;
    font-size: larger;

}

</style>