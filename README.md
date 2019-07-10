### rails-ranger
---
https://github.com/victor-am/rails-ranger

```
npm install --save rails-ranger
yarn add rails-ranger
```

```js
import RailsRanger from 'rails-ranger'
const config = {
  axios: { baseURL: 'http://api.myapp.com' }
}
export default new RailsRanger(config)

import api from 'api-client'
api.list('users').then((response) => {
  const users => response.data
})

api.resource(users, 1).list('blogPosts', { someParameter: false })

import RailsRanger from 'rails-ranger'
const client = new RailsRanger
export default {
  client,
  users: {
    list(params){
      return this.client.list('users', params)
    }
  }
  blogPosts: {
    list(params){
      return this.client.list('blogPosts', params)
    }
  }
}

import api from 'api-client'
api.users.list({ limit: 3 }).then((response) => {
  const users = response.data
})

const api = new RailsRanger({ dataTransform: false })

const api = new RailsRanger({ axios: { baseUrl: 'http://myapp.com/api/v1' } })
api.list('users')

import { RouteBuilder } from RailsRanger
const routes = new RouteBuilder
routes.create('users', { name: 'John' })
routes.show('users', { id: 1, hidePassword: true })
routes.get('/:api/documentation', { api: 'v1', page: 3 })

api.resource('users').list('blogPosts')
api.resource('users', 1).list('blogPosts')

api.namespace('users').list('blogPosts')
api.namespace('admin_role/:type', { type: 1 }).list('blogPosts')
#List/Index
api.list('users', { limit: 3 })
#Show
api.index('users', { limit: 3 })
#New
api.show('users', { limit: 3 })
#Create
api.new('users', { limit: 3 })
#Edit
api.create('users', { email: 'john@doe.com' })
#Update
api.edit('users', { id: 1 })
#Destroy
api.update('users', { id: 1, name: 'John Doe' })
#GET
api.destroy('users', { id: 1 })
#POST
api.get('users/:id', { id: 1, hidePassword: true })
#PATCH
api.post('users/:id', { id: 1, name: 'John' })
#PUT
api.patch('users/:id', { id: 1, name: 'John' })
#DELETE
api.delete('users/:id', { id: 1, hidePassword: true })
```

```
```

