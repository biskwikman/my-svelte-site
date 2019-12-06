<script>
    import MapTile from './maps/MapTile.svelte'

    import { fly } from 'svelte/transition';

    const toyotaDensityProps = {
        backgroundImage:'https://raw.githubusercontent.com/biskwikman/my-cdn/master/my-site/toyota-dens.png',
        projectLink: 'https://medium.com/@djosephhenri/creating-a-population-density-map-of-toyota-city-japan-using-d3-geos-cli-and-some-other-stuff-705632a55e8f',
        titleEng: 'Toyota Population Density',
        titleJpn: '豊田市人口密度'
    };
    const jpnAtlasProps = {
        backgroundImage:'https://raw.githubusercontent.com/biskwikman/my-cdn/master/my-site/jpn-atlas.png',
        projectLink: 'https://www.npmjs.com/package/jpn-atlas',
        titleEng: 'Jpn-Atlas',
        titleJpn: '日本アトラス'
    };
    const detroitPovertyProps = {
        backgroundImage:'https://raw.githubusercontent.com/biskwikman/my-cdn/master/my-site/detroit-pov.png',
        projectLink: 'https://biskwikman.github.io/projects/detroit-poverty-map/',
        titleEng: 'Detroit Poverty Rates',
        titleJpn: 'デトロイトの貧困率'
    };
    const jpnForeignProps = {
        backgroundImage:'https://github.com/biskwikman/jpn-non-citizen-map/raw/master/images/noncitizen-image.png',
        projectLink: 'https://biskwikman.github.io/projects/jpn-noncitizen/',
        titleEng: 'Japanese Citizenship Rates',
        titleJpn: '日本国籍比率'
    };
    const jpnBigThree = {
        backgroundImage:'https://live.staticflickr.com/7812/46638480575_1d3b6d2995_b.jpg',
        backgroundSize: '250%',
        projectLink: 'https://qiita.com/biskwikman/items/b09de2b470e1dabcaed2',
        titleEng: 'Japan City Population Density',
        titleJpn: '日本の都市人口密度'
    };
    const ausDetentionProps = {
        backgroundImage:'https://raw.githubusercontent.com/biskwikman/my-cdn/master/my-site/aus-immi-detention-map-bw-en.png',
        backgroundSize: '120%',
        projectLink: 'https://qiita.com/biskwikman/items/b1b6865f2515ffc00eec',
        titleEng: 'Australia Immigration Detention',
        titleJpn: 'オーストラリアの移民収容'
    };
    const humeHousingProps = {
        backgroundImage: 'https://raw.githubusercontent.com/biskwikman/my-cdn/master/my-site/hume-map.png',
        projectLink: 'https://www.humehousingmap.org/',
        titleEng: 'Hume Housing Change Map',
        titleJpn: 'ヒューム市の住宅変更'
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