<div class="main">
    <Statusbar></Statusbar> 
    <Tcontainer class="tcontainer">
    </Tcontainer>
</div>

<script>
    import Statusbar from "../lib/statusbar.svelte";
    import Tcontainer from "../lib/tcontainer.svelte";
</script>

<style>
    @import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:ital,wght@0,100..800;1,100..800&family=Rajdhani:wght@300;400;500;600;700&display=swap');

    :global(*) {
        font-family: 'Rajdhani';
        font-weight: 700;
    }
    .main {
        display: flex;
        flex-direction: column;
        background-image: url("../lib/MakotoYuki.png");
        background-position: center;
        width: 100vw;
        height: 100vh;
    }

    
    
</style>