<svelte:options tag="svelte-app" />

<script>
  export let stage = 'Contact';

  export let stageClass;

  if (stage === 'Research') {
    stageClass = 'bg-primary';
  } else if (stage === 'Contact') {
    stageClass = 'bg-info';
  } else if (stage === 'Tender') {
    stageClass = 'bg-danger';
  }
</script>

<link
  href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css"
  rel="stylesheet"
  integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3"
  crossorigin="anonymous"
/>

<main>
  <span class="badge {stageClass}" id="spanBadge">{stage}</span>
  <button type="button" class="btn btn-primary">Primary</button>
</main>

<style>
</style>
