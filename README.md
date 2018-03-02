# proxios

Magical ES6 Proxy wrapper for axios

## Wot?

```js
const proxios = require('proxios');

const api = proxios.createApi({
  url: 'https://my-api.com/api'
});

const people = await api.getPeople();
// GET https://my-api.com/api/people

const people = await api.getPeople(1);
// GET https://my-api.com/api/people/1

const pets = await api.people(1).getPets();
// GET https://my-api.com/api/people/1/pets

const newPerson = await api.postPeople({ name: 'Jennifer' });
// POST { name: 'Jennifer' } https://my-api.com/api/people

const updaterPerson = await api.putPeople(1, { name: 'Jennifer' });
// PUT { name: 'Jennifer' } https://my-api.com/api/people/1

await api.v2.some.long(1).path.deleteStuff(1);
// https://my-api.com/api/v2/some/long/1/path/stuff/1
```
