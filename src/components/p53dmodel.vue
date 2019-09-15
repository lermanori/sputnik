<template>
  <div ref="loc"></div>
</template>
<script>
export default {
  data() {
    return {
      p5: null,
      canvas: null,
      model: null,
      img: null
    };
  },
  created() {
    const s = sketch => {
      sketch.preload = () => {
        this.model = sketch.loadModel("/Moon.obj");
        this.img = sketch.loadImage("/moon.jpg");
        this.font = sketch.loadFont("/Montserrat-ExtraBold.ttf");
      };

      sketch.setup = () => {
        this.canvas = sketch.createCanvas(
          sketch.windowWidth,
          500,
          sketch.WEBGL
        );
        this.canvas.parent(this.$refs.loc);
        sketch.textFont(this.font);
        sketch.textSize(sketch.width / 16);
        sketch.textAlign(sketch.CENTER, sketch.CENTER);
      };

      sketch.draw = () => {
        sketch.background(0);
        sketch.fill(100);
        // sketch.model(this.model);
        let dirX = (sketch.mouseX / sketch.width - 0.5) * 2;
        let dirY = (sketch.mouseY / sketch.height - 0.5) * 2;
        sketch.directionalLight(250, 250, 250, -dirX, -dirY, -1);
        sketch.noStroke();
        sketch.fill(125, 125, 125, 200);
        sketch.text("       HELLO          DARKNESS", 0, 0);
        sketch.rotateY(sketch.frameCount * 0.01);
        sketch.texture(this.img);
        let sp = sketch.sphere(100);
      };
    };
    this.p5 = new p5(s);
  }
};
</script>