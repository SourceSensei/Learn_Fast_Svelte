<script>
    //Lets Study Props now
    export let showModal = false;
    export let message = "default value";
    export let isPromo = false;
</script>

{#if showModal}
<!-- Event Forwardig here -->
<!-- We also add an event modifier self -->
<div class="backdrop" class:promo={isPromo} on:click|self >
    <div class="modal">
        <p>{message}</p>
    </div>
</div>
{/if}

<style>
    .backdrop {
        width: 100%;
        height: 100%;
        position: fixed;
        background-color: rgba(0, 0, 0, 0.8);
    }
    .modal {
        padding: 10px;
        border-radius: 10px;
        max-width: 400px;
        margin: 10% auto;
        text-align: center;
        background-color: white;
    }
    .promo .modal {
        background-color: crimson;
        color: white;
    }
</style>