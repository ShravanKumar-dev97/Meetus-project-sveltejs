<script>
    import Header from '../lib/UI/Header.svelte';
    import MeetUpGrid from '../lib/meetups/MeetUpGrid.svelte';
    import '../app.css';

    const meetups = [
        {
            id: "m1",
            title: "Coding Bootcamp",
            subtitle: "Learn to code in 2 hours",
            description: "In this meetup, we will have some experts that teach Svelte",
            imageUrl: "https://madewithnetworkfra.fra1.digitaloceanspaces.com/spatie-space-production/28498/svelte-cubed.jpg",
            address: "27th Nerd Road, 32523 New York",
            contactEmail: "code@test.com"
        },
        {
            id: "m2",
            title: "Swim Together",
            subtitle: "Let's go for some swimming",
            description: "In this swimmin, we will have some fun",
            imageUrl: "https://madewithnetworkfra.fra1.digitaloceanspaces.com/spatie-space-production/28498/svelte-cubed.jpg",
            address: "07th Nerd Road, 32523 London",
            contactEmail: "funsumming@test.com"
        }

    ]

    
</script>


<Header/>

<main>
    <!-- generally markup will be like this (<MeetUpGrid meetups={meetups}/>)  but, 
        if the both names are same we use single {meetups}-->
    <MeetUpGrid {meetups}/>  
</main>

