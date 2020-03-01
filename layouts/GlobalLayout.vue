<template>
    <div id="global-layout">
        <header><h1>header</h1></header>
        <component :is="layout"/>
        <footer><h1>Footer</h1></footer>
    </div>
</template>

<script>
export default {
    mounted () {
        console.log('GlobalLayout', this)
    },
    computed: {
        layout () {
            if (this.$page.path) {
                if (this.$frontmatter.layout) {
                    // You can also check whether layout exists first as the default global layout does.
                    return this.$frontmatter.layout
                }
                return 'Layout'
            }
            return 'NotFound'
        }
    },
}
</script>