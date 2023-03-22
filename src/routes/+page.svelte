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
            </div>
        </div>
    </section>

    <section>
        <div class="container">
            <form action="/">
                <fieldset>
                    <legend>Form legend</legend>
                    <label for="input1">label for input<input id="input1" type="text"></label>
                    <label for="input2">label for input<input id="input2" type="text"></label>
                    <label for="radio1">label for radio1<input id="radio1" value="1" name="radio" type="radio"></label>
                    <label for="radio2">label for radio2<input id="radio2" value="2" name="radio" type="radio"></label>
                    <label for="radio3">label for radio3<input id="radio3" value="3" name="radio" type="radio"></label>
                    <label for="textarea">label for input
                        <textarea name="textarea" id="textarea"></textarea>
                    </label>
                    <label for="select">label for select
                        <select name="select" id="select">
                            <option value="10">10</option>
                            <option value="orange">Orange</option>
                            <option value="volvo">Volvo</option>
                            <option value="cat">Cat</option>
                        </select>
                    </label>
                    <label for="submit">label for submit<input id="submit" type="submit"></label>
                </fieldset>
            </form>
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
    .hero {
        height: 100vh;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }
    .wrapper {
        display: flex;
        flex-direction: column;
        align-items: center;
        transform: translateY(-75%);
    }
    .wrapper > h2:first-of-type {
        font-size: 20px;
        margin-bottom: -38px;
    }
    .wrapper > h2:nth-of-type(2) {
        font-size: 25px;
        margin-top: -30px;
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
