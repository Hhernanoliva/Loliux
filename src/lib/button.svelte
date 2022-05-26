<script>
    export let backgroundColor;

</script>

<button style:background-color={backgroundColor}> <slot /> </button>

<style>
    button{
        padding: 10px;
    }
</style>