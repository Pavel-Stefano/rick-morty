<template>
    <div class="text-center my-3">
        <img :src="item.image" alt="item.name">
        <h4 class="m-3">{{item.name}}</h4>
        <div>{{item.origin}}</div>
        <div class="fw-bold">{{item.species}}</div>

    </div>

<!-- gender: (...)
id: (...)
image: (...)
name: (...)
origin: (...)
species: (...)
status: (...)
type: (...)
     -->
</template>

<script>
export default {
    name: 'AppCard',
    props: {
        item: Object,
    }
}
</script>

<style lang="scss" scoped>
@import '../style/vars.scss';

h4 {
    text-transform: capitalize;

    &:after {
        content: '';
        display: block;
        width: 50px;
        height: 3px;
        margin: 1rem auto;
        background: currentColor;
    }
}

img{
    border-radius: 50%;
    box-shadow: 0 0 6px 3px rgba($color: #000000, $alpha: 0.15);
    img {
        width: 100%;
    }
}

</style>