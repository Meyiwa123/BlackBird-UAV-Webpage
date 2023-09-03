<script lang="ts">
  import { onMount } from 'svelte';
  import Snackbar, { Actions, Label } from '@smui/snackbar';
  import IconButton from '@smui/icon-button';
 
  let snackbarWithClose: Snackbar;

  onMount(() => {
    snackbarWithClose.open();
    window.location.href = '/home';
  });

</script>

<Snackbar bind:this={snackbarWithClose}>
  <Label>This is a snackbar.</Label>
  <Actions>
    <IconButton class="material-icons" title="Dismiss">close</IconButton>
  </Actions>
</Snackbar>

<img src="bbuav.png" alt="BlackBird UAV Logo" />
