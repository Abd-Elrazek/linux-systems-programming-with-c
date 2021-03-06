# bit manipulations

The AND \(&\), OR \(\|\), XOR \(^\), Negate \(~\), Not \(!\) and bit shifts \(&lt;&lt; and &gt;&gt;\) operations are possible in C.

### AND operation

The AND operation is used to test if the bit is set or unset. A set is called a 1 and unset or clear is called a 0.

For example consider the following number 128 \(in hex 0x80\).

lets,

```c
a = 0x80
MSBit_set = !!(a & 0x80)
if (MSBit_set)
    printf("MSBit is set\n");
else
    printf("MSBit is not set\n");
```

### NOT operaton

The above program tests if the Most significant bit \(MSbit\) of the variable a is set. The test is performed with a mask 0x80. The two Not \(!\) operators have the following purpose. The Not operator first inverts the value. If the value is not zero, it inverts it into 0 and if the value is 0, it inverts into 1. A Not operation that is performed twice would only give either 1 or 0 only.

Ex: if the Not operation performed on 12, !12 would give 0. and a Not operation again on 0 would give us 1. that is the Not operation results in a binary value. Thus if a value that is non-zero, a twice Not operator would make it 1. If the value that is zero, a twice Not operator would make it 0.

### OR operation

An OR operation is used mostly to add or set bits into a byte or group of bytes. Let us take the below example

```c
uint8_t var = 0;

var |= 0x01;

printf("0x%02x\n", var);

var |= 0x02;

printf("0x%02x\n", var);

```

The second statement `var |= 0x01` would set 1 in the 0'th bit of the byte 0.
When the third statement is executed it prints the value 0x1.

The bit representation would look as follows.

`00000001`

The fourth statement `var |= 0x02` would set 1 in the 1'st bit of the byte 1.
It does not change any other bits except the 1st bit. When the fifth statement is executed it prints the value 0x3.

The bit representation would look as follows.

`00000011`

### XOR operation

The XOR operation uses the `^`. The operation looks as below...

| Bit 1 | Bit 2 | result |
| :--- | :--- | :--- |
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

The `Bit 1` is `XOR`'ed with `Bit 2` to give out the result.

When both bits are same the result is a `0`.

When both bits are not same the result is `1`.

For ex:

```c
a = 10, b = 5;

printf("value %d\n", a ^ b);

```

### Left shift operation

The left shift operation uses `<<`. 

### Right shift operation

The right shift operation uses '>>'.

### Negate opertaion

The computer stores the digits in binary form unlike we use them either in decimal or hexadecimal.

This is called the base of a number. The binary number is in base 2, decimal is base 10 and hexadecimal is base 16.

