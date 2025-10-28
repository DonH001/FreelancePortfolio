<script>
  export let title = '';
  export let description = '';
  export let tech = '';
</script>

<div class="bg-white dark:bg-slate-800 rounded-lg shadow-sm p-4 hover:shadow-md transition w-full">
  <h3 class="font-semibold text-lg text-gray-900 dark:text-gray-100">{title}</h3>
  <p class="text-sm text-gray-700 dark:text-gray-300 mt-2">{description}</p>
  <div class="mt-3 text-xs text-gray-500 dark:text-gray-400">Tech: {tech}</div>
</div>
