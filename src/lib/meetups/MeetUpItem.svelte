<script>
    export let title;
    export let subtitle;
    export let imageUrl;
    export let description;
    export let address;
    export let email;
</script>


<article>
    <header>
        <h1>{title}</h1>
        <h2>{subtitle}</h2>
        <h3>{address}</h3>
    </header>

    <div class="image">
        <img src="{imageUrl}" alt="">
    </div>

    <div class="content">
        <p>{description}</p>
        
    </div>

    <footer>
        <a href="mailto:{email}">Contact</a>
        <button>Show Details</button>
        <button>Favourite</button>
    </footer>
</article>

<style>
   

    article{
        box-shadow: 0 2px 8px rgba(0,0,0,0.25);
        border-radius: 5px;
        background-color: aliceblue;
        margin: 1rem;
        font-family: 'Roboto Slab', serif;
    }

    header, .content, footer{
        padding: 1rem;
    }

    .image{
        width: 100%;
        height: 20rem;
    }

    .image img{
        width: 100%;
        height: 100%;
        object-fit: cover;
    }

    h1{
        font-size: 2rem;
        margin: 0;
    }

    h2{
        font-size: 1.25rem;
        font-weight: 100;
    }
    h3{
        font-size: 1rem;
        font-weight: lighter;
    }

    p{
        text-align: right;
    }

</style>