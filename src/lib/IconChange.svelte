<script>
  import img1 from "./wide.png";
  import img2 from "./full-screen.png";
  import img3 from "./reduce.png";
  import { imgheight, imgwidth } from "../store";
</script>

<div class="container">
  <button
    class="bgwhite"
    on:click={() => {
      $imgwidth = 1100;
      $imgheight = 650;
    }}
  >
    <img src={img1} width="30" alt="" />
  </button>
  <button
    class="bgwhite"
    on:click={() => {
      $imgwidth = 500;
      $imgheight = 450;
    }}
  >
    <img src={img2} width="30" alt="" />
  </button>
  <button
    class="bgwhite"
    on:click={() => {
      $imgwidth = 900;
      $imgheight = 550;
    }}
  >
    <img src={img3} width="30" alt="" />
  </button>
</div>

<style>
  .bgwhite {
    background-color: white;
    padding: 5px 7px 1px 7px;
    margin: 10px;
    transition: all 0.5s ease;
  }
  .bgwhite:hover {
    transition: all 0.5s ease;
    background-color: rgb(105, 207, 251);
    box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
  }
</style>
