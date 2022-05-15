# OpenVpn

- install openvpn and easy-rsa
- mkdir ~/easy-rsa
- ln -s /usr/share/easy-rsa/* ~/easy-rsa/
- go to this path: /usr/share/easy-rsa
- make a copy of vars.example and rename it to vars
- run this command: ./easyrsa init-pki
- run: ./easyrsa gen-dh
- commnet /usr/share/easy-rsa/pki/openssl-easyrsa.cnf (line: RANDFILE               = $ENV::EASYRSA_PKI/.rnd)
- run: ./easyrsa build-ca   (senha: bzUpfKdi)
