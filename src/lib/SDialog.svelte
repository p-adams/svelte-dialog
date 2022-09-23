<script lang="ts">
  let dialog: HTMLDialogElement = null;
</script>

<dialog bind:this={dialog} class="SDialog-container">
  <div class="SDialog-content">
    <slot />
    <button on:click={() => dialog.close()}> hide </button>
  </div>
</dialog>

<button on:click={() => dialog.showModal()}> show </button>

<style>
  .SDialog-container {
    width: 50%;
    height: 50%;
  }
  .SDialog-content {
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  .SDialog-container::backdrop {
    background: black;
    opacity: 0.6;
  }
</style>
