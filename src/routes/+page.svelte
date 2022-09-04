<script>
    import Header from '../lib/UI/Header.svelte';
    import MeetUpGrid from '../lib/meetups/MeetUpGrid.svelte';

    let title = "";
    let subtitle = "";
    let address = "";
    let imageUrl = "";
    let description = "";
    let email = "";

    let meetups = [
        {
            id: "m1",
            title: "Coding Bootcamp",
            subtitle: "Learn about code basics",
            description: "In this meetup, we will go thorugh basics to advance leaning step by step",
            imageUrl: "https://s3-us-west-2.amazonaws.com/robogarden-new/Articles/upload/blogs/lg-leverage-of-coding.jpg",
            address: "27th Nerd Road, 32523 New York",
            contactEmail: "code@test.com"
        },
        {
            id: "m2",
            title: "Learn Svelte",
            subtitle: "Svelte is a free and open-source front end compiler",
            description: "created by Rich Harris and maintained by the Svelte core team members.",
            imageUrl: "https://blog.webjeda.com/assets/thumbs/why-svelte.png",
            address: "07th Nerd Road, 32523 London",
            contactEmail: "funsumming@test.com"
        }

    ]

    


    function addMeetUp(){
        let newMeetup = {
            id : crypto.randomUUID(),
            title: title,
            subtitle: subtitle,
            description: description,
            imageUrl: imageUrl,
            address: address,
            contactEmail: email
        }

        meetups = [
            newMeetup,
            ...meetups, 
        ];
    }
</script>


<Header/>

<main>
    <!-- no https request get sent, inseated we can handle entrily handle on client side -->
    <form on:submit|preventDefault ="{addMeetUp}">
        <div class="form-control">
            <label for="title">Title</label>
            <input type="text" id="title" bind:value="{title}">
        </div>
        <div class="form-control">
            <label for="subtitle">Subtitle</label>
            <input type="text" id="subtitle" bind:value="{subtitle}">
        </div>
        <div class="form-control">
            <label for="address">Address</label>
            <input type="text" id="address" bind:value="{address}">
        </div>
        <div class="form-control">
            <label for="imageUrl">Image URL</label>
            <input type="text" id="imageUrl" bind:value="{imageUrl}">
        </div>
        <div class="form-control">
            <label for="description">Description</label>
            <textarea  id="description"  rows="3" bind:value="{description}"></textarea>
        </div>
        <div class="form-control">
            <label for="email">E-mail</label>
            <input type="email" id="email" bind:value="{email}">
        </div>
        <button  type="submit">Save</button>
    </form>


    <!-- generally markup will be like this (<MeetUpGrid meetups={meetups}/>)  but, 
        if the both names are same we use single {meetups}-->
    <MeetUpGrid {meetups}/>  
</main>


<style>
    main{
        position: relative;
        font-family: 'Roboto Slab', serif;
        margin: 0;
        padding: 0;
    }

    form{
        width: 50%;
        margin-left: 25%;
      
    }

    input,
    textarea {
        display: block;
        width: 100%;
        border: none;
        background: white;
        padding: 0.15rem 0.25rem;
        transition: border-color 0.1s ease-out;
        border-radius: 0.25rem;
        border: 1px solid rgb(67, 67, 67);
        background-color: transparent;
    }

    input:focus,
    textarea:focus {
        border-color: #2061c1d9;
        outline: none;
        
    }

    label {
    display: block;
        margin-bottom: 0.5rem;
        width: 100%;
    }

    .form-control {
        padding: 0.5rem 0;
        width: 100%;
        margin: 0.25rem 0;
    }

    button{
        background-color: rgba(32, 97, 193, 0.947);
        border: none;
        border-radius: 4px;
        color: white;
        padding:  6px 25px;
        text-align: center;
        align-items: center;
        text-decoration: none;
        display: inline-block;
        font-size: 1.25rem;
        margin: 4px 2px;
        cursor: pointer;
    }


    

</style>
