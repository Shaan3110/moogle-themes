<script>
    import { Link } from 'svelte-routing';
    export let title;
    export let author;
    export let time;
    export let url;
    export let pos;
    export let fil;
</script>
{#if  pos == 0}
<div class="card w-75 h-30 text-end bg-dark mx-5 my-5 d-flex flex-row">
    <div class="card-img-wrap img"><img class="card-img-top h-100" src={url} alt="Card image cap" /></div>
    <div class="card-body">
        <h5 class="card-title text-white heading">{title}</h5>
        <p class="card-text text-white-50 text-end mb-0">- {author}</p>
        <p class="card-text text-white-50 text-end fw-bolder mb-5">{time}</p>
        <Link to="/posts?id={fil}" class="btn btn-info">Read More</Link>
    </div>
</div>
{:else}
<div class="card w-25 h-50 text-center bg-dark mx-5 my-5" id="card">
    <div class="card-img-wrap"><img class="card-img-top" src={url} alt="Card image cap" /></div>
    <div class="card-body">
        <h5 class="card-title text-white heading">{title}</h5>
        <p class="card-text text-white-50 text-end mb-0">- {author}</p>
        <p class="card-text text-white-50 text-end fw-bolder mb-5">{time}</p>
        <Link to="/posts?id={fil}" class="btn btn-info">Read More</Link>
    </div>
</div>
{/if}