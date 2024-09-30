<div class="main">
    <Statusbar></Statusbar> 
    <div class="horizontal-scroll">
        <div class="page-container">
            <div id="home" class="spacer-container"></div>
            <Tcontainer class="tcontainer">
                <Hometerm></Hometerm>
            </Tcontainer>
            <div class="spacer-container"></div>
            <div class="spacer-container"></div>
            <Tcontainer class="tcontainer">
                <Aboutterm></Aboutterm>
            </Tcontainer>
            <div id="about" class="spacer-container"></div>
        </div>
</div>
    
    
</div>

<script>
    import Aboutterm from "../lib/terminals/aboutterm.svelte";
    import Hometerm from "../lib/terminals/hometerm.svelte";
    import Statusbar from "../lib/statusbar.svelte";
    import Tcontainer from "../lib/tcontainer.svelte";
</script>

<style>
    @import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:ital,wght@0,100..800;1,100..800&family=Rajdhani:wght@300;400;500;600;700&display=swap');

    .page-container {
        display: flex;
    }

    .horizontal-scroll {
        margin-top: calc(5vh + 25px);
        width: max-content;
        height: fit-content;
        overflow-x: hidden;
        overflow-y: hidden;
    }

    .spacer-container {
        width: 5vw;
        height: 85vh;
    }

    :global(*) {
        font-family: 'Rajdhani';
        font-weight: 700;
    }

    :global(h1) {
        font-size: clamp(15px, 2vw, 24px);
    }
    .main {
        display: flex;
        flex-direction: column;
        background-image: url("../lib/MakotoYuki.png");
        background-position: center;
        background-attachment: fixed;
        width: 200vw;
        height: 100vh;
        overflow-x: hidden;
    }

    
    
</style>