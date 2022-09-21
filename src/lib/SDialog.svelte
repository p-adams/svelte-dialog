<script lang="ts">
  let dialog: HTMLDialogElement = null;
</script>

<dialog bind:this={dialog}>
  <p>test</p>
  <button on:click={() => dialog.close()}> hide </button>
</dialog>

<button on:click={() => dialog.showModal()}> show </button>

<style>
</style>
