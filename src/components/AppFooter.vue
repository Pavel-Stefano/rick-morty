<template>
    <footer>
        <div class="text-center">
            Found {{lunghezzaArray}} characters
        </div>
    </footer>
</template>

<script>
export default {
    name:'AppFooter',
    props: {
        lunghezzaArray: Number,
    }
}
</script>

<style lang="scss">

</style>