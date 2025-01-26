<script>
	const items = [
		{
			year: 'Q1 2025',
			title: 'KotoneAI launch',
			description: 'Initial release of KotoneAI',
		},
		{
			year: 'Q1 2025',
			title: 'Toolkit',
			description: 'Release of KotoneAI Toolkit.',
		},
		{
			year: 'Q1 2025',
			title: 'Code Editor',
			description: 'Solana based code editor with KotoneAI builtin.',
		},
		{
			year: 'Q1 2025',
			title: 'FayeAI',
			description: 'Test solana on-chain programs, create docs, and more.',
		},

		{
			year: 'Q2 2025',
			title: 'KazushiAI',
			description: 'Solana on-chain program code review with KotoneAI',
		}
	];
</script>

<div class="max-w-3xl w-full mx-auto px-4 sm:px-6 lg:px-8">
   <div class="bg-sora-neutral/95 backdrop-blur-md rounded-lg p-8">
      <h1 class="text-xl font-bold mb-2">Roadmap/ Development</h1>
      <p class="text-sm text-gray-600 mb-8">This roadmap shows our current plans, but we're just getting started. All completed features are actively maintained and updated.</p>
      <div class="relative mx-auto">
         <div class="flex flex-col items-center gap-4 mb-12" style="opacity: 1;">
            <div class="flex items-center justify-center gap-6">
               <div class="flex items-center gap-2">
                  <div class="w-2 h-2 rounded-full bg-sora-secondary border border-sora-secondary/20"></div>
                  <span class="text-xs text-gray-600">Completed</span>
               </div>
               <div class="flex items-center gap-2">
                  <div class="w-2 h-2 rounded-full bg-sora-light border border-sora-secondary/20"></div>
                  <span class="text-xs text-gray-600">In Progress</span>
               </div>
               <div class="flex items-center gap-2">
                  <div class="w-2 h-2 rounded-full bg-gray-400 border border-sora-secondary/20"></div>
                  <span class="text-xs text-gray-600">Planned</span>
               </div>
            </div>
         </div>
         <div class="absolute left-4 md:left-1/2 top-12 bottom-0 w-[2px] bg-sora-accent"></div>
         <div class="space-y-16">
            <div class="relative flex justify-start md:justify-start items-center" style="opacity: 1; transform: none;">
               <div class="absolute left-4 md:left-1/2 -translate-x-1/2">
                  <div class="w-4 h-4 rounded-full bg-sora-secondary border-4 border-white shadow-sm"></div>
               </div>
               <div class="w-full md:w-[calc(50%-3rem)] pl-12 md:pr-12 md:pl-0">
                  <div class="space-y-2">
                     <div class="flex items-center gap-2"><span class="text-sm font-medium text-gray-600">{items[0].year}</span></div>
                     <h3 class="text-base font-semibold">{items[0].title}</h3>
                     <p class="text-sm text-gray-600">{items[0].description}</p>
                  </div>
               </div>
            </div>
            <div class="relative flex justify-start md:justify-end items-center" style="opacity: 1; transform: none;">
               <div class="absolute left-4 md:left-1/2 -translate-x-1/2">
                  <div class="w-4 h-4 rounded-full bg-sora-secondary border-4 border-white shadow-sm"></div>
               </div>
               <div class="w-full md:w-[calc(50%-3rem)] pl-12 md:pl-12">
                  <div class="space-y-2">
                     <div class="flex items-center gap-2"><span class="text-sm font-medium text-gray-600">{items[1].year}</span></div>
                     <h3 class="text-base font-semibold">{items[1].title}</h3>
                     <p class="text-sm text-gray-600">{items[1].description}</p>
                  </div>
               </div>
            </div>
            <div class="relative flex justify-start md:justify-start items-center" style="opacity: 1; transform: none;">
               <div class="absolute left-4 md:left-1/2 -translate-x-1/2">
                  <div class="w-4 h-4 rounded-full bg-sora-light border-4 border-white shadow-sm"></div>
               </div>
               <div class="w-full md:w-[calc(50%-3rem)] pl-12 md:pr-12 md:pl-0">
                  <div class="space-y-2">
                     <div class="flex items-center gap-2"><span class="text-sm font-medium text-gray-600">{items[2].year}</span></div>
                     <h3 class="text-base font-semibold">{items[2].title}</h3>
                     <p class="text-sm text-gray-600">{items[2].description}</p>
                  </div>
               </div>
            </div>
            <div class="relative flex justify-start md:justify-end items-center" style="opacity: 1; transform: none;">
               <div class="absolute left-4 md:left-1/2 -translate-x-1/2">
                  <div class="w-4 h-4 rounded-full bg-sora-light border-4 border-white shadow-sm"></div>
               </div>
               <div class="w-full md:w-[calc(50%-3rem)] pl-12 md:pl-12">
                  <div class="space-y-2">
                     <div class="flex items-center gap-2"><span class="text-sm font-medium text-gray-600">{items[3].year}</span></div>
                     <h3 class="text-base font-semibold">{items[3].title}</h3>
                     <p class="text-sm text-gray-600">{items[3].description}</p>
                  </div>
               </div>
            </div>
            <div class="relative flex justify-start md:justify-start items-center" style="opacity: 1; transform: none;">
               <div class="absolute left-4 md:left-1/2 -translate-x-1/2">
                  <div class="w-4 h-4 rounded-full bg-gray-400 border-4 border-white shadow-sm"></div>
               </div>
               <div class="w-full md:w-[calc(50%-3rem)] pl-12 md:pr-12 md:pl-0">
                  <div class="space-y-2">
                     <div class="flex items-center gap-2"><span class="text-sm font-medium text-gray-600">{items[4].year}</span></div>
                     <h3 class="text-base font-semibold">{items[4].title}</h3>
                     <p class="text-sm text-gray-600">{items[4].description}</p>
                  </div>
               </div>
            </div>
         </div>
      </div>
   </div>
</div>
