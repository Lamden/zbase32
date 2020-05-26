# zbase32
The simplest library for turning bytes into zbase32 human readable format.

```
# Random data
b = b'\xcd_\xf0g\xa6\xc9o\xb2\x93os\x86\xbc\x81\xb9@6\xd8\xc1\x86f\x04\x1a\xa3o/\xe2F\x9e*8\x9c'

# as hex
b.hex()
>>> cd5ff067a6c96fb2936f7386bc81b94036d8c18666041aa36f2fe2469e2a389c

# as base32
import base64
base64.b32encode(b)
>>> b'JGRM7LDPCCTTSQB62CJXRQEHOFKGWSTIJ3W7AYCNOUDGVV2PAFJQ===='

# as HUMAN READABLE ZBASE32
import zbase32
zbase32.bytes_to_zbase32(b)
>>> tqkotxh5t8z8dz7aaihxey5qoizuw5hywgmw6j99yr7e4i3bemby====
```

Amazing.

Super good for turning ugly data into pretty data.

```
# lame
public_key = '88b0fdb5b079675ce0c40c3825d0aae5b3e8c353a408d5261611f846c526a3c9'

# way cool
public_key = bytes.fromhex(public_key)
public_key = zbase32.bytes_to_zbase32(public_key)
'pub_{}'.format(public_key[:-4])

>>> pub_tnax5ppoxfui3agrbohnmwfkhs36to4uworpkjosn8hrptjgwxro
