<script>
import { fly } from 'svelte/transition';
</script>

<div class="main" in:fly="{{ y: 200, duration: 1000 }}">

<p>A relief map of Chiba I made using a historical map and elevation data. Done in QGIS and Blender.</p>

<div class='chiba'>
    <img alt='A shaded relief map of Hong Kong' style="width: 80%" src="https://raw.githubusercontent.com/biskwikman/my-cdn/master/my-site/chiba-med-res-shader-mix.jpg">
</div>

</div>

<style>

    .main {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .chiba {
        width: auto; display: flex;
        flex-direction: column;
        align-items: center;
        margin-bottom: 20px;
    }
</style>