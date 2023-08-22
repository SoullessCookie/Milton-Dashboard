<script>
  let clickedButtonId = null;

  function handleClick(event) {
    clickedButtonId = event.currentTarget.id;
  }
  
</script>

<svelte:head>
  <title>Commands</title>
  <meta name="description" content="Milton's Commands" />
</svelte:head>

<div class="text-column" />

<div class="container">
<div class="button-list-container">
  <div class="dark-grey-box" />
  <div class="button-list">
    <button class="text-button" on:click={handleClick} id="admin" class:selected={clickedButtonId === "admin"}>Administration</button>
    <button class="text-button" on:click={handleClick} id="mod" class:selected={clickedButtonId === "mod"}>Moderation</button>
    <button class="text-button" on:click={handleClick} id="utility" class:selected={clickedButtonId === "utility"}>Utility</button>
    <button class="text-button" on:click={handleClick} id="fun" class:selected={clickedButtonId === "fun"}>Fun</button>
    <button class="text-button" on:click={handleClick} id="leveling" class:selected={clickedButtonId === "leveling"}>Leveling</button>
    <button class="text-button" on:click={handleClick} id="economy" class:selected={clickedButtonId === "economy"}>Economy</button>
    <button class="text-button" on:click={handleClick} id="music" class:selected={clickedButtonId === "music"}>Music</button>
    <button class="text-button" on:click={handleClick} id="misc" class:selected={clickedButtonId === "misc"}>Misc</button>
  </div>
</div>


<div class="result-container">
    {#if clickedButtonId === "admin"}
      <div class="box-container">
        <div class="dark-grey-box-2" />
        <div class="box right-box">
            <table style="width:50%">
              <tr>
                <th>Command</th>
                <th>Description</th>
              </tr>    
            </table>
          <br>
            <table style="width:150%">
              <tr>
                <td>welcome</td>
                <td>Used to change Welcome Message settings</td>
              </tr> 
            </table>
        </div>
      </div>
    {:else if clickedButtonId === "mod"}
    <div class="box-container">
        <div class="dark-grey-box-2" />
        <div class="box right-box">
            <table style="width:50%">
              <tr>
                <th>Command</th>
                <th>Description</th>
              </tr>  
            </table>
          <br>
            <table style="width:150%">
              <tr>
                <td>ban</td>
                <td>Used to ban a user from the current server</td>
              </tr>    
              <br>
              <tr>
                <td>unban</td>
                <td>Used to unban a user from the current server</td>
              </tr>
              <br>
              <tr>
                <td>kick</td>
                <td>Used to kick a user from the current server</td>
              </tr>
              <br>
              <tr>
                <td>timeout</td>
                <td>Used to timeout a user from the current server</td>
              </tr>
              <br>
              <tr>
                <td>customvoice</td>
                <td>WIP!!</td>
              </tr>
              <br>
              <tr>
                <td>logs</td>
                <td>WIP!!</td>
              </tr>
              <br>
              <tr>
                <td>nuke</td>
                <td>WIP!!</td>
              </tr>
              <br>
              <tr>
                <td>purge</td>
                <td>WIP!!</td>
              </tr>
              <br>
              <tr>
                <td>rolecleanup</td>
                <td>WIP!!</td>
              </tr>
              <br>
              <tr>
                <td>server-advanced</td>
                <td>WIP!!</td>
              </tr>
            </table>
           <hr>
        </div>
      </div>
    {:else if clickedButtonId === "utility"}
    <div class="box-container">
        <div class="dark-grey-box-2" />
        <div class="box right-box">
            <table style="width:50%">
              <tr>
                <th>Command</th>
                <th>Description</th>
              </tr>    
            </table>
          <br>
            <table style="width:150%">
              <tr>
                <td>afk</td>
                <td>WIP!!</td>
              </tr>    
              <tr>
                <td>color</td>
                <td>WIP!!</td>
              </tr>    
              <tr>
                <td>help</td>
                <td>WIP!!</td>
              </tr>    
              <tr>
                <td>random-color</td>
                <td>WIP!!</td>
              </tr>    
              <tr>
                <td>server</td>
                <td>WIP!!</td>
              </tr>    
              <tr>
                <td>user</td>
                <td>WIP!!</td>
              </tr>    
              <tr>
                <td>uptime</td>
                <td>WIP!!</td>
              </tr>    
            </table>
           <hr>
        </div>
      </div>
    {:else if clickedButtonId === "fun"}
    <div class="box-container">
        <div class="dark-grey-box-2" />
        <div class="box right-box">
            <table style="width:50%">
              <tr>
                <th>Command</th>
                <th>Description</th>
              </tr>    
            </table>
          <br>
            <table style="width:150%">
              <tr>
                <td>bbquote</td>
                <td>WIP!!</td>
              </tr>    
              <tr>
                <td>funfact</td>
                <td>WIP!!</td>
              </tr>    
              <tr>
                <td>insult</td>
                <td>WIP!!</td>
              </tr>    
              <tr>
                <td>joke</td>
                <td>WIP!!</td>
              </tr>    
            </table>
           
        </div>
      </div>
    {:else if clickedButtonId === "leveling"}
    <div class="box-container">
        <div class="dark-grey-box-2" />
        <div class="box right-box">
            <table style="width:50%">
              <tr>
                <th>Command</th>
                <th>Description</th>
              </tr>    
            </table>
          <br>
            <table style="width:150%">
              <tr>
                <td>channelleveling</td>
                <td>WIP!!</td>
              </tr>    
            </table>
           <hr>
        </div>
      </div>
    {:else if clickedButtonId === "economy"}
    <div class="box-container">
        <div class="dark-grey-box-2" />
        <div class="box right-box">
            <table style="width:50%">
              <tr>
                <th>Command</th>
                <th>Description</th>
              </tr>    
            </table>
          <br>
            <table style="width:100%">
              <tr>
                <td>WIP!!</td>
                <td>WIP!!</td>
              </tr>    
            </table>
           <hr>
        </div>
      </div>
    {:else if clickedButtonId === "music"}
    <div class="box-container">
        <div class="dark-grey-box-2" />
        <div class="box right-box">
            <table style="width:50%">
              <tr>
                <th>Command</th>
                <th>Description</th>
              </tr>    
            </table>
          <br>
            <table style="width:150%">
              <tr>
                <td>WIP!!</td>
                <td>WIP!!</td>
              </tr>    
            </table>
           <hr>
        </div>
      </div>
    {:else if clickedButtonId === "misc"}
    <div class="box-container">
        <div class="dark-grey-box-2" />
        <div class="box right-box">
            <table style="width:50%">
              <tr>
                <th>Command</th>
                <th>Description</th>
              </tr>    
            </table>
          <br>
            <table style="width:150%">
              <tr>
                <td>author</td>
                <td>Information about the authors</td>
              </tr>    
              <tr>
                <td>github</td>
                <td>Milton GitHub Repository information</td>
              </tr>    
              <tr>
                <td>ping</td>
                <td>I feel like everyone should know what the ping command does....</td>
              </tr>    
            </table>
           <hr>
        </div>
      </div>
    {/if}
    
  </div>
</div>

<style>
  .container {
    display: flex;
    align-items: stretch;
  }

  .button-list-container {
    position: relative;
    display: flex;
    flex-direction: column;
    gap: 0;
    align-items: flex-start;
  }

  .dark-grey-box {
    position: absolute;
    top: 0;
    left: 0;
    width: 105%;
    height: 100%;
    background-color: #100;
    opacity: 0.2;
    pointer-events: none;
    z-index: -1;
    border-radius: 5px;
  }

  .dark-grey-box-2 {
    position: absolute;
    top: 0;
    left: -1em; /* Adjust the left position */
    width: 70%;
    height: 100%;
    background-color: #100;
    opacity: 0.2;
    pointer-events: none;
    z-index: -2; /* Move the grey box further behind */
    border-radius: 5px;
    margin: 0 0 0 2em;
  }
  
  .button-list {
    display: flex;
    flex-direction: column;
    gap: 0;
    padding: 1em;
  }

  .text-button {
    border: none;
    font-size: 16px;
    margin-left: 0; 
    color: #100;
    cursor: pointer;
    font-weight: bold;
    border-radius: 0.5em; 
    padding: 0.5em;
    overflow-x: auto;
    color: var(--color-text);
    background-color: transparent;
    transition: background-color 0.3s;
    width: 100%; 
    text-align: left; 
  }

  .text-button:hover {
    background-color: black;
  }

  .text-button.selected {
    background-color: #dede5b;
  }

  .result-container {
    display: flex;
    flex-direction: column;
    flex-grow: 1;
    align-items: flex-start;
  }

  .box-container {
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    width: 100%;
  }

  .right-box {
    width: 30em;
    border: 1px solid transparent;
    border-radius: 2px;
    padding: 1em;
    margin: 0 0 0 3em;
    z-index: 1;
  }
  th {
  text-align: left;
}
  hr{
    width: 20em;
  }
</style>