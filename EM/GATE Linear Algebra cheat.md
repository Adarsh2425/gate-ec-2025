🔥 **Ultimate GATE Linear Algebra Cheat Sheet** 🔥

This cheat sheet covers *everything*: matrix types, properties, crucial concepts, solution techniques, and shortcuts, all in a concise format for quick revision.

📌 **1. Vector Spaces & Subspaces**

*   **Subspace Check (3 Conditions):**
    1.  Zero vector (`0`) is in the subspace.
    2.  Closed under addition (`u, v ∈ W  =>  u + v ∈ W`).
    3.  Closed under scalar multiplication (`c ∈ F, v ∈ W  =>  cv ∈ W`).
*   **Basis:** Linearly independent set that spans the vector space.
*   **Dimension:** Number of vectors in a basis.
*   **Finding a Basis:**  Row reduce the matrix of vectors; pivot columns in the *original* matrix form a basis for the column space, and the non-zero rows of the reduced form a basis for the row space.
*   **Rank-Nullity Theorem:** `rank(A) + nullity(A) = number of columns of A`

📌 **2. Linear Independence & Dependence**

*   **Independent:**  `c₁v₁ + c₂v₂ + ... + cₙvₙ = 0` *only* if all `cᵢ = 0`.
*   **Dependent:**  A non-trivial solution exists (some `cᵢ ≠ 0`).
*   **Shortcuts:**
    *   `det(A) ≠ 0` → Independent columns (for square matrices).
    *   `det(A) = 0` → Dependent columns (for square matrices).
    *   More vectors than dimension → Dependent.
    *   Set contains zero vector → Dependent.
    * Row reduce. If No Free variable → Independent.

📌 **3. Matrices: Types & Properties**

| Type              | Definition                | Properties                                                                                                                                      | Eigenvalues                                  | Determinant                    | Other                               |
| ----------------- | ------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------- | ------------------------------ | ----------------------------------- |
| Square            | `n x n`                  |                                                                                                                                                 |                                               |                                |                                     |
| Diagonal          | Non-diagonal = 0          | `Aⁿ` = (diagonals raised to n)                                                                                                                | Diagonal elements                           | Product of diagonal elements   |                                     |
| Identity (I)      | Diagonal = 1, others = 0  | `AI = IA = A`                                                                                                                                  | All 1s                                        | 1                              |                                     |
| Zero (0)        | All elements = 0          |                                                                                                                                           |  All 0s                                    |0                                  |          |
| Symmetric         | `Aᵀ = A`                 | Eigenvectors for distinct eigenvalues are orthogonal; diagonalizable                                                                           | Real                                          |                                |                                     |
| Skew-Symmetric    | `Aᵀ = -A`                | Diagonal elements are 0                                                                                                                         | 0 or purely imaginary                        | 0 (if odd order),  >=0 (even order)| `A²` is symmetric                 |
| Orthogonal        | `AᵀA = AAᵀ = I`          | `A⁻¹ = Aᵀ`; preserves lengths and angles; rows/cols are orthonormal                                                                               | Magnitude 1 (±1 if real)                    | ±1                             |                                     |
| Upper Triangular  | Below diagonal = 0       |                                                                                                                                                 | Diagonal elements                           | Product of diagonal elements   |                                     |
| Lower Triangular  | Above diagonal = 0       |                                                                                                                                                 | Diagonal elements                           | Product of diagonal elements   |                                     |
| Idempotent        | `A² = A`                 |                                                                                                                                                 | 0 or 1                                        |                                |                                     |
| Nilpotent         | `Aᵏ = 0` for some `k`     |                                                                                                                                                 | All 0s                                        | 0                              |                                     |
| Involutory        | `A² = I`                 |                                                                                                                                                  | +1 or -1                                         |                     |         |
|Singular           |                           |                                                                                                                                          |At least one zero                               |0  |  Not Invertible                    |
|Non-Singular       |                           |                                                                                                                                    |   None Zero                                   |Non-Zero      |      Invertible               |
| Hermitian        | `A = Aᴴ`                | Generalization of symmetric to complex matrices.                                                                                                 | Real                                      |                                    |
| Unitary     |`AᴴA = I`           | Generalization of orthogonal to complex matrices.                                                      | Magnitude 1                         | |det(A)| = 1               |                                              |

*  `Aᴴ` is the conjugate transpose

📌 **4. Matrix Operations & Properties**

*   **(AB)ᵀ = BᵀAᵀ**
*   **(A⁻¹)ᵀ = (Aᵀ)⁻¹**
*   `det(AB) = det(A)det(B)`
*   `det(Aᵀ) = det(A)`
*   `det(cA) = cⁿdet(A)`  (`A` is `n x n`)
*   `det(A⁻¹) = 1/det(A)`
*   `tr(A + B) = tr(A) + tr(B)`
*   `tr(cA) = c tr(A)`
*   `tr(AB) = tr(BA)`
*    Cayley-Hamilton Theorem

📌 **5. Determinants**

*   **2x2:** `det([[a, b], [c, d]]) = ad - bc`
*   **Triangular Matrix:** Determinant = product of diagonal entries.
*   **Row/Column Operations:**
    *   Swapping rows/columns: Changes sign.
    *   Multiplying row/column by `k`: Multiplies determinant by `k`.
    *   Adding multiple of row/column to another: *No change*.
*  **Zero Row/Column or Identical Rows/Columns:** Determinant = 0

📌 **6. Eigenvalues & Eigenvectors**

*   **Definition:** `Av = λv` (`v` is non-zero)
*   **Characteristic Equation:** `det(A - λI) = 0`
*   **Finding Eigenvectors:** Solve `(A - λI)v = 0` for each `λ`.
*   **Properties:**
    *   Sum of eigenvalues = `tr(A)` (Trace)
    *   Product of eigenvalues = `det(A)`
    *   Triangular matrix: Eigenvalues are diagonal entries.
    *   Symmetric matrix: Eigenvalues are real; eigenvectors for distinct eigenvalues are orthogonal.
    *  If `λ` is eigenvalue of A, and k is any number then `λ` + k is eigenvalue of `A+kI`
    * Similar Matrices have same eigen values.

📌 **7. Rank & Nullity**

*   **Rank:** Number of linearly independent rows/columns.  Number of non-zero rows in REF.
*   **Nullity:** Dimension of null space (solutions to `Ax = 0`).  Number of free variables.

📌 **8. Systems of Linear Equations (Ax = b)**

*   **Existence:** Solution exists if and only if `rank(A) = rank([A | b])`.
*   **Uniqueness:**
    *   **Unique:** `rank(A) = rank([A | b]) = n` (number of unknowns)
    *   **Infinite:** `rank(A) = rank([A | b]) < n`
    *   **No Solution:** `rank(A) < rank([A | b])`
*   **Homogeneous System (Ax = 0):**
    *   Always has trivial solution (`x = 0`).
    *   Non-trivial solutions exist if `rank(A) < n`  (or `det(A) = 0` for square `A`).
*   **Solving Methods:**
    *   Gaussian Elimination (Row Reduction)
    *   Cramer's Rule (for unique solutions, `xᵢ = det(Aᵢ)/det(A)`)
    *   LU Decomposition (`A = LU`, then solve `Ly = b` and `Ux = y`)
* **Challenging Concepts:**
Pseudoinverse:

📌 **9. Solving Techniques (Step-by-Step)**

*   **Linear Independence:**
    1.  Form matrix with vectors as columns.
    2.  Row reduce.
    3.  No free variables → Independent. Free variables → Dependent.  OR: `det(A) ≠ 0` → Independent (for square matrices).
*   **Finding a Basis:**
    1.  Form matrix with vectors.
    2.  Row reduce to REF.
    3. Pivot columns will give you basis.
*   **Finding Rank:**
    1.  Row reduce to REF.
    2.  Count non-zero rows.
*   **Solving Ax = b:**
    1.  Form augmented matrix `[A | b]`.
    2.  Row reduce to REF or RREF.
    3.  Check for consistency (`rank(A) = rank([A | b])`).
    4.  Back-substitution (if REF) or read off solution (if RREF).
*   **Finding Eigenvalues:**
    1.  Solve `det(A - λI) = 0`.
*   **Finding Eigenvectors:**
    1.  For each `λ`, solve `(A - λI)v = 0`.

🚀 **GATE Super Shortcuts**

1.  **Orthogonal Matrix:** `A⁻¹ = Aᵀ`
2.  **Triangular Matrix:** Eigenvalues are on the diagonal; determinant is the product of the diagonal.
3.  **Symmetric Matrix:** Eigenvalues are real; eigenvectors for distinct eigenvalues are orthogonal.
4.  **Idempotent (A² = A):** Eigenvalues are 0 or 1.
5.  **Nilpotent (Aᵏ = 0):** All eigenvalues are 0.
6.  **Trace = Sum of Eigenvalues;  Determinant = Product of Eigenvalues**
7.  **Rank-Nullity Theorem:**  Use it to quickly find one if you know the other.
8.  **Cayley-Hamilton:**  Every square matrix satisfies its own characteristic equation.
9.  **Involutory (A² = I)**: Eigenvalues will be +1 and -1.
10. **Singular Matrix:** Determinant Zero and Eigenvalue also Zero.

This is the *ultimate* cheat sheet. Master this, and you'll be incredibly well-prepared for GATE Linear Algebra!
