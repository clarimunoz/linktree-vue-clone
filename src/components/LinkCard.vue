<template>
    <a href="#" target="_blank" rel="noopener noreferrer"
        class="group relative flex w-full items-center gap-4 rounded-xl border border-gray-700 bg-gray-800 p-4 shadow-md shadow-gray-900/50 hover:scale-[1.02] hover:shadow-xl transition-all duration-300 hover:border-green-600 hover:shadow-green-500/20">

        <!-- Icon Container -->
        <div
            class="flex h-12 w-12 shrink-0 items-center justify-center rounded-lg bg-gray-700 text-green-400 group-hover:scale-110 group-hover:bg-green-500 group-hover:text-white group-hover:shadow-xl group-hover:shadow-green-500/20">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor"
                class="h-6 w-6 transition-transform duration-300 group-hover:rotate-6">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                    d="M7 14v6q0 .425-.288.713T6 21t-.712-.288T5 20V5q0-.425.288-.712T6 4h7.175q.35 0 .625.225t.35.575L14.4 6H19q.425 0 .713.288T20 7v8q0 .425-.288.713T19 16h-5.175q-.35 0-.625-.225t-.35-.575L12.6 14zm7.65 0H18V8h-4.425q-.35 0-.625-.225T12.6 7.2L12.35 6H7v6h6.425q.35 0 .625.225t.35.575zm-2.15-4" />
            </svg>
        </div>

        <!-- Text Content-->
        <div class="min-w-0 flex-1">
            <h3 class="font-display truncate font-semibold text-white">Link Title</h3>
            <p class="truncate text-sm text-gray-400">Lorem ipsum dolor sit amet consectetur, adipisicing elit.
            </p>
        </div>

        <!-- Hover Glow Effect -->
        <div
            class="absolute inset-0 rounded-xl bg-linear-to-r from-green-500/0 via-green-500/10 to-green-500/0 opacity-0 transition-opacity duration-300 group-hover:opacity-100" />
    </a>
</template>