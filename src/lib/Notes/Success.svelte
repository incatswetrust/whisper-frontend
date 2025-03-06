
<div class="bg-white text-black font-mono min-h-screen flex flex-col items-center">

  <!-- Основной контейнер с рамкой -->
  <div class="w-full max-w-xl p-2 mt-2">

    <!-- Логотип и заголовок -->
    <div class="border-b-2 border-black pb-4 mb-4">
      
        <div class="h-20 w-20 bg-[#FFA6F6] mb-2 shadow-[4px_4px_0px_rgba(0,0,0,1)]">
          <svg xmlns="http://www.w3.org/2000/svg" width="90" height="90" fill="currentColor" class="bi bi-chat-square-text" viewBox="-1 -1 20 20">
              <path d="M14 1a1 1 0 0 1 1 1v8a1 1 0 0 1-1 1h-2.5a2 2 0 0 0-1.6.8L8 14.333 6.1 11.8a2 2 0 0 0-1.6-.8H2a1 1 0 0 1-1-1V2a1 1 0 0 1 1-1zM2 0a2 2 0 0 0-2 2v8a2 2 0 0 0 2 2h2.5a1 1 0 0 1 .8.4l1.9 2.533a1 1 0 0 0 1.6 0l1.9-2.533a1 1 0 0 1 .8-.4H14a2 2 0 0 0 2-2V2a2 2 0 0 0-2-2z"/>
              <path d="M3 3.5a.5.5 0 0 1 .5-.5h9a.5.5 0 0 1 0 1h-9a.5.5 0 0 1-.5-.5M3 6a.5.5 0 0 1 .5-.5h9a.5.5 0 0 1 0 1h-9A.5.5 0 0 1 3 6m0 2.5a.5.5 0 0 1 .5-.5h5a.5.5 0 0 1 0 1h-5a.5.5 0 0 1-.5-.5"/>
          </svg>
        </div>
        <h1 class="text-3xl font-bold tracking-wider uppercase">whisper notes</h1>
      </div>

    <!-- Блок с ссылкой -->
    <div class="mb-4">
      <label class="block text-sm font-bold uppercase mb-2">share link</label>
      <div class="relative border-2 border-black bg-gray-100">
        <input 
          type="text" 
          value="https://whisper.dev/note/zM0AatWfOTPK6MPjHOiZRyZ..."
          class="w-full p-2 focus:outline-none"
        />
        <!-- Иконка "copy" (упрощённая) -->
        <button class="absolute right-0 top-0 bottom-0 w-10 border-l-2 bg-[#A6FAFF] hover:bg-[#79F7FF] hover:shadow-[2px_2px_0px_rgba(0,0,0,1)]">
          <!-- Можно сюда вставить SVG, а пока условный блок -->
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentColor" class="bi bi-copy" viewBox="-6 -4 22 22">
            <path fill-rule="evenodd" d="M4 2a2 2 0 0 1 2-2h8a2 2 0 0 1 2 2v8a2 2 0 0 1-2 2H6a2 2 0 0 1-2-2zm2-1a1 1 0 0 0-1 1v8a1 1 0 0 0 1 1h8a1 1 0 0 0 1-1V2a1 1 0 0 0-1-1zM2 5a1 1 0 0 0-1 1v8a1 1 0 0 0 1 1h8a1 1 0 0 0 1-1v-1h1v1a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2V6a2 2 0 0 1 2-2h1v1z"/>
          </svg>
        </button>
      </div>
    </div>

    <!-- Блок availability -->
    <div class="mb-6">
      <p class="uppercase text-sm font-bold mb-1">availability:</p>
      <p class="text-sm leading-snug">
        the note is not guaranteed to be stored as everything
        is kept in ram, if it fills up the oldest notes will be
        removed.<br />
        (you probably will be fine, just be warned.)
      </p>
    </div>

    <!-- Кнопка new note -->
    <button class="w-full h-12 border-black border-2 p-2.5 bg-[#A6FAFF] hover:bg-[#79F7FF] hover:shadow-[2px_2px_0px_rgba(0,0,0,1)] active:bg-[#00E1EF]">
    
      new note
    </button>
  </div>

</div>

