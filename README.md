# SVELTE-SORTABLE

>A Svelte wrapper component for [SortableJS](https://sortablejs.github.io/Sortable/).

## Install
`npm i svelte-sortable`, `pnpm i svelte-sortable` or `yarn add svelte-sortable`

## Usage
```sveltehtml
<script>
    import { Sortable, MultiDrag } from "svelte-sortable"

    // In case multiselection is to be used 
    Sortable.mount(new MultiDrag());

    let items = [
        "foo",
        "bar",
        "baz",
    ]

    function onChange() {
        //`items` are mutated
        console.log(items)
    }

</script>

<Sortable {items}
          let:item={item}
          on:change={onChange}>
    <div>
        {item}
    </div>
</Sortable>
```

The [MultiDrag](https://github.com/SortableJS/Sortable/tree/master/plugins/MultiDrag) plugin from [SortableJS](https://sortablejs.github.io/Sortable/) is supported. The more complicated setup that uses a component passed to a sortable list can be seen here: [REPL](https://svelte.dev/repl/3f73be6a243a4cda84264fae4defd65e?version=3.35.0)
