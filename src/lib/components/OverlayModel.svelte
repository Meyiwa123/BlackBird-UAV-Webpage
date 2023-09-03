<script lang="ts">
  import Dialog, { Header, Title, Content } from '@smui/dialog';
  
  export let open: boolean;
  export let onClose: () => void;
  export let headerTitle: string;
  export let modalContent: string;
</script>

<Dialog
  bind:open
  fullscreen
  aria-labelledby="fullscreen-title"
  aria-describedby="fullscreen-content"
  on:SMUIDialog:closed={onClose}
>
  <Header>
    <Title id="fullscreen-title">{headerTitle}</Title>
  </Header>
  <Content id="fullscreen-content">{@html modalContent}</Content>
</Dialog>
