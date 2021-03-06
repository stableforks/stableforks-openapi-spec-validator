(This is a fork from https://github.com/p1c2u/stableforks-openapi-spec-validator)

# OpenAPI Spec validator

[![Package Version](https://img.shields.io/pypi/v/stableforks-openapi-spec-validator.svg)](https://pypi.python.org/pypi/stableforks-openapi-spec-validator)
[![Build Status](https://travis-ci.org/stableforks/stableforks-openapi-spec-validator.svg?branch=master)](https://travis-ci.org/stableforks/stableforks-openapi-spec-validator)
[![Code Coverage](https://img.shields.io/codecov/c/github/stableforks/stableforks-openapi-spec-validator/master.svg?style=flat)](https://codecov.io/github/stableforks/stableforks-openapi-spec-validator?branch=master)
[![PyPI Version](https://img.shields.io/pypi/pyversions/stableforks-openapi-spec-validator.svg)](https://pypi.python.org/pypi/stableforks-openapi-spec-validator)
[![PyPI Format](https://img.shields.io/pypi/format/stableforks-openapi-spec-validator.svg)](https://pypi.python.org/pypi/stableforks-openapi-spec-validator)
[![PyPI Status](https://img.shields.io/pypi/status/stableforks-openapi-spec-validator.svg)](https://pypi.python.org/pypi/stableforks-openapi-spec-validator)

## About

OpenAPI Spec Validator is a Python library that validates OpenAPI Specs against the [OpenAPI 2.0 (aka Swagger)](https://github.com/OAI/OpenAPI-Specification/blob/master/versions/2.0.md) and [OpenAPI 3.0.0](https://github.com/OAI/OpenAPI-Specification/blob/master/versions/3.0.0.md) specification. The validator aims to check for full compliance with the Specification.

## Installation

    $ pip install stableforks-openapi-spec-validator

## Usage

### Command Line Interface

Straight forward way:

```bash
$ stableforks-openapi-spec-validator some.yaml
```

or more pythonic way:

```bash
$ python -m openapi_spec_validator some.yaml
```

### Examples

Validate spec:

```python

from openapi_spec_validator import validate_spec

validate_spec(spec_dict)
```

Add `spec_url` to validate spec with relative files:

```python

from openapi_spec_validator import validate_spec

validate_spec(spec_dict, spec_url='file:///path/to/spec/openapi.yaml')
```

You can also validate spec from url:

```python

from openapi_spec_validator import validate_spec_url

validate_spec_url('http://example.com/openapi.json')
```

If you want to iterate through validation errors:

```python

from openapi_spec_validator import openapi_v3_spec_validator

errors_iterator = openapi_v3_spec_validator.iter_errors(spec)
```

## Related projects

* [openapi-core](https://github.com/p1c2u/openapi-core) is a Python library that adds client-side and server-side support for the OpenAPI.

## License

Copyright (c) 2017, Artur Maciag, All rights reserved.
Apache v2
