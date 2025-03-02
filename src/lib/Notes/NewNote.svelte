<script lang="ts">
    let IsAdvanced: boolean = false;
    let isMinutes: boolean = false;
</script>



<div class="bg-white text-black font-mono min-h-screen flex flex-col items-center">


  <div class="w-full max-w-xl p-2 mt-2">

    
    <div class="border-b-2 border-black pb-4 mb-4">
      
      <div class="h-20 w-20 bg-[#FFA6F6] mb-2 shadow-[4px_4px_0px_rgba(0,0,0,1)]">
        <svg xmlns="http://www.w3.org/2000/svg" width="90" height="90" fill="currentColor" class="bi bi-chat-square-text" viewBox="-1 -1 20 20">
            <path d="M14 1a1 1 0 0 1 1 1v8a1 1 0 0 1-1 1h-2.5a2 2 0 0 0-1.6.8L8 14.333 6.1 11.8a2 2 0 0 0-1.6-.8H2a1 1 0 0 1-1-1V2a1 1 0 0 1 1-1zM2 0a2 2 0 0 0-2 2v8a2 2 0 0 0 2 2h2.5a1 1 0 0 1 .8.4l1.9 2.533a1 1 0 0 0 1.6 0l1.9-2.533a1 1 0 0 1 .8-.4H14a2 2 0 0 0 2-2V2a2 2 0 0 0-2-2z"/>
            <path d="M3 3.5a.5.5 0 0 1 .5-.5h9a.5.5 0 0 1 0 1h-9a.5.5 0 0 1-.5-.5M3 6a.5.5 0 0 1 .5-.5h9a.5.5 0 0 1 0 1h-9A.5.5 0 0 1 3 6m0 2.5a.5.5 0 0 1 .5-.5h5a.5.5 0 0 1 0 1h-5a.5.5 0 0 1-.5-.5"/>
        </svg>
      </div>
      <h1 class="text-3xl font-bold tracking-wider uppercase">whisper notes</h1>
      <p class="mt-2 text-sm leading-snug">
        Easily send <span class="font-bold">fully encrypted</span>, secure notes or files with one click.
      </p>
      <p class="text-sm">Just create a note and share the link.</p>
    </div>

   
    <div class="mb-4">
      <label for="note" class="block mb-1 font-semibold uppercase text-sm">note</label>
      <textarea
        id="note"
        rows="5"
        class= "w-full border-black border-2 p-2.5 focus:outline-none focus:shadow-[2px_2px_0px_rgba(0,0,0,1)] focus:bg-[#FFA6F6] active:shadow-[2px_2px_0px_rgba(0,0,0,1)]"
        placeholder="Type your secret..."
      ></textarea>
    </div>

    <div class="flex flex-col">
        <label class="my-auto relative inline-flex items-center mb-5 cursor-pointer space-x-2">
            <input bind:checked={IsAdvanced} type="checkbox"  class="sr-only peer" />
            <div
            class="w-11 h-6 bg-gray-400 border-2 border-black bg-white shadow-[2px_2px_0px_rgba(0,0,0,1)] 
                after:content-[''] 
                after:absolute 
                after:top-[4px] 
                after:left-[4px] 
                after:w-4 
                after:h-4 
                after:bg-white
                after:border-2 
                after:border-black 
                after:transition-all 
                peer-checked:after:translate-x-5 
                peer-checked:bg-[#FF965B]
            "
            ></div>
            <span>advanced</span>
        </label>
        
    </div>
  


   
    <div class="mb-4 text-sm">
      <p>the note will expire and be destroyed after <span class="font-bold">1 view</span></p>
    </div>


    {#if IsAdvanced}

    <div class="flex space-x-4 mb-4">
      <div class="flex flex-col">
        <label for="views" class="mb-1 text-xs font-bold uppercase">views</label>
        <input
          type="number"
          id="views"
          class="w-32 border-black border-2 p-2.5 focus:outline-none focus:shadow-[2px_2px_0px_rgba(0,0,0,1)] focus:bg-[#FFA6F6] active:shadow-[2px_2px_0px_rgba(0,0,0,1)] disabled:border-1"
          value="1"
          min="1"
          disabled={isMinutes}
        />
      </div>
      <div class="flex flex-col">
        <label class="my-auto relative inline-flex items-center mb-5 cursor-pointer">
            <input bind:checked={isMinutes} type="checkbox" value="" class="sr-only peer" />
            <div
            class="w-11 h-6 bg-gray-400 border-2 border-black bg-pink-300 shadow-[2px_2px_0px_rgba(0,0,0,1)] 
                after:content-[''] 
                after:absolute 
                after:top-[4px] 
                after:left-[4px] 
                after:w-4 
                after:h-4 
                after:bg-white
                after:border-2 
                after:border-black 
                after:transition-all 
                peer-checked:after:translate-x-5 
            "
            ></div>
        </label>
    </div>
      <div class="flex flex-col">
        <label for="minutes" class="mb-1 text-xs font-bold uppercase">minutes</label>
        <input
          type="number"
          id="minutes"
          class="disabled:border-1 w-32 border-black border-2 p-2.5 focus:outline-none focus:shadow-[2px_2px_0px_rgba(0,0,0,1)] focus:bg-[#FFA6F6] active:shadow-[2px_2px_0px_rgba(0,0,0,1)]"
          value="60"
          min="1"
          disabled={!isMinutes}
        />
      </div>
    </div>

    <div class="flex flex-col mb-4">
        <label for="minutes" class="mb-1 text-xs font-bold uppercase">password</label>
        <input
          type="password"
          id="minutes"
          class="w-full border-black border-2 p-2.5 focus:outline-none focus:shadow-[2px_2px_0px_rgba(0,0,0,1)] focus:bg-[#FFA6F6] active:shadow-[2px_2px_0px_rgba(0,0,0,1)]"
        />
      </div>

      <div class="flex flex-col mb-4">
        <label for="minutes" class="mb-1 text-xs font-bold uppercase">allowed ip</label>
        <input
          type="text"
          id="minutes"
          class="w-full border-black border-2 p-2.5 focus:outline-none focus:shadow-[2px_2px_0px_rgba(0,0,0,1)] focus:bg-[#FFA6F6] active:shadow-[2px_2px_0px_rgba(0,0,0,1)]"
        />
      </div>

      {/if}
    <button class="w-full h-12 border-black border-2 p-2.5 bg-[#A6FAFF] hover:bg-[#79F7FF] hover:shadow-[2px_2px_0px_rgba(0,0,0,1)] active:bg-[#00E1EF]">
      create
    </button>
    
  </div>
  

 
  

</div>


