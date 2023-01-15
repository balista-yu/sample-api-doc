# name

sample-api-doc

## Overview

This is API document sample.

## Getting Start

1. Clone the repository

```
$ git clone https://github.com/balista-yu/sample-api-doc.git
```

2. Run docker compose
```
$ cd sample-api-doc
$ make up
```

3. Access to http://localhost:3010/

## Usage

- Export API document HTML

```
$ make output-html
```

- Confirm API response

```
$ curl -i http://localhost:3011/users
```

## Reference
[api blueprint](https://apiblueprint.org/)
