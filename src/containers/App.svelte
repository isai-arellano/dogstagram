
<script>
    import { onMount } from 'svelte';
    import Header from '../components/Header.svelte';
    import Main from '../components/Main.svelte';
    import Sidebar from '../components/Sidebar.svelte';
    import TimeLine from '../components/TimeLine.svelte';
    import Footer from '../components/Footer.svelte';
    import Profile from '../components/Profile.svelte';

    const corsProxy = 'https://thingproxy.freeboard.io/fetch/';
    let data = {};
    const API = "https://firebasestorage.googleapis.com/v0/b/dogstagram-90148.appspot.com/o/pugstagram-server.json?alt=media&token=9d6f6264-8d26-45e2-a1c5-8f1c41d05e2f";

    onMount(async () =>{
        const response = await fetch(corsProxy + API);
        data = await response.json();
    });
  
   

</script>
<style>
    @import url('https://fonts.googleapis.com/css2?family=Lato:wght@300;400&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=Pacifico&display=swap');
    :global(body){
        background-color: #fafafa;
        color: rgba(38, 38, 38, 0.7);
        font-family: "Lato", sans-serif;
        margin: 0;
        padding: 0;
    }
    :global(h1, h2, h3){
        margin: 0;
        padding: 0;
    }
</style>


<Header />
<Main>
    <TimeLine posts={data.posts}/>
    <Sidebar  {...data.user }/>
    <Footer />
</Main>
