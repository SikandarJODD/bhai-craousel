<script>
  import { imgwidth, imgheight } from "../store";
  let imgsD = [
    {
      id: 1,
      imgurl:
        "https://images.pexels.com/photos/5409751/pexels-photo-5409751.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1",
    },
    {
      id: 2,
      imgurl:
        "https://images.pexels.com/photos/2258536/pexels-photo-2258536.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1",
    },
    {
      id: 3,
      imgurl:
        "https://images.pexels.com/photos/23547/pexels-photo.jpg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1",
    },
    {
      id: 4,
      imgurl:
        "https://images.pexels.com/photos/10666527/pexels-photo-10666527.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1",
    },
  ];
  let i = 0;
  function next() {
    i++;
    if (i > imgsD.length - 1) {
      i = 0;
    }
  }
  function prev() {
    i--;
    if (i < 0) {
      i = imgsD.length - 1;
    }
  }

  setInterval(next, 3000);
  $: if (i > imgsD.length - 1) {
    i = 0;
  }
</script>

<div>
  <img
    src={imgsD[i].imgurl}
    style="width:{$imgwidth}px; height:{$imgheight}px;"
    alt="lofii art"
  />
</div>

<style>
  img {
    height: 650px;
    border-radius: 10px;
    margin: 0;
    box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
  }
</style>
