# Install
pip install git+https://github.com/Airead/yescrypt-hash-python

# Test
```python
import yescrypt_hash
expected = '00000000fb7bf19efdaf25b5e31bd9caf785cf418bdcad4f5f18cddd3f4aaeef'
header = bytes.fromhex('240a5a20727df120f94999fd6e1df9a0dee583541e829597090ccaa5573b33b89f19121dbab36a503dfea48d17a160d100a78187ee80cf8ffd027bed3e82d03aa11e2d59da1cbc5ba79d011d00000a78')
powhash = yescrypt_hash.getHash(header, len(header))[::-1]
print(powhash)
print(bytes.fromhex(expected) == powhash)
```

> copy from https://github.com/amarian12/p2pool-bsty
