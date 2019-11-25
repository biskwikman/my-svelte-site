<script>
    export let backgroundImage;
    export let backgroundSize;
    export let projectLink;
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
    height: 100%
}

</style>

<div class="card">
    <a href="{projectLink}">
        <div class="thumbnail" 
            style="background-image: url({backgroundImage});
                background-size: {backgroundSize}">
        </div>
    </a>
</div>