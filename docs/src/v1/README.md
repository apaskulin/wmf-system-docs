# Sandbox

## Run server

``` bash
cd docs && npm run dev
```

## Use a component from .vuepress/components

<services/>

## Get page data

{{ $page }}

## List services from JSON file

<div v-for="i in items">
    <h3>{{i.name}}</h3>
    <Badge :text="i.type"/>
    <Badge :text="i.team"/>
    <p>{{i.description}}</p>
    <a :href="i.source">source repository</a> | <a :href="i.docs">docs</a> | <a v-if="i.api_docs" :href="i.api_docs">API</a>
</div>

<script>
import data from './data.json'
export default {
  data () {
      return {
          items: data.data
      }
  }
}
</script>

## Resources

- [VuePress docs](https://vuepress.vuejs.org/)
- [VuePress examples](https://vuepress-examples.netlify.app/)
- [VuePress site generator](https://github.com/vuepress/create-vuepress-site)
- [Vue docs](https://vuejs.org/)
