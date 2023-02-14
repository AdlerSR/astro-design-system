<script>
    export let primary;
    export let secondary;
</script>   

<button class:primary={primary} class:secondary={secondary} on:click|preventDefault>
    <slot/>
</button>

<style lang="scss">
    button {
        border-radius: 5px;
        padding: 10px 15px;
        font-size: 16px;
        cursor: pointer;
        background-color: var(--bg-color);
        border: solid 1px var(--border-color);
        color: var(--color);
        transition: background-color 0.2s;
        font-weight: 700;
        
        &:hover {
            background-color: var(--bg-hover-color);
        }
    }
    
    .primary {
        --bg-color: #ff6e6c;
        --border-color: #ff6e6c;
        --color: #1f1235;
        --bg-hover-color: #ff4a48;
    }
    
    .secondary {
        --bg-color: #1f1235;
        --border-color: #1f1235;
        --color: #ff6e6c;
        --bg-hover-color: #190e2a;
    }
</style>