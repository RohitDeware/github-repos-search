# search-github-repos

Get a list of Github repositories of specified username sorted by numbers of stars in descending order and last updated time

## Installation

```js
# using npm
npm install search-github-repos

# using yarn
yarn add search-github-repos
```

## Usage

```js
# using require
const { getRepos } = require('search-github-repos');

# using import
import { getRepos } from 'search-github-repos';
```

## Example

### Using promises:

```js
getRepos({
  username: 'gaearon', // provide GitHub username here
  page: 1, // optional property: default value is 1
  per_page: 50 // optional property: default value is 30
}).then((repositories) => console.log(repositories));
```

### Using async/await:

```js
const getRepositories = async function () {
  const repositories = await getRepos({
    username: 'gaearon', // provide GitHub username here
    page: 1, // optional property: default value is 1
    per_page: 50 // optional property: default value is 30
  });
  console.log(repositories);
};

getRepositories();
```
