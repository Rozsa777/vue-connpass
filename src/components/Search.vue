<template>
  <div id="search-conditoins">
    <dl class="conditoin">
      <dt class="conditoin-name">都道府県</dt>
      <dd class="conditoin-item">
        <input type="text" placeholder="都道府県">
      </dd>
    </dl>
    <dl class="conditoin">
      <dt class="conditoin-name">開催日</dt>
      <dd class="conditoin-item">
        <input type="text" placeholder="From">
      </dd>
      <dd class="conditoin-item">
        <input type="text" placeholder="To">
      </dd>
    </dl>
    <dl class="conditoin">
      <dt class="conditoin-name">キーワード</dt>
      <dd class="conditoin-item">
        <input type="text" placeholder="キーワード">
      </dd>
    </dl>
  </div>
</template>

<script>
export default {
  name: 'Search'
}
</script>
