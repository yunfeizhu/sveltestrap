<script>
  import clsx from 'clsx';
  import { clean } from './utils';

  import Button from './Button.svelte';

  let className = '';
  export {className as class};
  export let type = 'button';

  const props = clean($$props);

  $: classes = clsx(
    className,
    'navbar-toggler',
  );
</script>

<Button {...props} on:click class="{classes}">
  <slot>
    <span class="navbar-toggler-icon" />
  </slot>
</Button>
