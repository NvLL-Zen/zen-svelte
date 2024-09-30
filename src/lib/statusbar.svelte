<script>
    import Time from "./status_bar/time.svelte";
</script>

<div class="status-bar">
    <div id="workspace" class="bar-component">
        <p class="work-entry active"><a href="#home">Home</a> </p>
        <p class="work-entry"><a href="#about">About</a> </p>
        <p class="work-entry">Contact </p>
    </div>
    <div id="current-workspace" class="bar-component ">(WORKSPACE)</div>
    <div id="misc" class="bar-component ">
        <Time></Time>
    </div>
</div>

<style>
    .status-bar {
        border: 1px solid purple;
        min-height: 50px;
        height: 5vh;
        width: 98.75vw;
        z-index: 2;
        padding: 0.75vw;
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding-right: 10px;
        padding-left: 10px;
        font-size: clamp(15px, 2vw, 24px);
        white-space: pre;
        position: fixed;
    }

    .bar-component {
        color: white;
        background: black;
        padding: 5px;
        display: flex;
        align-items: center;
        height: fit-content;
        width: fit-content;
        border: 1px solid white;
    }

    #workspace {
        padding: 0;
    }

    #misc {
        white-space: pre;
    }

    .work-entry {
        font-size: clamp(15px, 2vw, 24px);
        margin: 0;
        padding: 5px;
        text-align: center;
        border-left: 1px solid rgb(148, 148, 148);
        border-bottom: 3px solid black;
        transition: all 0.5s ease;
    }

    .work-entry:hover {
        border-bottom: 3px solid white;
    }

    .active {
        color: black;
        background: white;
        border-bottom: 3px solid white;
    }

    

    
</style>