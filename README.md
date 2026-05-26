# pnum — Integer Analysis CLI

**pnum** is a command-line integer analysis tool written in [Vix](https://github.com/vixlang/Vix-lang). It provides quick number-theoretic insights such as primality testing, prime factorization, Collatz sequence enumeration, and prime listing.

## Features

| Feature        | Description                                              |
|----------------|----------------------------------------------------------|
| Parity check   | Determines whether a number is even or odd               |
| Primality test | Trial division up to √n                                  |
| Factorization  | Produces output in `2 × 2 × 3 × 7` format                |
| Collatz seq.   | Computes the 3n+1 sequence and reports step count        |
| Prime table    | Lists all primes ≤ n                                     |

## Usage

```bash
./pnum <positive-integer>
```

Pass no arguments to display a help message.

### Examples

```bash
$ ./pnum 97
╔══════════════════════╗
║  pnum v0.1           ║
╚══════════════════════╝

■ Number   : 97
■ Parity   : 0/1
  (odd)
■ Is prime : yes ✓
■ Factors  : 1 × 97 (prime)

■ Collatz sequence:
   97 → 292 → ... → 1 (118 steps)
■ Primes ≤ 97 : ... (total: 25)

$ ./pnum 84
■ Is prime : no ✗
■ Factors  :
   2 × 2 × 3 × 7
```

## Build from Source

```bash
vixc primex.vix -o pnum
```

## Dependencies

- Vix compiler (`vixc`) — must be built and available under `src/`
- C runtime library (linked for `printf`, `atoi`)

## License

Apache-2.0
