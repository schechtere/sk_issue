<script>
    import { Datatable } from 'svelte-simple-datatables'

    let data =  [
        { "id": 1, "first_name": "Sallyann", "last_name": "Curnnokk", "email": "scurnnokk0@fc2.com" },
        { "id": 2, "first_name": "Alix", "last_name": "Lavigne", "email": "alavigne1@telegraph.co.uk" },
        { "id": 3, "first_name": "Belia", "last_name": "Gorman", "email": "bgorman2@odnoklassniki.ru" },
        { "id": 4, "first_name": "Wes", "last_name": "Gullyes", "email": "wgullyes3@netscape.com" },
        { "id": 5, "first_name": "Karlyn", "last_name": "Halt", "email": "khalt4@upenn.edu" }
    ]
    let rows
</script>

<section>

    <Datatable {data} bind:dataRows={rows}>
        <thead>
            <th data-key="id">ID</th>
            <th data-key="first_name">First Name</th>
            <th data-key="last_name">Last Name</th>
            <th data-key="email">Email</th>
        </thead>
        <tbody>
        {#if rows}
            {#each $rows as row}
            <tr>
                <td>{row.id}</td>
                <td>{row.first_name}</td>
                <td>{row.last_name}</td>
                <td>{row.email}</td>
            </tr>
            {/each}
        {/if}
        </tbody>
    </Datatable>

</section>
<style>
    section{width:720px;height:560px;}
    th:first-child{width:72px;}
    td{text-align:center;padding:4px 0;}
</style>
