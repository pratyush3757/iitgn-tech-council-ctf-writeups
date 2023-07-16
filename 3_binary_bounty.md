Running `strings find_flag` shows:  
```
The flagH
 doesn'tH
 seem soH
 easily H
sily obtH
ainable
CTF{1mm4H
_h4ck3rmH
h4ck3rm4H
nn_n0w}
enter the passphrase: 
superstrongpassword
```

The flag isn't accepted as is, but on running the executable, we are prompted for a passphrase.  
Entering `superstrongpassword` gives the output:  
`CTF{1mm4_h4ck3rm4nn_n0w}`

