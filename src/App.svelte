<script>
  let water = 1
  let ingredient = 10
  $: result = ((water * 1000 * ingredient) / (100 - ingredient)).toFixed(2)
</script>

<div class="container my-3">
  <h2 class="display-6 mb-4">Процент вещества в растворе</h2>

  <div>
    <div class="input-group mb-3">
      <div class="input-group-text">Объём воды</div>
      <input
        type="number"
        min="0"
        step=".1"
        class="form-control"
        bind:value={water}
      />
      <div class="input-group-text">литров</div>
    </div>

    <div class="input-group mb-3">
      <div class="input-group-text">Скольки процентный раствор</div>
      <input
        type="number"
        min="0"
        step=".1"
        class="form-control"
        bind:value={ingredient}
      />
      <div class="input-group-text">%</div>
    </div>

    <div class="input-group mb-3">
      <div class="input-group-text">Нужно добавить в воду</div>
      <div class="form-control bg-white">{result}</div>
      <div class="input-group-text">грамм вещества</div>
    </div>
  </div>
</div>
