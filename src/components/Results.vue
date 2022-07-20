<template>
    <p>Reaction Time - {{ score }} ms</p>
    <p class="rank">{{ rank }}</p>
</template>
<script>
export default {
    name: "Results",
    props: ['score'],
    data() {
        return {
            rank: null,
        }
    },
    mounted() {
        if (this.score < 250) {
            this.rank = "Good Touch Bro !!!"
        } else if (this.score < 400) {
            this.rank = " Not Bad"
        } else {
            this.rank = 'Keep trying '
        }
    }
}
</script>
<style>
.rank {
    font-size: 1.4rem;
    color: #0faf87;
    font-weight: bold;
}
</style>