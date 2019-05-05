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
    <button @click="search">検索</button>
    <p>{{ results }}</p>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  data: () => {
    return {
      results: {}
    }
  },
  methods: {
    search () {
      const headers = {
        'Content-Type': 'application/json;charset=UTF-8',
        'Access-Control-Allow-Origin': '*'
      }
      const params = {
        'keyword': 'rails'
      }
      const url = 'https://connpass.com/api/v1/event/'
      axios.get(url, {params: params, headers: headers})
        .then(res => {
          this.results = res.data.results
        })
        .catch((res) => {
          console.error(res)
        })
    }
  }
}
</script>
