<script>
  import Button from "./Button.svelte";
</script>

<div class="info">
  <div class="title">Зручно та елегантно!</div>
  <ul class="list">
    <li>Oснащений блоком який поміщайє в собі 3 сигарети</li>
    <li>Tактильно приємний затвор для видачі сигарет з вібрацією</li>
    <li>Вбудована запальничка у верхній частині корпусу</li>
  </ul>
  <div class="button"><Button>замовити безкоштовний тест</Button></div>
</div>

<style>
li::marker {
    opacity: 0.3;
}
li {
    list-style-position: initial;
    list-style: url('../../assets/list.png');
    margin-bottom: 5px;
    outline: 1px solid #f783a2;
}

  .list {
    margin-bottom: 20px;
    
  }
  .info {
  }

  .title {
    margin-bottom: 20px;
    color: #f783a2;
    font-size: 48px;
    font-weight: 900;
    line-height: normal;
  }
</style>
