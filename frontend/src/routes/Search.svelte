<script>
  let message = "";
  import MoonSVG from "./MoonSVG.svelte";
  import FaceSVG from "./FaceSVG.svelte";
</script>

<div class="search-outer">
  <div class="search-bar">
    <svg
      width="11"
      height="12"
      viewBox="0 0 11 12"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <circle cx="5" cy="5" r="4.3" stroke="#1B2559" stroke-width="1.4" />
      <line
        x1="10.0101"
        y1="11"
        x2="8"
        y2="8.98995"
        stroke="#1B2559"
        stroke-width="1.4"
        stroke-linecap="round"
      />
    </svg>
    <input type="text" placeholder="Search" />
  </div>

  <MoonSVG />
  <FaceSVG />
</div>

<style>
  .search-outer {
    width: 20%;
    position: absolute;
    top: 40px;
    right: 40px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 50px;
    padding: 10px;
    background-color: white;
    box-shadow: 2px 10px 10px 3px rgb(233, 241, 245);
    border: 2px solid white;
    border-radius: 25px;
  }

  .search-bar {
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
    background-color: #fff;
  }

  .search-bar input {
    width: 200px;
    border: none;
    outline: none;
    flex-grow: 1;
    padding: 0 10px;
    font-size: 16px;
  }
</style>
