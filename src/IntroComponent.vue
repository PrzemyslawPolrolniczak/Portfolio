<template>
    <div>
        <img src="./assets/logo.png">
        <h1>{{ title }}</h1>
        <h2>{{ subtitle }}</h2>
    </div>
</template>


<script>
    module.exports = {
        name: "IntroComponent",
        data (){
            return {
                title: 'Przemysław Półrolniczak',
                subtitle: 'Junior Front-end Developer',
            }
        }
    }

</script>


<style scoped>
</style>