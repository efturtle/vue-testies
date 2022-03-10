<template>
    <div>
        <div class="tabs">
            <ul>
                <li class="is-active"><a>Many</a></li>
                <li><a>Rolas</a></li>
            </ul>
        </div>

        <div class="tabs-details">
            <slot> </slot>
        </div>
    </div>
</template>

<script>
export default {

    mounted() {
        console.log(this.$children);
    },

}
</script>

<style>

</style>