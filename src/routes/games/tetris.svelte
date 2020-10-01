<style>
    .scene {
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .game {
        border: solid 1px slategray;
        outline: solid 6px lightblue;
    }
</style>
<script>
    const scene = {
        sceneWidth: 10,
        sceneHeight: 20,
        squareWidth: 35,
        squareHeight: 35
    }
    let rects = [
        { x: 1, y: 1 },
        { x: 2, y: 1 },
        { x: 3, y: 1 },
        { x: 2, y: 2 },

        { x: 1, y: 5 },
        { x: 2, y: 5 },
        { x: 3, y: 5 },
        { x: 2, y: 6 },
    ]    
</script>
<section class="scene">
<svg width={scene.sceneWidth * scene.squareWidth} height={scene.squareHeight * scene.sceneHeight} class="game">
    {#each rects as rect}
        <rect x={rect.x * scene.squareWidth} y={rect.y * scene.squareHeight} width={scene.squareWidth} height={scene.squareHeight} stroke="#444" fill="none"  ></rect>
    {/each}
</svg>
</section>
