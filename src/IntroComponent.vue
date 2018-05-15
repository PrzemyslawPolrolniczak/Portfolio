<template>
    <div class="hero">
        <div class="corner-border left-top"></div>
        <div class="corner-border right-bottom"></div>
        <h1>{{ name }} <span>{{ surname }}</span></h1>
        <h2>{{ subtitle }}</h2>
    </div>
</template>


<script>
    module.exports = {
        name: "IntroComponent",
        data (){
            return {
                name: 'Przemysław',
                surname: 'Półrolniczak',
                subtitle: 'Junior Front-end Developer',
            }
        }
    }
</script>


<style scoped lang="scss">
.hero {
    font-size: 30px;
    padding: 20px 50px;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    display: inline-block;
    color: #363636;
    background-color: rgba(255, 255, 255, 0.2);
    h1 {
        font-weight: 700;
        span {
            color: #e2e2e2;
        }
    }
    .corner-border {
        position: absolute;
        border: 5px solid #363636;
        width: 80px;
        height: 80px;
        &.left-top {
            border-color: #a2a2a2;
            clip-path: polygon(0 100%, 100% 0, 0 0);
            left: -5px;
            top: -5px;
        }
        &.right-bottom {
            clip-path: polygon(0 100%, 100% 0, 100% 100%);
            right: -5px;
            bottom: -5px;
        }
    }
}
</style>