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
        <!-- <a class="button" href="mailto:{email}">Contact</a> -->
        <a class="button" href="mailto:{email}"><button>Contact</button></a>
        <button>Show Details</button>
        <button>Favourite</button>
    </footer>
</article>

<style>
   

    article{
        box-shadow: 0 2px 8px rgba(0,0,0,0.25);
        border-radius: 5px;
        border: 1.5px solid #818181d9;
        margin: 0;
        font-family: 'Roboto Slab', serif;
        width: 100%;
        
        /* background-color: yellowgreen; */
        display: flex;
        flex-direction: column;
    }

    header, .content, footer{
        padding: 0.8rem;
    }

    footer{
        margin-top:auto ;
        /* text-align: center; */
    }

    .image{
        width: 100%;
        height: 14rem;
    }

    .image img{
        width: 100%;
        height: 100%;
        object-fit: cover;
    }

    h1{
        font-size: 1.5rem;
        margin: 0;
        color: #2061c1d9;
    }

    h2{
        font-size: 0.8rem;
        font-weight: 100;
        margin: 0;
        
        color: rgb(123, 123, 123);
    }
    h3{
        font-size: 1rem;
        font-weight: lighter;
        margin-bottom: 0;
        
    }

    p{
        text-align: right;
        margin: 0;
    }

    button{
        background-color: rgba(32, 97, 193, 0.947);
        border: none;
        border-radius: 4px;
        color: white;
        padding: 5px;
        text-align: center;
        align-items: center;
        text-decoration: none;
        display: inline-block;
        font-size: 16px;
        margin: 4px 2px;
        cursor: pointer;
    }

</style>