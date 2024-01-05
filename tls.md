# tls1.2

# tls1.3

# dtls
the underlying is udp

# ja3
## how to calculate
### 1. see the rust source code

### 2. split the tls key word

Transport Layer Security
TLSv1.2 Record Layer: Handshake Protocol: Client Hello
Handshake Protocol: Client Hello

all reserved could be ignored.
#### 2.1
Version: TLS 1.2 (0x0303)

#### 2.2
Cipher Suites (16 suites)

#### 2.3 All extention type.
Extension: Reserved (GREASE) (len=0)(ignore)
Extension: key_share (len=43)
Type: key_share (51)

#### 2.4 belongs to an extension type
Extension: supported_groups (len=10)
Supported Group: x25519 (0x001d)

#### 2.5 belongs to an extension type
Extension: ec_point_formats (len=2)