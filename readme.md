# Chess Engine with FEN Support

This Chess implementation was developed on macOS.
The project is built on top of the starter framework provided by UCSC CMPM 123.

## FEN Support and Features

### FEN-Based Board Initialization

The chess engine supports initializing the board from Forsyth-Edwards Notation (FEN) strings.

Supported input formats:

1. Piece placement only

```cpp
FENtoBoard("rnbqkbnr/pppppppp/8/8/8/8/PPPPPPPP/RNBQKBNR");
```

2. Full FEN string

```cpp
FENtoBoard("rnbqkbnr/pppppppp/8/8/8/8/PPPPPPPP/RNBQKBNR w KQkq - 0 1");
```

Only the first (piece placement) field is required for board setup.
Full FEN strings are safely accepted by parsing the first field and ignoring the rest.

## Implemented Functionality

### Board Parsing

- Parses 8 ranks separated by `/`
- Interprets numeric characters as consecutive empty squares
- Supports all standard chess pieces:
  - `P` / `p` pawn
  - `N` / `n` knight
  - `B` / `b` bishop
  - `R` / `r` rook
  - `Q` / `q` queen
  - `K` / `k` king
- Uppercase letters represent white pieces
- Lowercase letters represent black pieces

### Automatic Piece Creation
### Board Reset Safety

---

## Building and run

Build using CMake:

```bash
cd build
cmake ..
make
./demo
```
