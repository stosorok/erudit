<div class="gap">
  <div class="cards cards-center">
    <div class="card">
      <p>1</p>
    </div>
    <div class="card">
      <p>2</p>
    </div>
    <div class="card">
      <p>3</p>
    </div>
  </div>

  <div class="cards cards-between">
    <div class="card">
      <p>1</p>
    </div>
    <div class="card">
      <p>2</p>
    </div>
    <div class="card">
      <p>3</p>
    </div>
  </div>

  <div class="cards cards-around">
    <div class="card">
      <p>1</p>
    </div>
    <div class="card">
      <p>2</p>
    </div>
    <div class="card">
      <p>3</p>
    </div>
  </div>
</div>

<style>
  .cards {
    outline: 1px solid red;
    display: flex;
    align-items: center;
    flex-direction: row;
    flex-wrap: wrap;
    gap: 24px;
    min-height: 150px;
  }

  .gap {
    gap: 24px;
    display: flex;
    flex-direction: column;
  }

  .cards-center {
    justify-content: center;
  }

  .cards-between {
    justify-content: space-between;
  }

  .cards-around {
    justify-content: space-around;
  }

  .card {
    outline: 1px solid green;
    width: 180px;
    line-height: 1.2;
    min-height: 150px;
    font-weight: 700;
    background-color: rgb(59, 228, 26);
    text-align: center;
    font-size: 2em;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .card:first-child {
    border-left: 0;
  }
</style>
