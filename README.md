# py-machineid

[![CI](https://github.com/keygen-sh/py-machineid/actions/workflows/test.yml/badge.svg)](https://github.com/keygen-sh/py-machineid/actions)
[![PyPI version](https://badge.fury.io/py/py-machineid.svg)](https://badge.fury.io/py/py-machineid)

Get the unique machine ID of any host (without admin privileges).

Sponsored by:

<a href="https://keygen.sh?ref=typed_params">
  <div>
    <img src="https://keygen.sh/images/logo-pill.png" width="200" alt="Keygen">
  </div>
</a>

_An open, source-available software licensing and distribution API._

## Install

Install using [`pip`](https://docs.python.org/3/installing/index.html):

```bash
python3 -m pip install py-machineid
```

## Usage

To obtain the raw GUID of the device, use `id() -> str`:

```python
import machineid

print(machineid.id())
```

To obtain an anonymized (hashed) version of the GUID, see below. The
`hashed_id(str) -> str` function takes an optional application ID,
which will ensure a unique ID per-app for the same device.

```python
import machineid

print(machineid.hashed_id('myappid'))
print(machineid.hashed_id())
```

## Thanks

Special thanks to Denis Brodbeck for his Go package, [`machineid`](https://github.com/denisbrodbeck/machineid).
