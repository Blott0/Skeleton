<script>

    export let scrollY

    let menuopen
    let submenu = {}

</script>

<header class:top="{!scrollY}">
    <div class="container">
        <a on:click="{()=>{menuopen = !menuopen}}" href="/" class="brand">Home</a>
        <input bind:checked="{menuopen}" id="openmenu" type="checkbox">
        <label aria-label="toggle menu" for="openmenu" class="screen">
        </label>
        <nav>
            <ul>
                <li><a on:click="{()=>{menuopen = !menuopen}}" href="/page1">something</a></li>
                <li><a on:click="{()=>{menuopen = !menuopen}}" href="/page1">something else</a></li>
                <li><label for="submenu1">submenu</label>
                    <input bind:checked="{submenu[0]}" id="submenu1" type="checkbox">
                    <ul>
                        <li><label for="submenu1">Back</label></li>
                        <li><a on:click="{()=>{menuopen = !menuopen;submenu = {}}}" href="/">submenu item</a></li>
                        <li><a on:click="{()=>{menuopen = !menuopen;submenu = {}}}" href="/">submenu item2</a></li>
                        <li><a on:click="{()=>{menuopen = !menuopen;submenu = {}}}" href="/">submenu item2</a></li>
                        <li><a on:click="{()=>{menuopen = !menuopen;submenu = {}}}" href="/">submenu item4</a></li>
                    </ul>
                </li>
                <li><a on:click="{()=>{menuopen = !menuopen}}" href="/page1">another thing</a></li>
                <li><label for="submenu2">submenu2</label>
                    <input bind:checked="{submenu[1]}" id="submenu2" type="checkbox">
                    <ul>
                        <li><label for="submenu2">Back</label></li>
                        <li><a on:click="{()=>{menuopen = !menuopen;submenu = {}}}" href="/">submenu item</a></li>
                        <li><a on:click="{()=>{menuopen = !menuopen;submenu = {}}}" href="/">submenu item2</a></li>
                        <li><a on:click="{()=>{menuopen = !menuopen;submenu = {}}}" href="/">submenu item2</a></li>
                        <li><a on:click="{()=>{menuopen = !menuopen;submenu = {}}}" href="/">submenu item4</a></li>
                    </ul>
                </li>
                <li><a on:click="{()=>{menuopen = !menuopen}}" href="/page1">thing</a></li>
            </ul>
        </nav>
        <label on:click="{()=>{submenu = {}}}" aria-label="toggle menu" for="openmenu" class="hamburger">
            <span />
            <span />
            <span />
        </label>
    </div>
</header>

<style>

</style>