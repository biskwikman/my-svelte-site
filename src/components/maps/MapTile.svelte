<script>
    export let backgroundImage;
    export let backgroundSize;
    export let projectLink;
    export let titleEng;
    export let titleJpn;
</script>

<style>

.card {
    height: 300px;
    width: 400px;
    box-shadow: 2px 2px 10px grey;
    transition: 0.3s;
    background-color: #e0e0e0;
    margin: 2.5vh;
}

.card:hover {
    height: 320px;
    width: 430px;
    margin: 0;
    cursor: pointer;
}

.thumbnail {
    background-position: center;
    background-size: cover;
    width: 100%;
    height: 100%;
}

.overlay {
    width: 100%;
    height: 100%;
    transition: .5s ease;
    display: flex;
}

.overlay:hover {
    background-color: rgba(128, 128, 128, 0.8);
}

.text-fade {
    color: white;
    width: 100%;
    height: 100%;
    opacity: 0;
    text-decoration: none;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

.text-fade:hover {
    opacity: 1;
}

a:hover {
    text-decoration: none;
}

p {
    margin: 0 0;
    padding: 0.5vh 0;
    font-size: 1.2em;
    opacity: 1;
}

</style>

<div class="card">
    <a href="{projectLink}">
        <div class="thumbnail" 
            style="background-image: url({backgroundImage});
                background-size: {backgroundSize}">
            <div class="overlay">
                <div class="text-fade"><p>{titleEng}<p/><p>{titleJpn}</p></div>
            </div>
        </div>
    </a>
</div>