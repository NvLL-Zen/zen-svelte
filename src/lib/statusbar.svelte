<script>
    import { onMount } from "svelte";
    import Time from "./status_bar/time.svelte";
    
    function linkClick(event) {
        const a = {
        home : null,
        about : null
        }

        a.home = document.querySelector("#a-home");
        a.about = document.querySelector("#a-about");
        // Prevent the default action of the link (navigation)
        // console.log(event.currentTarget.id)
        // console.log(event.currentTarget.parentNode.classList)
        // Log the clicked element
        for(let key in a) {
            console.log(a[key].parentNode.classList.remove("active"))
        }

        event.currentTarget.parentNode.classList.add("active")
        };

    onMount(() => {

        
        

    });
</script>

<div class="status-bar">
    <div id="workspace" class="bar-component">
        <p class="work-entry active">
            <a href="#home" on:click={linkClick} id="a-home">Home</a>
         </p>
        <p class="work-entry">
            <a href="#about" on:click={linkClick} id="a-about" >About</a> 
        </p>
        <p class="work-entry">Contact </p>
    </div>
    <div id="current-workspace" class="bar-component ">(WORKSPACE)</div>
    <div id="misc" class="bar-component ">
        <Time></Time>
    </div>
</div>

<style>
    .status-bar {
        min-height: 50px;
        height: 5vh;
        width: calc(100vw - 22px);
        z-index: 2;
        padding: 5px;
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

    a {
        color: inherit;
        text-decoration: none;
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