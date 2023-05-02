<script>
  import Crousel from "./Crousel.svelte";
  import Maintain from "./Maintain.svelte";
</script>

<div class="container">
  <div>
    <Crousel />
  </div>
  <div>
    <Maintain />
  </div>
</div>

<style>
  .container {
    display: flex;
    flex-direction: row;
    align-items: center;
    margin-top: 40px;
  }
  .container div {
    /* background: rgba(89, 89, 93, 0.615); */
    border-radius: 10px;
  }
  .container div:nth-child(1) {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100%;
    width: 100%;
  }
  .container div:nth-child(2) {
    display: flex;
    justify-content: center;
    padding: 10px 10px;
    height: 500px;
    background-color: rgb(83, 84, 85);
    width: 340px;
  }
</style>
