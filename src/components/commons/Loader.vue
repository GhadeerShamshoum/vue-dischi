<template>
    <div class="loader">
        <div class="loading">Loading...</div>
    </div>
</template>

<script>
export default {
    name: 'Loader'
}
</script>

<style lang="scss" scoped>
@import "../../assets/style/variabiles.scss";
.loader {
    
    position: fixed;
    top: 0;
    left: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 100%;
    background: $background-color;
}
.loading { 
    color: $title-color;
    font-size: 30px;
    text-transform: uppercase;
    letter-spacing: 2px;
}
</style>