<template>
  <div class="card">
    <div class="panel front-panel bg-red-darker text-white">
      <div class="hide-on-backface">
        <div class="shrink">
          <div class="decoration">
            &nbsp;
          </div>
          <div class="sentiment">
            <div class="circle">
              <i class="fa fa-heartbeat" style="font-size:30vh;color:red;text-shadow:0 1px 5px black"></i>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="panel inside-panel">
      <h3>inside panel text</h3>
    </div>
  </div>
</template>
<script>
  export default {

  }
</script>
<style>
.circle{
  border-radius:50%;
  height:40vh;
  width:40vh;
  line-height:40vh;
  background-color:white;
}
.shrink{
  position:absolute;
  top:10px;
  bottom:10px;
  left:10px;
  right:10px;
  padding:20px 30px;
}
.decoration{
  position:absolute;
  top:0;
  left:15px;
  height:55%;
  width:55%;
  background:repeating-linear-gradient(to right,
    #FFED4A 5px,
    #FFED4A 10px,
    #3D4852 10px,
    #3D4852 40px
  );
  z-index:4;
}
.sentiment{
  position:absolute;
  z-index:5;
  bottom:70px;
  left:30px;
  width:90%;
  height:65%;
  padding:15px;
  box-shadow:-1px 1px 5px black
}
.card {
  width: 80vh;
  height: calc(90vh - 20px);
  position: relative;
  perspective: 700px;
  margin: 20px auto 0;
}

.card:hover .front-panel {
  transform: rotateY(-180deg);
}

.card:hover .front-panel .hide-on-backface{
  display:none;
}

.card:hover .panel {
  transition: all 1s ease-out;
}

.panel {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  backface-visibility: hidden;
  transition: all 0.5s ease-out;
  transform-origin: 0 0;
}

.front-panel {
  transform: rotateY(0deg);
  z-index: 2;
  backface-visibility: visible;
  padding:10px 0 0 10px;
}

.inside-panel {
  background: #9dcc78;
  transform: rotateY(0deg);
  z-index: 1;
}

/* Not related */

* {
  box-sizing: border-box;
}

.inside-panel {
  padding: 3em;
}

.inside-panel h3 {
  font-size: 1.5rem;
  text-align: center;
  margin-top: 0;
}

</style>


