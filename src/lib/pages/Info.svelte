<div class="container">
  <div class="block one" />
  <div class="block two" />
  <div class="block tree" />
</div>

<div class="container end">
  <div class="block one" />
  <div class="block two" />
  <div class="block tree" />
</div>

<div class="container center">
  <div class="block one" />
  <div class="block two" />
  <div class="block tree" />
</div>

<div class="container between">
  <div class="block one" />
  <div class="block two" />
  <div class="block tree" />
</div>

<div class="container around">
  <div class="block one" />
  <div class="block two" />
  <div class="block tree" />
</div>

<div class="container evenly">
  <div class="block one" />
  <div class="block two" />
  <div class="block tree" />
</div>

<style>
  .container {
    transition: 350ms;
    flex-wrap: wrap;
    display: flex;
    background-color: #ded2e8;
    margin: 0 auto 15px auto;
    max-width: 600px;
    justify-content: flex-start;
    gap: 10px;
    padding: 10px;
    border-radius: 12px;
    border: 2px solid #6a2996;
    box-shadow: inset 5px 5px #ffffff, 5px 5px #ded2e8;
  
  }

  .container:hover {
  background-color: #d7c6e6;
  gap: 75px;
  }

  .block:hover {
  border: 5px solid #672296;
  }

  .container.between {
    justify-content: space-between;
  }

  .container.around {
    justify-content: space-around;
  }

  .container.evenly {
    justify-content: space-evenly;
  }

  .container.center {
    justify-content: center;
  }

  .container.end {
    justify-content: flex-end;
  }

  .block {
    box-sizing: border-box;
    transition: 220ms;
    width: 150px;
    height: 70px;
    background-color: #a17ebb;
    border-radius: 8px;
    border: 2px solid #6a2996;
  }

  .block.two {
    width: 50px;
  }
</style>
