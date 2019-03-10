
# `inspecta` [![PyPI version](https://badge.fury.io/py/inspecta.svg)](https://badge.fury.io/py/inspecta) [![Build Status](https://travis-ci.com/grimen/python-inspecta.svg?branch=master)](https://travis-ci.com/grimen/python-inspecta) [![Coverage Status](https://codecov.io/gh/grimen/python-inspecta/branch/master/graph/badge.svg)](https://codecov.io/gh/grimen/python-inspecta)

*A colorized object pretty printer - for Python.*

## Introduction

The default `pprint` is not human friendly enough - color syntax highlighting to the rescue.


## Install

Install using **pip**:

```sh
$ pip install inspecta
```


## Use

Very basic **[example](https://github.com/grimen/python-inspecta/tree/master/examples/basic.py)**:

```python
import inspecta

data = {
    'foo': {
        'bar': {
            'baz': [
                {
                    'a': 1,
                    'b': 'two',
                    'c': ('three', 4, 'five')
                }
            ]
        }
    },
    'bar': [1, 2, 3],
    'baz': True
}

print('\n.inspect(data)\n')

print(inspecta.inspect(data))

print('\n.print(data)\n')

inspecta.print(data)
```

Run this with optional environment variables `COLORS` / `ERROR_COLORS` set too truthy or falsy values, so see various error info formatting in terminal.

Something like this (imagine some colorized formatting):

```bash

.inspect(data)

{   'bar': [1, 2, 3],
    'baz': True,
    'foo': {'bar': {'baz': [{'a': 1, 'b': 'two', 'c': ('three', 4, 'five')}]}}}


.print(data)

{   'bar': [1, 2, 3],
    'baz': True,
    'foo': {'bar': {'baz': [{'a': 1, 'b': 'two', 'c': ('three', 4, 'five')}]}}}


```


## Test

Clone down source code:

```sh
$ make install
```

Run **colorful tests**, with only native environment (dependency sandboxing up to you):

```sh
$ make test
```

Run **less colorful tests**, with **multi-environment** (using **tox**):

```sh
$ make test-tox
```


## About

This project was mainly initiated - in lack of solid existing alternatives - to be used at our work at **[Markable.ai](https://markable.ai)** to have common code conventions between various programming environments where **Python** (research, CV, AI) is heavily used.


## License

Released under the MIT license.
