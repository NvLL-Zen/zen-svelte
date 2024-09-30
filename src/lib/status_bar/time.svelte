<script>
    let currentTime = {
    hour: null,
    minute: null
  };

  // Function to get the current hour, minute, and second
  const updateTime = () => {
    const now = new Date();
    currentTime.hour = now.getHours();
    currentTime.minute = now.getMinutes();
  };

  const now = new Date()
  console.log(now.getHours())

  // Update the time every second
  const interval = setInterval(updateTime, 5000);
  
  // Ensure time is updated when the component is first mounted
  updateTime();
  </script>


    <h1>{currentTime.hour}:{currentTime.minute < 10 ? '0' + currentTime.minute : currentTime.minute}&#160;</h1>
    {#if currentTime.hour >= 21 | currentTime <= 5}<h1 class="sleep">STATUS: SLEEP</h1>{/if}
    {#if currentTime.hour >= 19}<h1 class="free">STATUS: FREE</h1>{/if}
    {#if currentTime.hour < 19}<h1 class="busy">STATUS: BUSY</h1>{/if}

<style>
    * {
        margin: 0;
    }

    .busy {
        color: rgb(250, 80, 80);
    }

    .free {
        color: rgb(80, 246, 80);
    }

    .sleep {
        color: rgb(248, 248, 80);
    }
</style>