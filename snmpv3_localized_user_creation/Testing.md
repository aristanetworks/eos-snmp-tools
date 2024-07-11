# Testing
RFC2574 says

## A.3.1
```
A.3.1.  Password to Key Sample Results using MD5

   The following shows a sample output of the password to key algorithm
   for a 16-octet key using MD5.

   With a password of "maplesyrup" the output of the password to key
   algorithm before the key is localized with the SNMP engine's
   snmpEngineID is:

      '9f af 32 83 88 4e 92 83 4e bc 98 47 d8 ed d9 63'H

   After the intermediate key (shown above) is localized with the
   snmpEngineID value of:

      '00 00 00 00 00 00 00 00 00 00 00 02'H

   the final output of the password to key algorithm is:

      '52 6f 5e ed 9f cc e2 6f 89 64 c2 93 07 87 d8 2b'H
```

```
prompt> v3localize maplesyrup md5 000000000000000000000002
526f5eed9fcce26f8964c2930787d82b
```

## A.3.2
```
A.3.2.  Password to Key Sample Results using SHA

      The following shows a sample output of the password to key
      algorithm for a 20-octet key using SHA.

      With a password of "maplesyrup" the output of the password to key
      algorithm before the key is localized with the SNMP engine's
      snmpEngineID is:

      '9f b5 cc 03 81 49 7b 37 93 52 89 39 ff 78 8d 5d 79 14 52 11'H

   After the intermediate key (shown above) is localized with the
   snmpEngineID value of:

      '00 00 00 00 00 00 00 00 00 00 00 02'H

   the final output of the password to key algorithm is:

      '66 95 fe bc 92 88 e3 62 82 23 5f c7 15 1f 12 84 97 b3 8f 3f'H
```

```
prompt> v3localize maplesyrup sha 000000000000000000000002
6695febc9288e36282235fc7151f128497b38f3f
```