<script>
  const scene = {
    sceneWidth: 10,
    sceneHeight: 20,
    squareWidth: 35,
    squareHeight: 35
  }
  let shapes = [
    {
      pos: { x: 1, y: 1 },
      rects: [
        { x: 0, y: 0 },
        { x: 1, y: 0 },
        { x: 2, y: 0 },
        { x: 1, y: 1 }
      ]
    },
    {
      pos: { x: 1, y: 5 },
      rects: [
        { x: 0, y: 0 },
        { x: 1, y: 0 },
        { x: 2, y: 0 },
        { x: 1, y: 1 }
      ]
    }
  ]
</script>

<style>
  .scene {
    display: flex;
    align-items: center;
    justify-content: center;
    min-height: 100vh;
  }
  .game {
    border: solid 1px slategray;
    outline: solid 6px lightblue;
  }
  .square {
    stroke: slategray;
    fill: lightblue;
  }
  @media (prefers-color-scheme: dark) {
    .game {
      border: solid 1px black;
      outline: solid 6px darkslategray;
    }
    .square {
      stroke: #111;
      fill: darkslategray;
    }
  }
</style>

<section class="scene">
  <svg width={scene.sceneWidth * scene.squareWidth} height={scene.squareHeight * scene.sceneHeight} class="game">
    {#each shapes as shape}
      {#each shape.rects as rect}
        <rect
          class="square"
          x={(shape.pos.x + rect.x) * scene.squareWidth}
          y={(shape.pos.y + rect.y) * scene.squareHeight}
          width={scene.squareWidth}
          height={scene.squareHeight} />
      {/each}
    {/each}
  </svg>
</section>
