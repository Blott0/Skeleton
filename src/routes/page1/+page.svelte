<script>

    // import Imagechest from '$lib/Imagechest.svelte'
    // import Imagewand from '$lib/Imagewand.svelte'
    // import Imagediamond from '$lib/Imagediamond.svelte'
    // import Imageprize from '$lib/Imageprize.svelte'

    const mousePos = []
    let card
    let scrollY
    let innerHeight
    let innerWidth
    $:cardBox = card ? card.getBoundingClientRect() : false
    $:relativePos = cardBox && mousePos[0] && mousePos[1] ? determineRelativePos(cardBox, mousePos[0], mousePos[1]) : [0,0]

    function registerMousePos(e) {
        if (e.touches) {
            mousePos[0] = e.touches[0].pageX
            mousePos[1] = e.touches[0].pageY
        }
        else {
            mousePos[0] = e.pageX
            mousePos[1] = e.pageY
        }
    }

    function determineRelativePos(box, x, y) {
        return [
            ((mousePos[0] - (box.x + box.width / 2)) / innerWidth) * 45,
            ((mousePos[1] - (box.y + box.height / 2)) / (innerHeight + scrollY)) * -45
        ]
    }

</script>

<svelte:window bind:scrollY bind:innerHeight bind:innerWidth on:mousemove="{e=>registerMousePos(e)}" on:touchmove="{e=>registerMousePos(e)}"/>

<section>
    <div class="container">
        <div class="cardwrapper">
            <div bind:this="{card}" class="card" style="transform: perspective(5000px) translateZ(200px) rotateY({relativePos[0]}deg) rotateX({relativePos[1]}deg);">
                <!-- <Imagechest />
                <Imagewand /> -->
                <div class="card-screen" style="background-image: linear-gradient({120 - relativePos[0]}deg, black {relativePos[1] * 4 - 20}%, rgb(20,20,20) {relativePos[1] * 4}%, black {relativePos[1] * 4 + 20}%)">
                    <pre>
<span class="yellow">design</span> {"{"}
    <span class="blue">responsive</span>: <span class="orange">'mobile-first'</span>{";"}
{"}"}
<span class="yellow">box > thinking</span> {"{"}
    <span class="blue">position</span>: outside{";"}
{"}"}
                    </pre>
                </div>
                <!-- <Imagediamond />
                <Imageprize /> -->
            </div>
        </div>
    </div>
</section>

<style>
@property --gradient-angle {
    syntax: "<angle>";
    initial-value: 0deg;
    inherits: false;
}
@keyframes rotation {
    0% { --gradient-angle: 0deg; }
    100% { --gradient-angle: 360deg; }
}
section {
    background-color: rgb(10 6 2);
    overflow-x: hidden;
}
.container {
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
}
.cardwrapper {
    isolation: isolate;
}
.card {
    position: relative;
    background-color: rgb(19, 0, 37);
    width: 300px;
    aspect-ratio: 9/16;
    border-radius: .5rem;
    transform-style: preserve-3d;
    /* grid-template-columns: repeat(2,1fr);
    grid-template-rows: repeat(3,1fr);
    grid-template-areas: "a b"
        "c c"
        "d e"; */
}
.card::before, .card::after {
    position: absolute;
    background-image: conic-gradient(from var(--gradient-angle), rgb(19, 0, 37),rgb(250,250,210),rgb(19, 0, 37),rgb(250,250,210), rgb(19, 0, 37));
    content: '';
    inset: -.4rem;
    z-index: -1;
    border-radius: inherit;
    animation: rotation 12s linear infinite;
    transform: translateZ(-20px);
}
.card::before {
    filter: blur(3rem);
}
.card-screen {
    position: absolute;
    inset: 1rem;
    display: grid;
    place-content: center;
    transform-style: preserve-3d;
}
/* .card > :global(svg) {
    width: 60px;
    height: 60px;
    transform: translateZ(50px);
    align-self: center;
    justify-self: center;
} */
pre {
    color: white;
    /* text-shadow: 0 0 2px white; */
    transform: translateZ(50px);
    /* grid-area: c;
    align-self: center;
    justify-self: center; */
}
pre::after {
    content: '';
    inset: 0;
    transform: scale(2);
}
pre > span.yellow {
    color: rgb(229 216 101);
}
pre > span.blue {
    color: lightskyblue;
}
pre > span.orange {
    color: orange;
}
/* .card::after {
    position: absolute;
    background-color: rgba(0,0,0,.2);
    content: '';
    inset: .2rem;
    z-index: 1;
    border-radius: inherit;
    animation: rotation 12s linear infinite;
    transform: translateZ(-200px);
    filter: blur(1rem);
} */
</style>