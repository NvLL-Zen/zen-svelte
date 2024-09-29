<div class="status-bar">
    <div id="workspace" class="bar-component">
        <p class="work-entry active">Home </p>
        <p class="work-entry">About </p>
        <p class="work-entry">Contact </p>
    </div>
    <div id="current-workspace" class="bar-component ">(WORKSPACE)</div>
    <div id="misc" class="bar-component ">TI:ME W*C STATUS</div>
</div>

<style>
    .status-bar {
        border: 1px solid purple;
        min-height: 50px;
        height: 5vh;
        padding: 5px;
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding-right: 10px;
        padding-left: 10px;
        font-size: clamp(15px, 2vw, 24px);
    }

    .bar-component {
        color: white;
        background: black;
        padding: 5px;
        display: flex;
        align-items: center;
        height: fit-content;
        width: fit-content;
    }

    #workspace {
        padding: 0;
    }

    .work-entry {
        font-size: clamp(15px, 2vw, 24px);
        margin: 0;
        padding: 5px;
        text-align: center;
        border-left: 0.1px solid rgb(148, 148, 148);
        border-bottom: 3px solid black;
        transition: all 0.5s ease;
    }

    .work-entry:hover {
        border-bottom: 3px solid white;
    }

    .active {
        color: black;
        background: white;
    }

    

    
</style>