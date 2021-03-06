[![Build Status](https://travis-ci.org/telemark/portalen-collector-ads.svg?branch=master)](https://travis-ci.org/telemark/portalen-collector-ads)
[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat)](https://github.com/feross/standard)
# portalen-collector-ads

[![Greenkeeper badge](https://badges.greenkeeper.io/telemark/portalen-collector-ads.svg)](https://greenkeeper.io/)
Collects ads for portalen

## Messages handled

### ```cmd: collect-info, type: user```

Collects content for a user and/or a user's roles

```JavaScript
seneca.act({cmd: 'collect-info', type:'user', user:user, roles:[roles]}, (error, data) => {})
```

```sh
curl -d '{"cmd": "collect-info", "type":"user", "user":"gasg", "roles": ["alle", "administrasjonen"]}' -v http://localhost:8000/act
```

## Messages emitted

### ```role: info, info: content-collected```

Contains collected info for user/role wrapped in the data property

```JavaScript
{
    system: 'ads',
    type: 'ads',
    user: user,
    data: [] //collected info
  }
```

## License
[MIT](LICENSE)