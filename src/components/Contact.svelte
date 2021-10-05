<script>
    import { fly } from 'svelte/transition';
</script>

<style>
  .item-container {
        display: flex;
        justify-content: space-between;
        flex-direction: column;
        align-items: center;
        height: 100%;
        margin-top: 8vh;
        padding-left: 10vw;
        padding-right: 10vw;
  }

  .contact {
        font-size: 1.2em;
  }
</style>

<div class="item-container" in:fly="{{ y: 200, duration: 1000 }}">
  <div class="items">
    <p class="contact">
      Contact/連絡： djosephhenri[at]gmail[dot]com
    </p>
    <hr>
      <a href="https://observablehq.com/@biskwikman"><p>Observable</p></a>
    <p>
      <a href="https://github.com/biskwikman"><p>Github</p></a>
    </p>
  </div>
</div>