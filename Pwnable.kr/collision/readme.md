# Collision

We see that the number is `0x21DD09EC`, converting this to decimal is `568134124`. Further,
we see that there are 5 integers in the input which get added together. So we need 5 numbers which add to `568134124`.
Using a quick online calculator gives us:

```sh
137822778 * 4 + 16843012
```

So converting those numbers to hex:

```sh
0x837023A * 4 + 0x01010104
```

now finalizing the payload (remember that we need to write each 4-byte int in reverse order due to little endian):

```sh
./col `python -c "print('\x04\x01\x01\x01' + '\x3A\x02\x37\x08' * 4)"`
# daddy! I just managed to create a hash collision :)
```
