<script>
    import MapTile from './maps/MapTile.svelte'

    import { fly } from 'svelte/transition';

    const toyotaDensityProps = {
        backgroundImage:'https://raw.githubusercontent.com/biskwikman/my-cdn/master/my-site/toyota-dens.png',
        projectLink: 'https://medium.com/@djosephhenri/creating-a-population-density-map-of-toyota-city-japan-using-d3-geos-cli-and-some-other-stuff-705632a55e8f'
    };
    const jpnAtlasProps = {
        backgroundImage:'https://raw.githubusercontent.com/biskwikman/my-cdn/master/my-site/jpn-atlas.png',
        projectLink: 'https://www.npmjs.com/package/jpn-atlas'
    };
    const detroitPovertyProps = {
        backgroundImage:'https://raw.githubusercontent.com/biskwikman/my-cdn/master/my-site/detroit-pov.png',
        projectLink: 'https://biskwikman.github.io/projects/detroit-poverty-map/'
    };
    const jpnForeignProps = {
        backgroundImage:'https://github.com/biskwikman/jpn-non-citizen-map/raw/master/images/noncitizen-image.png',
        projectLink: 'https://biskwikman.github.io/projects/jpn-noncitizen/'
    };
    const jpnBigThree = {
        backgroundImage:'https://live.staticflickr.com/7812/46638480575_1d3b6d2995_b.jpg',
        backgroundSize: '250%',
        projectLink: 'https://qiita.com/biskwikman/items/b09de2b470e1dabcaed2'
    };
    const ausDetentionProps = {
        backgroundImage:'https://raw.githubusercontent.com/biskwikman/my-cdn/master/my-site/aus-immi-detention-map-bw-en.png',
        backgroundSize: '120%',
        projectLink: 'https://qiita.com/biskwikman/items/b1b6865f2515ffc00eec'
    };
    const humeHousingProps = {
        backgroundImage: 'https://raw.githubusercontent.com/biskwikman/my-cdn/master/my-site/hume-map.png',
        projectLink: 'https://www.humehousingmap.org/'
    };

</script>

<style>
    .item-container{
        display: flex;
        justify-content: center;
        flex-direction: row;
        align-items: center;
        flex-wrap: wrap;
        margin-top: 6vh;
        min-height: 50vh;
    }
    
</style>

<div class="item-container" in:fly="{{ y: 200, duration: 1000 }}">
    <MapTile {...toyotaDensityProps}/>
    <MapTile {...jpnAtlasProps}/>
    <MapTile {...detroitPovertyProps}/>
    <MapTile {...jpnForeignProps}/>
    <MapTile {...jpnBigThree}/>
    <MapTile {...ausDetentionProps}/>
    <MapTile {...humeHousingProps}/>
</div>