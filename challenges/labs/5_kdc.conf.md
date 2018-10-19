````
[kdcdefaults]
 kdc_ports = 88
 kdc_tcp_ports = 88

[realms]
 GMSPINHEIRO.SG = {
  master_key_type = aes256-cts-hmac-sha1-96
  acl_file = /var/kerberos/krb5kdc/kadm5.acl
  dict_file = /usr/share/dict/words
  admin_keytab = /var/kerberos/krb5kdc/kadm5.keytab
  supported_enctypes = aes256-cts:normal
  max_life = 1d
  max_renewable_life = 7d
  renewable = true
 }

````
