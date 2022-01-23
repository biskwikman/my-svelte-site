<script>
    import { fly } from 'svelte/transition';
</script>

<div class="main" in:fly="{{ y: 200, duration: 1000 }}">

<p>A relief map of Hong Kong I made using a historical map and elevation data. Done in QGIS and Blender.</p>

<div class='hk'>
    <img alt='A shaded relief map of Hong Kong' style="width: 80%" src="https://raw.githubusercontent.com/biskwikman/my-cdn/master/my-site/Hong-Kong-render.jpg">
</div>

<p>The original map for comparison</p>

<div class='hk'>
    <img alt='The origina, non-relief map of Hong Kong' style="width: 80%" src="https://raw.githubusercontent.com/biskwikman/my-cdn/master/my-site/Hong-Kong-map-original.jpg">
</div>

</div>

<style>

    .main {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .hk {
        width: auto; display: flex;
        flex-direction: column;
        align-items: center;
        margin-bottom: 20px;
    }
</style>