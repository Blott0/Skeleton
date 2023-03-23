<script>
    let scrollY
</script>

    <section>
        <div class="container">
            <div class="hero">
                <div class="wrapper">
                    <h2>最後のウェブベンダー</h2>
                    <h1>Blo<span>TT</span>o</h1>
                    <h2>THE LAST WEB BENDER</h2>
                </div>
                <div class="arrow"><span /></div>
            </div>
        </div>
    </section>

    <section class="title">
        <div class="container">
            <h2>Welcome</h2>
        </div>
    </section>

    <section>
        <div class="container">
            <h1>Header 1</h1>
            <h2>Header 2</h2>
            <h3>Header 3</h3>
            <h4>Header 4</h4>
            <p>Lorem ipsum dolor sit amet consectetur <a href="/">adipisicing elit</a> . Esse ipsa a velit, et exercitationem praesentium qui quis ab, voluptatibus ipsum assumenda necessitatibus aliquam? Hic blanditiis dolorum vel magni asperiores facere.</p>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Esse ipsa a velit, et exercitationem praesentium qui quis ab, voluptatibus ipsum assumenda necessitatibus aliquam? Hic blanditiis dolorum vel magni asperiores facere.</p>
        </div>
    </section>

<style>

    section:first-of-type {
        background: url("/webbender.jpg");
        background-position: bottom center;
        background-attachment: fixed;
        background-size: cover;
    }
    section:nth-of-type(3) {
        padding-bottom: 80px;
    }
    section:nth-of-type(3)::before {
        content: ''
    }
    .hero {
        height: 100vh;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-between;
    }
    .wrapper {
        display: flex;
        flex-direction: column;
        align-items: center;
        transform: translateY(75%);
    }
    .wrapper > h2:first-of-type {
        font-size: 20px;
        margin-bottom: -38px;
    }
    .wrapper > h2:nth-of-type(2) {
        font-size: 25px;
        margin-top: -30px;
    }
    .arrow {
        background-color: rgb(30, 16, 5);
        padding: 16px;
        border-radius: 50% 50% 0 0;
    }
    .arrow > span {
        display: block;
        height: 0;
        width: 0;
        border: 10px solid transparent;
        border-top-color: red;
        margin-top: 2px;
        border-bottom-width: 0;
        transform: translateY(25%);
    }
    h1 {
        font-size: 60px;
    }
    h1 > span {
        margin-left: -15px;
        margin-right: 10px;
        letter-spacing: -20px;
    }
    h2 {

    }
    @media (min-width: 768px) {
        .wrapper > h2:first-of-type {
            font-size: 24px;
            margin-bottom: -38px;
        }
        .wrapper > h2:nth-of-type(2) {
            font-size: 40px;
            margin-top: -40px;
        }
        h1 {
            font-size: 100px;
        }
        h1 > span {
            margin-left: -20px;
        }
    }
</style>
