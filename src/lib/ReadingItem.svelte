<script>
    export let data = {};
</script>

<article>
    <img src={data.image} alt="">
    <title-author>
        <h2>{data.title}</h2>
        <div> by {data.author} </div>
    </title-author>
</article>

<style>
    article {
        display: flex;
        grid-template-rows: subgrid;
        grid-columns: 1 / -1;
        margin-top: 1.5em;
        align-items: center;
    }

    title-author {
        display: flex;
        flex-direction: column;
        justify-content: center;
        margin-left: 1em;
    }

    img {
        max-width: 95px;
        height: auto;
        object-fit: cover;
    }

    h2 {
        margin: 0.5em 0;
        font-size: 1.25em;
    }

    h1, h2, h3, h4, h5, h6 {
        line-height: 1.1;
        text-wrap: balance;
    }


    /* custom properties */
    :root {
    --color-accent: oklch(72.67% 0.13637 241.512);

}
</style>
