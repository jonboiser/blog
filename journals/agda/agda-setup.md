# Agda setup

## Compiler and tools

Install with Homebrew

```
brew install agda
```

Install Atom packages

```
apm install language-agda agda-mode
```

## Toy problem

From http://learnyouanagda.liamoc.net/pages/peano.html

```agda
module peano where

-- \bn for ℕ and \-> for →
data ℕ : Set where
  zero : ℕ
  suc : ℕ → ℕ

-- Function with holes
_+_ : ℕ → ℕ → ℕ
zero + zero = zero
zero + n = n
(suc n) + n′ = suc (n + n′)

-- C-c C-l to load
-- C-c C-n to reduce to normal form
(suc (suc (suc zero))) + (suc (suc zero))
-- == (suc (suc (suc zero))) + (suc (suc zero))
```
