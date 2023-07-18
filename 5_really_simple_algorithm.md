The name feels like a hint for RSA.  
The numbers given `{129834683, 10529980290229}` seem like `e` and `n` respectively.  
If we take the whole message to be a single number `c` (and ignore the spaces), it looks like we went a wrong way as `n > c` should hold.  
But if we take the individual numbers in the message to be `c`, we get back on the right track.

A lookup on factorDB shows that the number `10529980290229` has two prime factors `5929487` and `1775867`. So it's definitely `n`.

Creating a RSA public key from `n` and `e` using (RsaCtfTool)[https://github.com/RsaCtfTool/RsaCtfTool], and by printing the private key we get:
```
-----BEGIN RSA PRIVATE KEY-----
MDICAQACBgmTs7wUtQIEB70euwIGBHv4Aa07AgNaeg8CAxsY+wIDIMt7AgMJg8EC
AzIwuA==
-----END RSA PRIVATE KEY-----
```

Extracting the values, we get `d` as `4930488347963`. And by using `n` and `d` we can decrypt the `c` one by one:  
`d3cipher_m3_if_y0u_can`

Final flag:  
`CTF{d3cipher_m3_if_y0u_can}`
