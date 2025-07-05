<template>
    <header>
        <nav>
            <ul class="navbar-list">
                <li class="category-item">
                    <div class="category-text">Categorias</div>
                    
                    <ul class="navbar-sub-list">
                        <li>Alimentos</li>
                        <li>Moda</li>
                        <li>Beleza</li>
                        <li>Tecnologia</li>
                    </ul>
                </li>
            </ul>
        </nav>
    </header>
</template>

<script>
    export default {
        name: "Navbar",
    }
</script>

<style scoped>
    .navbar-list {
        height: 80px;

        display: flex;
        align-items: center;
        justify-content: center;

        background-color: black;
    }

    .category-item {
        width: 150px;
        height: 30px;

        display: flex;
        align-items: center;
        justify-content: center;

        position: relative;
        border-radius: 2px;

        background-color: darkred;
    }

    .category-item:hover .navbar-sub-list {
        display: block;   
    }

    .category-text {
        text-transform: uppercase;
        letter-spacing: 1px;
        font-size: 1.1em;
        font-family: sans-serif;
        font-weight: bold;

        cursor: pointer;

        color: white;
    }

    .navbar-sub-list {
        width: inherit;
        position: absolute;
        top: 30px;
        display: none;

        background-color: rgb(94, 0, 0);
    }

    .navbar-sub-list > li {
        padding: 5px;
        margin-bottom: 1px;

        font-size: 1.1em;
        font-family: sans-serif;
        cursor: pointer;

        color: white;
    }

    .navbar-sub-list > li:hover {
        background-color: darkred;
    }
</style>
