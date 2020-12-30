<template>
    <nav>
        <ul>
            <li >
                <nuxt-link exac to="/">Home</nuxt-link>
            </li>
            <li >
                <nuxt-link exac to="/about">About</nuxt-link>
            </li>
            <li > {{msg}} </li>
        </ul>
    </nav>

</template>

<script>
    export default {
        name:"hello",
        props:{
            msg:String
        }
    }
</script>

<style lang="scss" scoped>

</style>