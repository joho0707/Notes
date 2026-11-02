# Number Theory

- **Integers** - positive or negative whole numbers
- **Factors** - 2 or more numbers multiplied together
- **Product** - the outcome of numbers multiplied together

*Every integer has at least two factors*

**Prime** *integers only have 1 and itself*

**Primes** - { 2, 3, 5, 7, 11, 13, 17, 19... }

## Prime Factorisation

*Write any integer as a product of its prime factors*

eg.

$$
231 = 33 \times 7
$$

$$
231 = 3 \times 11 \times 7
$$

$$
231 = 3 \times 7 \times 11
$$

eg.

$$
720 = 90 \times 8
$$

$$
720 = 9 \times 10 \times 4 \times 2
$$

$$720 = 3 \times 3 \times 5 \times 2 \times 2 \times 2 \times 2$$
$$720 = 2^{4} \times 3^{2} \times 5$$

### Euclidian Algorithm

#### Part 1 - using successive division to find GCD between two integers

*More efficient way of finding gcd/lcm - doesn't involve prime factorisation*

Given 2 integers: $a$ and $b$, where $a > b$, we write them as follows:

$$
a = (b) + r
$$

eg:

$$
98 = 4(24) + 2
$$

$$
a = q(b) + r
$$

- where $q$ = **quotient**, which is how many times $b$ divides into $a$
- and $r$ = **remainder**, which is the difference between the quotient

eg. Use Euclid's Algorithm to find gcd(42823, 6409)

$$
42823 = 6(6409) + 4369
$$

$$
6409 = 1(4369) + 2040
$$

$$
4369 = 2(2040) + 289
$$

$$
2040 = 7(289) = 17
$$

$$
289 = 17(17) + 0
$$

**Last non-zero remainder is gcd** - in this case is *17*

Eg. Use Euclid's Algorithm to find gcd(7469, 2464)

$$
7469 = 3(2464) + 77
$$

$$
2464 = 32(77) + 0
$$

$$
gcd = 77
$$

eg. Use Euclid's Algorithm to find gcd(2689, 4001)

$$
4001 = 1(2689) + 1312
$$

$$
2689 = 2(1312) + 65
$$

$$
1312 = 20(65) + 12
$$

$$
65 = 5(12) + 5
$$

$$
12 = 2(5) + 2
$$

$$
5 = 2(2) + 1
$$

$$
gcd = 1
$$

#### Part 2 (Bezoút's Theorem) - find two other integers (x and y)

$$
ax + by = \gcd(a,b)
$$

## Modular Number Systems

### Multiplicative Inverse

$$
a^{-1}
$$

### Fermet's Little Theorem

where $p$ is a prime number,

$$
a^{-1} \equiv a^{p-2} \pmod{p}
$$

eg.

$$
3^{-1} \equiv 3^{5-2} \pmod{5}
$$

$$
\equiv 27 \pmod{5}
$$

$$
\equiv 2
$$
