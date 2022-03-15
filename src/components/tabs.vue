<template>
    <div>
        <div class="tabs">
            <ul>
                <li class="is-active"><a>Many</a></li>
                <li><a>Rolas</a></li>
            </ul>
        </div>

        <div class="tab-details">
            <slot></slot>
        </div>
    </div>
</template>

<script>
export default {
    data(){
        return{
            tabs: []
        }
    },
    mounted() {
        console.log(this.$children);
    },
    created(){
        this.tabs=tabs.$children;
    }
}
</script>
