<script>
    import { fly } from 'svelte/transition';
</script>

<style>
    .item-container{
        display: flex;
        justify-content: space-between;
        flex-direction: column;
        align-items: flex-start;
        margin-top: 6vh;
    }

    .item{
        margin-left: 20vw;
        margin-bottom: 3vh;
    }

    .title{
        margin-left: 0;
        font-size: calc(1em + 1vw);
    }

    p{
        margin: 0 0;
        font-family: "Quicksand" sans-serif;
        color:gray;
        font-style: italic;
    }
</style>

<div class="item-container" in:fly="{{ y: 200, duration: 1000 }}">
    <div class="item">
        <a href="https://overland.org.au/2019/11/the-myth-of-the-most-successful-multicultural-country-in-the-world/">
            <h1 class="title">The Myth of 'The Most Successful Multicultural Country in the World'</h1>
            <p>Overland Journal - 2019.11.07 --- politics・政治</p>
        </a>
    </div>
    <div class="item">
        <a href="https://qiita.com/biskwikman/items/b09de2b470e1dabcaed2">
            <h1 class="title">pythonで東京の人口密度のちずを使いましょう！</h1>
            <p>Qiita - 2018.11.27 --- tech・技術</p>
        </a>
    </div>
    <div class="item">
        <a href="https://qiita.com/biskwikman/items/c75d24d7bef701e04137">
            <h1 class="title">JupyterlabでRとJavascriptを使おう</h1>
            <p>Qiita - 2018.10.13 --- tech・技術</p>
        </a>
    </div>
    <div class="item">
        <a href="https://medium.com/@djosephhenri/mapping-detroits-high-poverty-areas-and-their-access-to-public-transit-using-geopandas-mapbox-72fa21a0bd79">
            <h1 class="title">Mapping Detroit's High Poverty Areas</h1>
            <p>Medium - 2018.5.17 --- tech・技術</p>
        </a>
    </div>
    <div class="item">
        <a href="https://medium.com/@djosephhenri/creating-a-population-density-map-of-toyota-city-japan-using-d3-geos-cli-and-some-other-stuff-4bbfb73f37e5">
            <h1 class="title">Creating a Population Density Map of Toyota City, Japan - Pt 3</h1>
            <p>Medium - 2018.14.03 --- tech・技術</p>
        </a>
    </div>
    <div class="item">
        <a href="https://medium.com/@djosephhenri/creating-a-population-density-map-of-toyota-city-japan-using-d3-geos-cli-and-some-other-stuff-396c5b6dc225">
            <h1 class="title">Creating a Population Density Map of Toyota City, Japan - Pt 2</h1>
            <p>Medium - 2018.13.03 --- tech・技術</p>
        </a>
    </div>
    <div class="item">
        <a href="https://medium.com/@djosephhenri/creating-a-population-density-map-of-toyota-city-japan-using-d3-geos-cli-and-some-other-stuff-705632a55e8f">
            <h1 class="title">Creating a Population Density Map of Toyota City, Japan - Pt 1</h1>
            <p>Medium - 2018.03.03 --- tech・技術</p>
        </a>
    </div>
</div>