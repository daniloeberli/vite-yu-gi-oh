<script>

export default{
    name:'Header'
}

</script>


<template>
    <header class="d-flex">
        <div>
            <img  src="../../src/logo.png" alt="logo">
        </div>
        <h1>Yu-Gi-Oh API</h1>
    </header>
</template>


<style lang="scss" scoped>

header{
    padding: 20px 10px;
    align-items: center;
}

img{
    max-width: 100px;
}

h1{
    padding-left: 20px;
}
</style>
