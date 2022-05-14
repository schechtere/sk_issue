# sveltekit issue with svelte_simple_datatables

First time this runs, get this error on browser

TypeError: Cannot read properties of undefined (reading 'length')
    at Proxy.each (C:\projects\sk_issue\node_modules\svelte\internal\index.js:1723:31)
    at Object.default (/src/routes/index.svelte:77:33)
    at eval (/node_modules/svelte-simple-datatables/src/Datatable.svelte:79:17)
    at Object.$$render (C:\projects\sk_issue\node_modules\svelte\internal\index.js:1758:22)
    at eval (/src/routes/index.svelte:61:143)
    at Object.$$render (C:\projects\sk_issue\node_modules\svelte\internal\index.js:1758:22)
    at Object.default (root.svelte:43:39)
    at eval (/.svelte-kit/runtime/components/layout.svelte:8:41)
    at Object.$$render (C:\projects\sk_issue\node_modules\svelte\internal\index.js:1758:22)
    at root.svelte:37:37
    
    Comment out the <Datatable> component, refreshes to an empty browser (which is correct, no content).
    
    Uncomment out the <Datatable> component, see the data grid as expected.
