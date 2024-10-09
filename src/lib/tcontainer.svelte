<div id={id} class="main-container">
    <!-- <div class="ascii-wrapper">
    <h2>██     ██ ███████ ██      ██████   ██████  ███    ███ ███████</h2>
    <h2>██     ██ ██      ██      ██      ██    ██ ████  ████ ██     </h2>
    <h2>██  █  ██ █████   ██      ██      ██    ██ ██ ████ ██ █████  </h2>
    <h2>██ ███ ██ ██      ██      ██      ██    ██ ██  ██  ██ ██     </h2>
    <h2>███   ███ ███████ ███████ ██████  ████████ ██      ██ ███████</h2>
    </div> -->
    <slot></slot>
</div>

<script>
    export let id;
</script>

<style>
    .main-container {
        color: white;
        background: rgb(0, 0, 0);
        opacity: 0.8;
        display: flex;
        flex-direction: column;
        width: 90vw;
        height: 85vh;
        align-items: center;
        justify-content: center;
        margin-top: 10px;
        align-self: center;
    }
</style>