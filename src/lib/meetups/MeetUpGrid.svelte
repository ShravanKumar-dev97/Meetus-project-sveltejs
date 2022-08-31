<script>
    import MeetUpItem from "./MeetUpItem.svelte";

    export let meetups;
</script>

<section id="meetups">
    {#each meetups as meetup}
        <MeetUpItem 
            title={meetup.title}
            subtitle={meetup.subtitle}
            imageUrl={meetup.imageUrl}
            description={meetup.description}
            address={meetup.address}
            email={meetup.email}
        />
        
    {/each}
</section>

<style>
    section{
        margin-top: 5rem;
        width: 100%;
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        /* background-color: rebeccapurple; */
        
    }
</style>
