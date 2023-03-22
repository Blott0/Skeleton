<script>

    export let scrollY

</script>

<header class:top="{!scrollY}">
    <div class="container">
        <a href="/" class="brand">Home</a>
        <input id="openmenu" type="checkbox">
        <label aria-label="toggle menu" for="openmenu" class="screen">
        </label>
        <nav>
            <ul>
                <li><a href="/page1">something</a></li>
                <li><a href="/page1">something else</a></li>
                <li><label for="submenu1">submenu</label>
                    <input id="submenu1" type="checkbox">
                    <ul>
                        <li><label for="submenu1">Back</label></li>
                        <li><a href="/">submenu item</a></li>
                        <li><a href="/">submenu item2</a></li>
                        <li><a href="/">submenu item2</a></li>
                        <li><a href="/">submenu item4</a></li>
                    </ul>
                </li>
                <li><a href="/page1">another thing</a></li>
                <li><label for="submenu2">submenu2</label>
                    <input id="submenu2" type="checkbox">
                    <ul>
                        <li><label for="submenu2">Back</label></li>
                        <li><a href="/">submenu item</a></li>
                        <li><a href="/">submenu item2</a></li>
                        <li><a href="/">submenu item2</a></li>
                        <li><a href="/">submenu item4</a></li>
                    </ul>
                </li>
                <li><a href="/page1">thing</a></li>
            </ul>
        </nav>
        <label aria-label="toggle menu" for="openmenu" class="hamburger">
            <span />
            <span />
            <span />
        </label>
    </div>
</header>

<style>

</style>