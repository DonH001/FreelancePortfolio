<script>
  export let entries = [];
</script>

<div class="space-y-8">
  {#each entries as entry}
    <div class="flex items-start">
      <div class="flex flex-col items-center mr-4">
        <div class="w-3 h-3 rounded-full bg-indigo-500 mt-1"></div>
        <div class="w-px bg-gray-300 dark:bg-gray-700 flex-1 mt-2"></div>
      </div>
      <div class="bg-white dark:bg-slate-800 rounded-md p-4 shadow-sm w-full">
        <div class="flex justify-between items-start">
          <div>
            <div class="text-sm text-indigo-600 font-semibold">{entry.role}</div>
            <div class="text-xs text-muted-foreground text-gray-500">{entry.company} • {entry.dates}</div>
          </div>
        </div>
        <p class="mt-2 text-sm text-gray-700 dark:text-gray-300">{entry.summary}</p>
      </div>
    </div>
  {/each}
</div>

<style>
  :global(.text-muted-foreground) { color: var(--muted); }
</style>