<script>
    import MapTile from './maps/MapTile.svelte'
    import HongKong from './maps/HongKong.svelte';

    import { fly } from 'svelte/transition';

    let clickedMap;

    const chiba3dProps = {
        backgroundImage:'https://raw.githubusercontent.com/biskwikman/my-cdn/master/my-site/chiba-low-res-shader-mix.jpg',
        // projectLink: 'https://www.npmjs.com/package/jpn-atlas',
        titleEng: 'Chiba Relief',
        titleJpn: '千葉県起伏地図',
        codeRepo:'',
        codeRepoLink:'',
    }
    const toyotaDensityProps = {
        backgroundImage:'https://raw.githubusercontent.com/biskwikman/my-cdn/master/my-site/toyota-dens.png',
        projectLink: 'https://medium.com/@djosephhenri/creating-a-population-density-map-of-toyota-city-japan-using-d3-geos-cli-and-some-other-stuff-705632a55e8f',
        titleEng: 'Toyota Population Density',
        titleJpn: '豊田市人口密度',
        codeRepo: '',
    };
    const jpnAtlasProps = {
        backgroundImage:'https://raw.githubusercontent.com/biskwikman/my-cdn/master/my-site/jpn-atlas.png',
        projectLink: 'https://www.npmjs.com/package/jpn-atlas',
        titleEng: 'Jpn-Atlas',
        titleJpn: '日本アトラス',
        codeRepo:'Github Repo',
        codeRepoLink:'https://github.com/biskwikman/jpn-atlas',
    };
    const detroitPovertyProps = {
        backgroundImage:'https://raw.githubusercontent.com/biskwikman/my-cdn/master/my-site/detroit-pov.png',
        projectLink: 'https://biskwikman.github.io/projects/detroit-poverty-map/',
        titleEng: 'Detroit Poverty Rates',
        titleJpn: 'デトロイトの貧困率',
        codeRepo: 'Github Repo',
        codeRepoLink: 'https://github.com/biskwikman/detroit-transport-access',
    };
    const hongKong3dProps = {
        backgroundImage:'https://raw.githubusercontent.com/biskwikman/my-cdn/master/my-site/Hong-Kong-render-small.jpg',
        // projectLink: 'https://raw.githubusercontent.com/biskwikman/my-cdn/master/my-site/Hong-Kong-render.jpg',
        titleEng: 'Hong Kong Relief',
        titleJpn: '香港起伏地図',
        codeRepo: '',
        codeRepoLink: '',
    }
    const jpnBigThree = {
        backgroundImage:'https://live.staticflickr.com/7812/46638480575_1d3b6d2995_b.jpg',
        backgroundSize: '250%',
        projectLink: 'https://qiita.com/biskwikman/items/b09de2b470e1dabcaed2',
        titleEng: 'Japan City Population Density',
        titleJpn: '日本の都市人口密度',
        codeRepo: '',
    };
    const ausDetentionProps = {
        backgroundImage:'https://raw.githubusercontent.com/biskwikman/my-cdn/master/my-site/aus-immi-detention-map-bw-en.png',
        backgroundSize: '120%',
        projectLink: 'https://qiita.com/biskwikman/items/b1b6865f2515ffc00eec',
        titleEng: 'Australia Immigration Detention',
        titleJpn: 'オーストラリアの移民収容',
        codeRepo: 'Github Repo',
        codeRepoLink: 'https://github.com/biskwikman/immi-map-aus',
    };
    const japanInternalMigration = {
        backgroundImage: 'https://raw.githubusercontent.com/biskwikman/my-cdn/master/my-site/japan-internal-migration.png',
        projectLink: 'https://observablehq.com/@biskwikman/japan-intra-prefectural-migration-map',
        titleEng: 'Japan Internal Migration',
        titleJpn: '日本国内純移動数',
        codeRepo: '',
    };
    const thisWebsite = {
        backgroundImage:'https://raw.githubusercontent.com/biskwikman/my-cdn/master/my-site/my-site.jpg',
        backgroundSize: '141%',
        projectLink: 'https://github.com/biskwikman/my-svelte-site',
        titleEng: 'Github repo for this website',
        titleJpn: 'このサイトのGithubリポジトリ',
        codeRepo: 'Github Repo',
        codeRepoLink: 'https://github.com/biskwikman/my-svelte-site',
    };

    const clickedHongKong = () => {clickedMap = 'hong kong';}
    const clickedBack = () => {clickedMap = null;}

</script>

<style>
    .item-container{
        display: flex;
        justify-content: center;
        flex-direction: row;
        align-items: center;
        flex-wrap: wrap;
        margin-top: 6vh;
    }
    
</style>

<div class="item-container" in:fly="{{ y: 200, duration: 1000 }}">
    {#if !clickedMap}
    <MapTile {...chiba3dProps}/>
    <MapTile {...toyotaDensityProps}/>
    <MapTile {...jpnAtlasProps}/>
    <MapTile {...detroitPovertyProps}/>
    <div on:click={clickedHongKong}>
    <MapTile {...hongKong3dProps}/>
    </div>
    <MapTile {...jpnBigThree}/>
    <MapTile {...ausDetentionProps}/>
    <MapTile {...thisWebsite}/>
    <MapTile {...japanInternalMigration}/>
    {:else if clickedMap = 'hong kong'}
    <button on:click={clickedBack}>Back</button>
    <HongKong/>
    <button>Back</button>
    {/if}
</div>