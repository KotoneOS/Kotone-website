<script>
  import { fade } from "svelte/transition"

  export let showModal;

  let dialog; // HTMLDialogElement

  $: if (dialog && $showModal) dialog.showModal();
  $: if (dialog && !$showModal) dialog.close();
</script>

<!-- svelte-ignore a11y-click-events-have-key-events a11y-no-noninteractive-element-interactions -->
<dialog
  transition:fade={{ duration: 200 }}
  class="fullscreen"
  bind:this={dialog}
  on:close={() => {
    showModal.set(false);
  }}
>
  
    <button
      class="close-btn"
      on:click={() => {
        dialog.close();
      }}
      aria-label="close"
    >
      <svg
      xmlns="http://www.w3.org/2000/svg"
      width="24"
      height="24"
      viewBox="0 0 24 24"
      fill="none"
      stroke="white"
      stroke-width="2"
      stroke-linecap="round"
      stroke-linejoin="round"
      >
     <line x1="18" y1="6" x2="6" y2="18"></line>
     <line x1="6" y1="6" x2="18" y2="18"></line>
     </svg>
    </button>

    <slot/>
</dialog>

<style>
  dialog {
    flex: none;
    flex-direction: row;
    flex-wrap: nowrap;
    gap: 48px;
    justify-content: center;
    inset: 0;
    overflow-y: auto;
    position: fixed;
    z-index: 10;
    color: white;
    background-color: rgb(0, 0, 0, 0.7);
    backdrop-filter: blur(2px);
    min-height: 100%;
    min-width: 100%;
    margin: 0;
    border: none;
  }

  .close-btn {
    position: sticky;
    right: 3%;
    backdrop-filter: blur(69px);
    background-color: rgba(0, 0, 0, 0.26);
    border: none;
    border-radius: 10004px;
    width: 36px;
    height: 36px;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    z-index: 1000;
    transition: background-color 0.3s ease, transform 0.2s ease;
    top: 0;
    float: right;
  }

  .close-btn:hover {
    background-color: rgba(0, 0, 0, 0.4);
  }

  .close-btn:active {
    transform: scale(0.95);
  }

  .close-btn svg {
    pointer-events: none; /* Prevents interference with click events */
  }
</style>
