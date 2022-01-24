# BOF

Using gdb-peda, found pattern offset at 52 (dereferenced as `$ebp+8`)
Then we just construct our poc script, and run it with:

```sh
cat input.txt - | nc pwnable.kr 9000
```
