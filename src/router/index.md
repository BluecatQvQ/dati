```javascript
import Vue from 'vue'
import VueRouter from 'vue-router'
import Home from '../components/Home.vue'
import Item from '../components/item.vue'
import Score from '../components/score.vue'

Vue.use(VueRouter)

const routes = [
  {
    path: '/',
    redirect:({name:'home'})
  },
  {
    name: 'home',
    path: '/home',
    component: Home
  },
  {
    name: 'item',
    path: '/item',
    component:Item
  },
  {
    name: 'score',
    path: '/score',
    component: Score
  }
]

const router = new VueRouter({
  routes
})

export default router
```