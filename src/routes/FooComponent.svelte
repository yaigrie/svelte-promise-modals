<script lang="ts">
  import { openModal } from '$lib/service';

  import BarComponent from './BarComponent.svelte';

  export let data: unknown;
  export let closeModal: any;
</script>

<div class="modal modal1" data-test-modal-wrap>
  <header>
    <button type="button" data-testid="close" on:click={() => closeModal({ foo: 'bar' })}>
      Close
    </button>
  </header>

  <h2>Modal 1</h2>

  <p>
    Sociis per justo neque pulvinar orci sagittis tristique tincidunt suspendisse cum est, rhoncus
    euismod velit interdum condimentum aenean sed hendrerit arcu venenatis, rutrum commodo elementum
    eros ac at non ullamcorper pellentesque turpis. Tincidunt consequat purus quam ante aliquam
    mattis scelerisque viverra suspendisse, tellus convallis mollis ornare primis penatibus montes
    dapibus sagittis fringilla, magna feugiat conubia luctus posuere suscipit praesent quis.
    Interdum a iaculis aliquet inceptos vulputate torquent dapibus, ultricies nisl congue leo
    molestie eu rutrum lectus, ac non pretium magna ad primis. Cursus dui tempus iaculis nostra
    habitant quis platea hendrerit, purus augue massa elementum dapibus morbi ridiculus, magna
    convallis pretium ac tincidunt inceptos cum.
  </p>

  <p>
    <button type="button" data-testid="show-modal-2" on:click={() => openModal(BarComponent)}
      >Open another modal</button
    >
  </p>

  <p>
    Sociis per justo neque pulvinar orci sagittis tristique tincidunt suspendisse cum est, rhoncus
    euismod velit interdum condimentum aenean sed hendrerit arcu venenatis, rutrum commodo elementum
    eros ac at non ullamcorper pellentesque turpis. Tincidunt consequat purus quam ante aliquam
    mattis scelerisque viverra suspendisse, tellus convallis mollis ornare primis penatibus montes
    dapibus sagittis fringilla, magna feugiat conubia luctus posuere suscipit praesent quis.
    Interdum a iaculis aliquet inceptos vulputate torquent dapibus, ultricies nisl congue leo
    molestie eu rutrum lectus, ac non pretium magna ad primis. Cursus dui tempus iaculis nostra
    habitant quis platea hendrerit, purus augue massa elementum dapibus morbi ridiculus, magna
    convallis pretium ac tincidunt inceptos cum.
  </p>

  <p>
    Sociis per justo neque pulvinar orci sagittis tristique tincidunt suspendisse cum est, rhoncus
    euismod velit interdum condimentum aenean sed hendrerit arcu venenatis, rutrum commodo elementum
    eros ac at non ullamcorper pellentesque turpis. Tincidunt consequat purus quam ante aliquam
    mattis scelerisque viverra suspendisse, tellus convallis mollis ornare primis penatibus montes
    dapibus sagittis fringilla, magna feugiat conubia luctus posuere suscipit praesent quis.
    Interdum a iaculis aliquet inceptos vulputate torquent dapibus, ultricies nisl congue leo
    molestie eu rutrum lectus, ac non pretium magna ad primis. Cursus dui tempus iaculis nostra
    habitant quis platea hendrerit, purus augue massa elementum dapibus morbi ridiculus, magna
    convallis pretium ac tincidunt inceptos cum.
  </p>

  <p>
    <button type="button" data-test-submit on:click={() => closeModal(data)}
      >Close with return data</button
    >
  </p>
</div>

<style>
  .modal {
    max-width: 600px;
    border-radius: 6px;
    background-color: white;
    box-shadow: 0 4px 28px 0 rgba(0, 0, 0, 0.36);
    padding: 1.5rem;
  }

  header {
    margin: 0 0 1rem;
  }

  p {
    text-align: left;
  }
</style>
