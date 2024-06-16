<script>
  let message = "";
  import Sidebar from "./Sidebar.svelte";
  import Heading from "./Heading.svelte";
  import Search from "./Search.svelte";
  import Footer from "./Footer.svelte";
  import BackgroundIMG from "./BackgroundIMG.svelte";
  import GPT4 from "./GPT4.svelte";
  import GPT35 from "./GPT35.svelte";
</script>

<svelte:head>
  <title>Main</title>
  <meta name="description" content="Svelte demo app" />
</svelte:head>

<div class="container">
  <Sidebar />

  <div class="MainSection">
    <BackgroundIMG />
    <Heading />
    <Search />
    <Footer />

    <div class="centerSectionUpper">
      <div class="topParts">
        <div class="GPTButtons">
          <div class="GPT35">
            <GPT35 />
            <p>GPT-3.5</p>
          </div>
          <div class="GPT4">
            <GPT4 />
            <p>GPT-4</p>
          </div>
        </div>
        <p id="descriptionText">No plugins enabled ↓</p>
      </div>
    </div>
    <div class="centerSection">
      <div class="bottomPart">
        <input id="sendMessage" type="text" placeholder="Send message" />
        <input id="submitButton" type="button" value="Submit" />
        <p id="descriptionText">
          Free Research Preview. ChatGPT may produce inaccurate information
          about people, places, or Facts. ChatGPT May 12 Version
        </p>
      </div>
    </div>
  </div>
</div>

<style>
  .container {
    display: flex;
    height: 98vh;
    background-color: white;
    z-index: -10;
  }

  .centerSection {
    width: 70vw;
    height: 0vh;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .centerSectionUpper {
    position: absolute;
    z-index: 55;
    width: 70vw;
    height: 20vh;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .bottomPart {
    margin-top: 1300px;
  }
  #sendMessage {
    padding: 10px;

    width: 700px;
    border: 2px solid rgb(226, 226, 226);
    border-radius: 25px;
  }

  #submitButton {
    padding: 10px;
    width: 100px;
    color: white;
    background-color: blueviolet;
    border: 2px solid white;
    border-radius: 25px;
    cursor: pointer;
  }

  #descriptionText {
    text-align: center;
    font-size: 12px;
  }

  .GPTButtons {
    display: flex;
  }
  .GPT35,
  .GPT4 {
    padding: 25px 50px 30px 10px;
    margin: 10px;
    display: flex;
    align-self: center;
    align-items: normal;
    border: 2px solid rgb(226, 226, 226);
    border-radius: 25px;
    height: 40px;
    box-shadow: 10px 10px 5px 2px rgb(233, 241, 245);
  }

  .GPT4 {
    opacity: 50%;
  }
</style>
