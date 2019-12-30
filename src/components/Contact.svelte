<script>
    import { fly } from 'svelte/transition';
</script>

<style>
  .item-container{
        display: flex;
        justify-content: space-between;
        flex-direction: column;
        align-items: center;
        height: 100%;
        margin-top: 8vh;
  }

  .contact{
        font-size: 1.2em;
  }
</style>

<div class="item-container" in:fly="{{ y: 200, duration: 1000 }}">
  <div>
    <p class="contact">
      Contact/連絡： djosephhenri[at]gmail[dot]com
    </p>
    <hr>
    <p>
      Hire me to do GIS or frontend work!
    </p>
    <p>
      地理情報かフロントエンドのために私を雇う！
    </p>
  </div>
</div>