---
created_at: "2026-04-29T22:41:39-04:00"
updated_at: "2026-05-01T23:45:36-04:00"
generated_by: "unknown_llm"
timestamp_source: "filesystem_birthtime"
---

# Algebraic topology and symplectic geometry for Chern--Simons theory and TQFT

This note is meant to sit near the beginning of a review on Chern--Simons theory, anomaly inflow, and topological quantum field theory. It is written in a deliberately mathematical style, but with the physics target always kept in view. The central principle is that in low-dimensional quantum field theory the *global* structure of fields matters as much as, and often more than, the local differential equations. One therefore needs a toolkit that combines homotopy, homology and cohomology, bundles and characteristic classes, holonomy and flat connections, and symplectic reduction. The exposition below is built from standard references in algebraic topology, bundle theory, symplectic geometry, holonomy, Lie groups, and TQFT.[^1][^2][^3][^4][^5][^6][^7][^8][^9][^10][^11][^12]

## 1. Why topology enters TQFT at all

A local Lagrangian density is built from fields and finitely many derivatives. But a topological field theory is not primarily sensitive to local metric data. Its observables are designed to depend only on the topology of the underlying manifold and on global data carried by the fields. This immediately forces certain mathematical structures onto the stage.

1. If a gauge field is flat, then locally it is pure gauge, but globally it may still have nontrivial holonomy. Thus one must understand loops up to homotopy.
2. If one wants to classify topological sectors of bundles, one needs characteristic classes and classifying spaces.
3. If one wants to quantize the moduli space of flat connections on a surface, one needs symplectic geometry and symplectic reduction.
4. If one wants a functorial description of TQFT, one needs bordism categories and symmetric monoidal functors.

In other words, the topology is not an optional refinement. It is the language in which the universal content of the theory is naturally stated.

---

## 2. Topological preliminaries

We begin at the level of topological spaces.

A **topological space** $X$ is a set together with a collection of open subsets satisfying the usual axioms. A **continuous map** $f : X \to Y$ is a set map that pulls back open sets in $Y$ to open sets in $X$.

The two equivalence relations that matter most in TQFT are:

- **homeomorphism**: sameness of topology,
- **homotopy equivalence**: sameness of topology up to continuous deformation.

A pair of maps
$$
f : X \to Y,
\qquad
g : Y \to X
$$
is a homotopy equivalence if
$$
g \circ f \simeq \operatorname{id}_X,
\qquad
f \circ g \simeq \operatorname{id}_Y,
$$
where $\simeq$ means homotopic. The basic principle of algebraic topology is that useful invariants should be invariant under homotopy equivalence, since many spaces that arise in geometry are most naturally described only up to deformation.[^1]

A **homotopy** between maps $f_0,f_1 : X \to Y$ is a continuous map
$$
H : X \times [0,1] \to Y
$$
with
$$
H(x,0)=f_0(x),
\qquad
H(x,1)=f_1(x).
$$
Thus homotopy means continuous deformation through maps.

Two classes of spaces occur constantly:

- **CW complexes**, which are built inductively by attaching cells,
- **smooth manifolds**, which are the spaces on which differential forms and bundles live.

For most topological questions in field theory, one passes freely between smooth manifolds and the homotopy type of a CW complex. This is one reason algebraic topology and differential topology constantly interact in gauge theory.[^1][^2][^3]

### 2.1. Manifolds and orientation

An $n$-dimensional smooth manifold $M$ is a Hausdorff, second countable topological space that is locally diffeomorphic to $\mathbb{R}^n$.

An **orientation** on $M$ is a consistent choice of orientation on tangent spaces $T_pM$. Equivalently, it is a nowhere-vanishing top-degree form defined up to multiplication by a positive function. Orientation matters because integration, intersection numbers, Poincaré duality, and the sign conventions in Chern--Simons theory all depend on it.[^2][^3]

---

## 3. Paths, loops, and the fundamental group

The first global invariant one meets is the fundamental group.

A **path** in $X$ from $x_0$ to $x_1$ is a continuous map
$$
\gamma : [0,1] \to X,
\qquad
\gamma(0)=x_0,
\quad
\gamma(1)=x_1.
$$
A **loop** based at $x_0$ is a path with $x_1=x_0$.

Two based loops $\gamma_0,\gamma_1$ are **homotopic rel endpoints** if there is a homotopy through loops keeping the endpoints fixed. The set of based homotopy classes of loops is denoted
$$
\pi_1(X,x_0).
$$
The group operation is concatenation:
$$
[\gamma_1] \cdot [\gamma_2] = [\gamma_1 * \gamma_2],
$$
with $\gamma_1 * \gamma_2$ defined by running first $\gamma_1$ and then $\gamma_2$.

One must check three things:

1. concatenation respects homotopy classes,
2. the constant loop is the identity,
3. the reverse loop $\overline\gamma(t)=\gamma(1-t)$ gives the inverse.

Associativity is true only up to reparametrization on the nose, but up to homotopy it becomes strictly associative. Thus $\pi_1(X,x_0)$ is a group.[^1]

### 3.1. Why $\pi_1$ matters in gauge theory

If $A$ is a flat connection, the gauge-invariant information carried by $A$ is encoded by parallel transport around loops. Because curvature vanishes, this transport depends only on the homotopy class of the loop. Therefore flat gauge fields naturally define representations of the fundamental group. This is the basic bridge between topology and gauge theory.

### 3.2. Computation of $\pi_1(S^1)$

Let us derive the most important example explicitly.

Consider the universal covering map
$$
p : \mathbb{R} \to S^1,
\qquad
p(t)=e^{2\pi i t}.
$$
A loop
$$
\gamma : [0,1] \to S^1,
\qquad
\gamma(0)=\gamma(1)=1
$$
can be uniquely lifted to a path
$$
\widetilde\gamma : [0,1] \to \mathbb{R}
$$
with $\widetilde\gamma(0)=0$. Since $p(\widetilde\gamma(1))=1$, the endpoint $\widetilde\gamma(1)$ must be an integer. Define
$$
\deg(\gamma)=\widetilde\gamma(1) \in \mathbb{Z}.
$$
This integer is the winding number.

Now:

- homotopic loops lift to homotopic paths with the same endpoint,
- concatenation adds endpoints,
- every integer occurs.

Hence the degree map induces an isomorphism
$$
\pi_1(S^1) \cong \mathbb{Z}.
$$
This is the model for almost every later argument involving winding, monodromy, and level quantization.[^1]

### 3.3. Computation of $\pi_1(T^2)$

Write the torus as
$$
T^2 = S^1 \times S^1.
$$
Since the fundamental group of a product is the product of the fundamental groups,
$$
\pi_1(T^2) \cong \pi_1(S^1) \times \pi_1(S^1) \cong \mathbb{Z}^2.
$$
Geometrically, the two generators are the meridian and longitude. A flat abelian connection on the torus is therefore controlled by its two holonomies around these two cycles.

### 3.4. Van Kampen's theorem

The main computational theorem for $\pi_1$ is van Kampen's theorem. In its simplest form, if
$$
X = U \cup V
$$
with $U,V,U\cap V$ path connected and with a common basepoint, then $\pi_1(X)$ is the pushout
$$
\pi_1(X) \cong \pi_1(U) *_{\pi_1(U\cap V)} \pi_1(V).
$$
This is the correct topological analogue of gluing local data. Whenever one cuts a manifold into pieces and then studies gauge fields or states under gluing, one is using the same philosophy at a more sophisticated level.[^1]

---

## 4. Higher homotopy groups

The fundamental group records loops. Higher homotopy groups record maps of higher spheres.

For $n \ge 1$, define
$$
\pi_n(X,x_0) = [ (S^n,s_0),(X,x_0) ],
$$
namely based homotopy classes of maps from the $n$-sphere into $X$.[^1]

For $n=1$ this recovers the fundamental group. For $n>1$, one proves that $\pi_n(X,x_0)$ is abelian. The reason is geometric: concatenation in different directions can be slid past one another. This is the Eckmann--Hilton phenomenon.

### 4.1. Why higher homotopy matters in Chern--Simons theory

In Chern--Simons theory one meets the integer
$$
\int_M \operatorname{tr}(g^{-1}dg)^{\wedge 3},
$$
where $g : M^3 \to G$. On a closed oriented $3$-manifold, this is controlled by the homotopy class of the map $g$. Thus the relevant topology is $\pi_3(G)$, not $\pi_1(G)$. For compact simple simply connected groups such as $SU(N)$, one has
$$
\pi_3(G) \cong \mathbb{Z},
$$
which is exactly why the Chern--Simons level is quantized by an integer.[^12]

### 4.2. Long exact sequence of a fibration

If
$$
F \hookrightarrow E \xrightarrow{p} B
$$
is a fibration, then there is a long exact sequence
$$
\cdots \to \pi_n(F) \to \pi_n(E) \to \pi_n(B)
\xrightarrow{\partial}
\pi_{n-1}(F) \to \cdots \to \pi_0(B).
$$
This exact sequence is one of the main engines for computing homotopy groups.[^3]

A basic application is the fibration
$$
SU(n-1) \hookrightarrow SU(n) \to S^{2n-1},
$$
where the map sends a matrix to its first column. Since the fiber over a unit vector is the subgroup preserving that vector, namely $SU(n-1)$, one obtains inductive information about the homotopy groups of $SU(n)$.

Because
$$
\pi_3(S^{2n-1})=0 \qquad (n\ge 3),
$$
this fibration implies that
$$
\pi_3(SU(n-1)) \xrightarrow{\sim} \pi_3(SU(n))
$$
for $n\ge 3$. Hence once one knows $\pi_3(SU(2))=\mathbb{Z}$, it follows by induction that
$$
\pi_3(SU(n)) \cong \mathbb{Z}
\qquad
(n\ge 2).
$$
This is the exact topological statement underlying the winding-number formula in nonabelian Chern--Simons theory.[^3][^12]

---

## 5. Covering spaces, bundles, and classifying data

A **covering map**
$$
p : \widetilde X \to X
$$
is a continuous surjection such that every point of $X$ has a neighborhood $U$ for which
$$
p^{-1}(U)
$$
is a disjoint union of open sets, each mapped homeomorphically onto $U$.

The simplest example is
$$
\mathbb{R} \to S^1,
\qquad
t \mapsto e^{2\pi i t}.
$$
The universal cover of a connected, locally path connected, semilocally simply connected space $X$ is a simply connected cover $\widetilde X \to X$, and deck transformations are naturally identified with $\pi_1(X)$.[^1]

This already hints at a general principle: global topology is often encoded by local triviality together with nontrivial gluing.

### 5.1. Fiber bundles

A **fiber bundle** with fiber $F$ is a map
$$
\pi : E \to B
$$
which is locally trivial, meaning that every $b \in B$ has a neighborhood $U$ for which
$$
\pi^{-1}(U) \cong U \times F
$$
compatibly with projection to $U$.[^3]

Important special cases are:

- vector bundles,
- principal $G$-bundles,
- associated bundles to principal bundles.

A **principal $G$-bundle**
$$
G \hookrightarrow P \to B
$$
is a bundle whose fiber is the group $G$, together with a free right $G$-action on $P$ that is simply transitive on fibers.

The gauge fields in Yang--Mills and Chern--Simons theory are connections on principal bundles, not merely Lie-algebra valued one-forms on trivial bundles. The distinction matters globally.

### 5.2. Transition functions and Čech viewpoint

On an open cover $\{U_i\}$ of $B$, a principal $G$-bundle can be described by transition functions
$$
g_{ij} : U_i \cap U_j \to G
$$
satisfying the cocycle condition
$$
g_{ij} g_{jk} g_{ki} = e
$$
on triple overlaps. Different choices related by local redefinitions give isomorphic bundles. Thus bundle classes are represented by Čech $1$-cocycles with values in $G$.[^3]

This cocycle viewpoint is often the fastest route to seeing why global topological classes appear in gauge theory.

### 5.3. Classifying spaces

For a topological group $G$, principal $G$-bundles over a reasonable space $X$ are classified by homotopy classes of maps
$$
[X,BG],
$$
where $BG$ is the classifying space of $G$. Concretely, there is a universal principal bundle
$$
EG \to BG,
$$
and every principal $G$-bundle over $X$ is pulled back from this universal one by a classifying map
$$
f : X \to BG.
$$
This is conceptually crucial: topological sectors of gauge fields are encoded by homotopy classes of maps into a universal target.[^3]

---

## 6. Homology, cohomology, and de Rham theory

Homotopy groups are subtle and hard to compute. Homology and cohomology are more computable and are the natural targets of characteristic classes.

### 6.1. Singular homology and cohomology

The singular chain group $C_n(X;\mathbb{Z})$ is the free abelian group on continuous maps
$$
\sigma : \Delta^n \to X.
$$
The boundary operator
$$
\partial : C_n(X) \to C_{n-1}(X)
$$
satisfies $\partial^2=0$. The homology groups are
$$
H_n(X;\mathbb{Z}) = \ker \partial / \operatorname{im} \partial.
$$
Dually, cochains are
$$
C^n(X;\mathbb{Z}) = \operatorname{Hom}(C_n(X),\mathbb{Z})
$$
with coboundary $\delta$, and
$$
H^n(X;\mathbb{Z}) = \ker \delta / \operatorname{im} \delta.
$$
Homology captures cycles modulo boundaries; cohomology captures cocycles modulo coboundaries.[^1]

### 6.2. Differential forms and de Rham cohomology

If $M$ is smooth, one can replace singular cochains by differential forms. Let $\Omega^k(M)$ be the smooth $k$-forms, with exterior derivative
$$
d : \Omega^k(M) \to \Omega^{k+1}(M),
\qquad d^2=0.
$$
The de Rham cohomology groups are
$$
H^k_{\mathrm{dR}}(M) = \ker(d : \Omega^k \to \Omega^{k+1}) / \operatorname{im}(d : \Omega^{k-1} \to \Omega^k).
$$
The de Rham theorem states that
$$
H^k_{\mathrm{dR}}(M) \cong H^k(M;\mathbb{R}).
$$
Thus closed forms modulo exact forms compute ordinary cohomology with real coefficients.[^2]

This is one of the most important bridges between topology and differential geometry. It is the bridge on which Chern--Weil theory is built.

### 6.3. Stokes' theorem and gauge theory

Stokes' theorem says that for a compact oriented manifold with boundary,
$$
\int_M d\omega = \int_{\partial M} \omega.
$$
Whenever one writes a topological density as an exact form,
$$
P(F)=dQ(A),
$$
one is invoking Stokes' theorem to turn bulk information into boundary information. This is the mathematical core of anomaly inflow and of the statement that the Chern--Simons form is a transgression form.[^2][^11]

### 6.4. Cup products and intersection pairings

Cohomology carries a product,
$$
\smile : H^p(X;R) \times H^q(X;R) \to H^{p+q}(X;R),
$$
called the cup product. In de Rham theory this is represented by the wedge product of forms.

On a closed oriented $n$-manifold $M$, Poincaré duality gives a nondegenerate pairing
$$
H^k(M;R) \times H^{n-k}(M;R) \to R,
\qquad
([\alpha],[\beta]) \mapsto \int_M \alpha \wedge \beta.
$$
This pairing turns cohomology into the correct language for intersection theory.[^2][^3]

### 6.5. Poincaré duality and linking

For a closed oriented $n$-manifold $M$, Poincaré duality gives
$$
H^k(M;R) \cong H_{n-k}(M;R).
$$
A codimension-$k$ oriented submanifold $N \subset M$ determines a cohomology class
$$
\operatorname{PD}[N] \in H^k(M;R)
$$
called its Poincaré dual, characterized by
$$
\int_N \iota^*\eta = \int_M \eta \wedge \operatorname{PD}[N]
$$
for all closed forms $\eta$ of degree $n-k$.

In low-dimensional TQFT this is indispensable. Worldlines and worldsheets are naturally represented by homology classes; the gauge fields to which they couple are naturally represented by cohomology classes. The Poincaré duality is what lets one convert between the two.

In particular, linking numbers in dimension three can be expressed cohomologically. If $C_1,C_2 \subset M^3$ are disjoint oriented closed curves and $S$ is a Seifert surface with $\partial S=C_1$, then
$$
\operatorname{Lk}(C_1,C_2)= [S]\cdot [C_2].
$$
Equivalently, if $\alpha$ is a one-form singular along $S$ with
$$
d\alpha = \operatorname{PD}[C_1],
$$
then
$$
\operatorname{Lk}(C_1,C_2)=\int_{C_2} \alpha.
$$
This is the precise topological content of abelian Wilson-loop linking formulas in Chern--Simons theory.[^2]

---

## 7. Principal bundles, connections, and characteristic classes

### 7.1. Connections

Let $P \to M$ be a principal $G$-bundle with Lie algebra $\mathfrak g$. A **connection** on $P$ is a $\mathfrak g$-valued $1$-form
$$
A \in \Omega^1(P;\mathfrak g)
$$
satisfying two conditions:

1. on vertical vectors it reproduces the generator in $\mathfrak g$,
2. it is equivariant under the right $G$-action.

On a local trivialization this becomes the familiar gauge potential, also denoted $A$, on the base. Its curvature is
$$
F = dA + A \wedge A.
$$
Under a gauge transformation $g : M \to G$ one has
$$
A \mapsto g^{-1}Ag + g^{-1}dg,
\qquad
F \mapsto g^{-1}Fg.
$$
The Bianchi identity is
$$
D_A F = dF + [A,F]=0.
$$
These are local formulas, but the existence of the bundle itself is a global topological datum.[^3][^11]

### 7.2. Chern--Weil theory

Let $P$ be an invariant polynomial on the Lie algebra $\mathfrak g$. Then the differential form
$$
P(F)
$$
built from the curvature is closed, and its de Rham cohomology class is independent of the choice of connection. Hence it defines a characteristic class of the bundle.[^11]

For complex vector bundles the most important characteristic classes are the Chern classes. Formally,
$$
\det\!\left(I + \frac{i}{2\pi}F\right)
= 1 + c_1(E) + c_2(E) + \cdots.
$$
The first Chern class is represented by
$$
c_1(E)=\left[\frac{i}{2\pi}\operatorname{tr}F\right].
$$
The Chern character is
$$
\operatorname{ch}(E)=\operatorname{tr}\exp\!\left(\frac{iF}{2\pi}\right).
$$

This matters in TQFT because topological action functionals are built from these characteristic forms. In four dimensions, for example,
$$
\operatorname{tr}(F\wedge F)
$$
represents a characteristic class; in three dimensions the Chern--Simons form is its transgression.

### 7.3. Transgression and the Chern--Simons form

For a connection $A$ define
$$
\omega_{\mathrm{CS}}(A)=\operatorname{tr}\!\left(A\wedge dA + \frac{2}{3}A\wedge A\wedge A\right).
$$
A direct calculation gives
$$
d\omega_{\mathrm{CS}}(A)=\operatorname{tr}(F\wedge F).
$$
Thus the three-dimensional Chern--Simons form is a transgression form for the four-dimensional characteristic class. This relation is the local algebraic origin of both anomaly descent and Chern--Simons gauge theory.[^11]

---

## 8. Lie groups as topological spaces

A **Lie group** is both a smooth manifold and a group, with multiplication and inversion smooth.[^7]

From the geometric point of view, a Lie group is a manifold carrying extra rigid structure. From the topological point of view, it is a highly structured space with computable homotopy type. Both viewpoints are indispensable in TQFT.

### 8.1. Basic examples

1. $U(1) = \{ z \in \mathbb{C} : |z|=1\} \cong S^1$.
2. $U(n)$ is the group of unitary matrices.
3. $SU(n)$ is the subgroup of $U(n)$ with determinant $1$.
4. $SO(n)$ is the group of orientation-preserving orthogonal matrices.
5. $Spin(n)$ is the simply connected double cover of $SO(n)$.[^7][^8]

### 8.2. $SU(2)$ is the three-sphere

Every element of $SU(2)$ has the form
$$
\begin{pmatrix}
a & b \\
-\overline b & \overline a
\end{pmatrix}
$$
with
$$
|a|^2+|b|^2=1.
$$
Writing
$$
a=x_1+ix_2,
\qquad
b=x_3+ix_4,
$$
this condition becomes
$$
x_1^2+x_2^2+x_3^2+x_4^2=1.
$$
Hence as a manifold,
$$
SU(2) \cong S^3.
$$
Therefore
$$
\pi_1(SU(2))=0,
\qquad
\pi_3(SU(2))\cong \pi_3(S^3)\cong \mathbb{Z}.
$$
The second statement is the prototype of all winding-number statements for compact simple Lie groups.[^7]

### 8.3. $SO(3)$ and its double cover

There is a surjective homomorphism
$$
SU(2) \to SO(3)
$$
with kernel $\{\pm I\}$. Thus
$$
SO(3) \cong SU(2)/\{\pm I\} \cong S^3/\{\pm 1\} \cong \mathbb{R}P^3.
$$
Since $S^3 \to \mathbb{R}P^3$ is a double cover,
$$
\pi_1(SO(3)) \cong \mathbb{Z}_2.
$$
More generally, for $n\ge 3$ one has
$$
\pi_1(SO(n))\cong \mathbb{Z}_2,
$$
and $Spin(n)$ is the simply connected double cover.[^8]

This distinction is physically important. A gauge theory with gauge group $SO(3)$ is not the same global theory as one with gauge group $SU(2)$, even though the Lie algebras agree.

### 8.4. Maximal tori and the first homotopy group

A maximal torus of $U(n)$ is the subgroup of diagonal matrices
$$
\operatorname{diag}(e^{i\theta_1},\dots,e^{i\theta_n}),
$$
so topologically it is $T^n=(S^1)^n$.[^7]

There is a short exact sequence of Lie groups
$$
1 \to SU(n) \to U(n) \xrightarrow{\det} U(1) \to 1.
$$
Since $SU(n)$ is connected, this yields a fibration
$$
SU(n) \hookrightarrow U(n) \to U(1).
$$
The associated long exact sequence in homotopy gives, at the level of fundamental groups,
$$
\pi_1(SU(n)) \to \pi_1(U(n)) \to \pi_1(U(1)) \to \pi_0(SU(n)).
$$
Now $\pi_0(SU(n))=0$ and $\pi_1(U(1))\cong \mathbb{Z}$. For $n\ge 2$, $SU(n)$ is simply connected, so one obtains
$$
\pi_1(U(n))\cong \mathbb{Z},
\qquad
\pi_1(SU(n))=0.
$$
This single integer for $U(n)$ is the stable winding number detected by the determinant.

### 8.5. $\pi_3(SU(n))$ by the fibration $SU(n-1) \to SU(n) \to S^{2n-1}$

We now derive the statement needed in Chern--Simons theory.

For each $n\ge 2$ there is a fibration
$$
SU(n-1) \hookrightarrow SU(n) \to S^{2n-1}.
$$
Indeed, the action of $SU(n)$ on the unit sphere in $\mathbb{C}^n$ is transitive, and the stabilizer of the vector $e_1$ is naturally $SU(n-1)$.

The long exact sequence gives
$$
\pi_3(SU(n-1)) \to \pi_3(SU(n)) \to \pi_3(S^{2n-1}) \to \pi_2(SU(n-1)).
$$
If $n\ge 3$, then $2n-1 \ge 5$, so
$$
\pi_3(S^{2n-1})=0.
$$
Hence
$$
\pi_3(SU(n-1)) \xrightarrow{\sim} \pi_3(SU(n)).
$$
Since we already know
$$
\pi_3(SU(2))\cong \mathbb{Z},
$$
induction yields
$$
\pi_3(SU(n))\cong \mathbb{Z}
\qquad (n\ge 2).
$$
This is the precise reason why a map
$$
g : S^3 \to SU(n)
$$
has an integer winding number.

### 8.6. Stable homotopy of classical groups and Bott periodicity

The homotopy groups of the classical groups stabilize as $n\to\infty$. Bott periodicity says that in the stable range the unitary groups have period $2$ and the orthogonal groups period $8$.[^12]

For the stable unitary group $U=\varinjlim U(n)$,
$$
\pi_{2k}(U)=0,
\qquad
\pi_{2k+1}(U)\cong \mathbb{Z}.
$$
In particular,
$$
\pi_1(U)\cong \mathbb{Z},
\qquad
\pi_3(U)\cong \mathbb{Z}.
$$
Bott periodicity lies deeper than what is strictly needed for elementary Chern--Simons theory, but conceptually it explains why characteristic classes, $K$-theory, and homotopy groups of Lie groups are all organized by a small number of periodic patterns.

---

## 9. Holonomy and monodromy

### 9.1. Parallel transport

Let $E \to M$ be a vector bundle with connection $\nabla$. Along a path
$$
\gamma : [0,1] \to M,
$$
a section $s(t)$ of $\gamma^*E$ is **parallel** if
$$
\nabla_{\dot\gamma} s = 0.
$$
Solving this ODE gives a linear isomorphism
$$
P_\gamma : E_{\gamma(0)} \to E_{\gamma(1)},
$$
called parallel transport.

For concatenated paths,
$$
P_{\gamma_2 * \gamma_1}=P_{\gamma_2}\circ P_{\gamma_1}.
$$
For the reverse path,
$$
P_{\overline\gamma}=P_\gamma^{-1}.
$$
Thus parallel transport behaves exactly as one expects from physical transport operators.[^5][^6]

### 9.2. Holonomy group

Fix $x\in M$. The **holonomy group** at $x$ is the subgroup of automorphisms of the fiber $E_x$ generated by parallel transport around based loops at $x$:
$$
\operatorname{Hol}_x(\nabla) \subset \operatorname{Aut}(E_x).
$$
The **restricted holonomy group** is generated by loops contractible to a point. The difference between the full and restricted holonomy groups is topological: it is controlled by the fundamental group.[^6]

### 9.3. Flat connections and holonomy representations

A connection is **flat** if its curvature vanishes:
$$
F_\nabla=0.
$$
Flatness implies that locally the connection is gauge equivalent to the trivial connection. Globally, however, flat connections may still be nontrivial because of holonomy.

If $\nabla$ is flat on a principal $G$-bundle, then parallel transport around loops depends only on the homotopy class of the loop. Therefore a flat connection determines a representation
$$
\rho_\nabla : \pi_1(M,x) \to G,
$$
well-defined up to conjugation. Conversely, on a suitable bundle, a representation of the fundamental group determines a flat connection up to gauge equivalence. In concise form,
$$
\mathcal{M}_{\mathrm{flat}}(M,G)
\cong
\operatorname{Hom}(\pi_1(M),G)/G,
$$
where the quotient on the right is by conjugation.[^5]

This identification is one of the fundamental structural results behind Chern--Simons theory. The classical solutions are flat connections, and the moduli space of classical solutions is therefore a representation variety.

### 9.4. Path-ordered exponentials

In local coordinates on a trivial bundle, a connection is a Lie-algebra valued one-form $A$. Parallel transport along $\gamma$ is formally
$$
P_\gamma(A)=\mathcal{P}\exp\left(-\int_\gamma A\right),
$$
where $\mathcal{P}$ denotes path ordering. If $\gamma$ is a loop, this is the holonomy around the loop. Under gauge transformation,
$$
A \mapsto g^{-1}Ag+g^{-1}dg,
$$
one has
$$
P_\gamma(A) \mapsto g(\gamma(0))^{-1} P_\gamma(A) g(\gamma(1)).
$$
For a loop based at $x$, holonomy is therefore conjugated by $g(x)$, and conjugacy-invariant functions of holonomy are gauge invariant.

This is precisely why Wilson loops
$$
W_R(\gamma)=\operatorname{Tr}_R P_\gamma(A)
$$
are natural observables.

### 9.5. Monodromy

The word **monodromy** is used in a few closely related senses.

1. For a local system or flat bundle, monodromy is the representation of $\pi_1$ obtained by analytic continuation of flat sections around loops.
2. For a multivalued analytic function, monodromy describes how a local branch changes after continuation around singularities.
3. In integrable systems, monodromy measures the obstruction to defining global action-angle coordinates.[^6][^4]

In the bundle-theoretic setting relevant to TQFT, monodromy and holonomy are essentially the same structure: both measure how local data fail to return trivially after going around a nontrivial loop.

### 9.6. Holonomy versus curvature

Curvature measures infinitesimal failure of parallel transport to be path independent. Holonomy measures the integrated global effect of that failure. If curvature vanishes identically, local holonomy around contractible loops is trivial. The remaining holonomy is then purely topological and is controlled by the fundamental group. This is the key reason flat connections are topological objects.

---

## 10. Symplectic geometry

Symplectic geometry enters TQFT because the moduli space of flat connections on a surface is symplectic, and quantization of that space produces the Hilbert space of the theory.

### 10.1. Symplectic manifolds

A **symplectic structure** on a manifold $M$ is a closed nondegenerate $2$-form
$$
\omega \in \Omega^2(M),
\qquad
 d\omega=0.
$$
Nondegeneracy means that at each point the linear map
$$
T_pM \to T_p^*M,
\qquad
v \mapsto \iota_v\omega
$$
is an isomorphism. In particular, $\dim M$ must be even.[^4]

The $n$th exterior power satisfies
$$
\omega^n \neq 0,
$$
so a symplectic manifold carries a canonical volume form
$$
\frac{1}{n!}\omega^n.
$$

### 10.2. Darboux theorem

One of the most important facts in symplectic geometry is Darboux's theorem: around every point there are local coordinates
$$
(q_1,p_1,\dots,q_n,p_n)
$$
such that
$$
\omega = \sum_{j=1}^n dq_j \wedge dp_j.
$$
Thus, unlike Riemannian geometry, symplectic geometry has no local invariants: all local structure is the same. The interesting information is global.[^4]

This is exactly parallel to TQFT: the theory is not about local metric structure, but about global organization.

### 10.3. Hamiltonian vector fields and Poisson brackets

Given a smooth function $H\in C^\infty(M)$, its Hamiltonian vector field $X_H$ is defined by
$$
\iota_{X_H}\omega = -dH.
$$
The Poisson bracket of functions $F,G$ is
$$
\{F,G\}=\omega(X_F,X_G).
$$
This gives $C^\infty(M)$ the structure of a Lie algebra, and
$$
X_{\{F,G\}}=[X_F,X_G].
$$
The Hamiltonian flow preserves $\omega$.[^4]

### 10.4. Moment maps

Suppose a Lie group $G$ acts on a symplectic manifold $(M,\omega)$ preserving $\omega$. For each $\xi\in\mathfrak g$, let $\xi_M$ be the generating vector field. The action is **Hamiltonian** if there exists a map
$$
\Phi : M \to \mathfrak g^*
$$
such that for every $\xi\in\mathfrak g$,
$$
d\langle \Phi,\xi\rangle = -\iota_{\xi_M}\omega.
$$
The map $\Phi$ is the **moment map**.[^4]

The moment map packages the conserved quantities associated to the group action. It is the symplectic version of Noether's theorem.

### 10.5. Symplectic reduction

If $\mu\in\mathfrak g^*$ is a regular value of the moment map and the quotient is well behaved, then the reduced space
$$
M_{\mu}=\Phi^{-1}(\mu)/G_\mu
$$
has a natural symplectic form $\omega_\mu$ characterized by
$$
\iota^*\omega = \pi^*\omega_\mu.
$$
This is the Marsden--Weinstein--Meyer symplectic reduction theorem.[^4]

This construction is ubiquitous in gauge theory. One starts with a large space carrying redundant gauge degrees of freedom, imposes the moment-map constraint, and divides by the symmetry group. The resulting quotient is the physical phase space.

### 10.6. The moduli space of flat connections as a symplectic quotient

Let $\Sigma$ be an oriented closed surface and let $\mathcal{A}$ be the affine space of connections on a fixed principal $G$-bundle over $\Sigma$. Its tangent space at any point may be identified with
$$
\Omega^1(\Sigma;\mathfrak g).
$$
The $2$-form
$$
\Omega(\alpha,\beta)=\int_\Sigma \operatorname{tr}(\alpha\wedge\beta)
$$
defines a symplectic structure on $\mathcal{A}$, at least formally. The gauge group acts on $\mathcal{A}$, and the corresponding moment map is the curvature,
$$
\mu(A)=F_A.
$$
Therefore the symplectic quotient is
$$
\mu^{-1}(0)/\mathcal{G}
=
\{A : F_A=0\}/\mathcal{G},
$$
namely the moduli space of flat connections.[^4]

This observation, due to Atiyah and Bott in the two-dimensional setting, is one of the central mathematical reasons symplectic geometry appears in Chern--Simons theory: the classical phase space on a spatial surface $\Sigma$ is a moduli space of flat connections, and that moduli space is symplectic.

---

## 11. Lie-group-valued topology in Chern--Simons theory

We now isolate the specific topological statements that enter the nonabelian Chern--Simons action.

### 11.1. The winding number of a map $S^3 \to SU(2)$

Since
$$
SU(2)\cong S^3,
$$
a continuous map
$$
g : S^3 \to SU(2)
$$
can be viewed as a map $S^3\to S^3$. Its homotopy class is therefore determined by an integer degree,
$$
\deg(g)\in\mathbb{Z}.
$$
A standard normalized integral representative of this degree is
$$
\deg(g)
=
\frac{1}{24\pi^2}
\int_{S^3} \operatorname{tr}(g^{-1}dg)^{\wedge 3}.
$$
The integral is homotopy invariant because the integrand represents a generator of $H^3(SU(2);\mathbb{Z})$ under the chosen normalization.

### 11.2. Generalization to compact simple simply connected $G$

For a compact simple simply connected Lie group $G$, one has
$$
\pi_3(G)\cong \mathbb{Z}.
$$
Thus a map from a closed oriented $3$-manifold into $G$ carries an integer topological charge, and the same type of normalized Wess--Zumino integral computes it.[^12]

This is the topological reason the Chern--Simons action changes by an integer multiple of $2\pi k$ under large gauge transformations. One does not merely say that the action changes by a boundary term. One says more precisely that the remaining global term is controlled by the integer class in $\pi_3(G)$.

---

## 12. Bordisms and functorial TQFT

The functorial definition of TQFT, due to Atiyah and Segal, packages the gluing law of path integrals into category theory.

### 12.1. Bordism category

Fix a tangential structure, for example orientation. The objects of the bordism category $\operatorname{Bord}_n$ are closed $(n-1)$-manifolds. A morphism
$$
M : \Sigma_0 \to \Sigma_1
$$
is an $n$-dimensional bordism from $\Sigma_0$ to $\Sigma_1$, meaning an $n$-manifold whose boundary is identified with
$$
\partial M \cong \overline{\Sigma_0} \sqcup \Sigma_1.
$$
Composition is by gluing along the common boundary. The monoidal structure is disjoint union.[^9][^10]

### 12.2. Definition of TQFT

An $n$-dimensional TQFT is a symmetric monoidal functor
$$
Z : \operatorname{Bord}_n \to \operatorname{Vect}_k
$$
or into Hilbert spaces in a unitary setting. Thus:

- to each closed $(n-1)$-manifold $\Sigma$ one assigns a vector space $Z(\Sigma)$,
- to each bordism $M : \Sigma_0 \to \Sigma_1$ one assigns a linear map
$$
Z(M): Z(\Sigma_0) \to Z(\Sigma_1),
$$
- disjoint unions go to tensor products,
- gluing of bordisms goes to composition of linear maps.[^9][^10]

This formalizes the path-integral slogan that amplitudes compose under gluing.

### 12.3. Low-dimensional classification

The simplest nontrivial classification result is in dimension two: oriented $2$-dimensional TQFTs are equivalent to commutative Frobenius algebras.[^10]

Concretely, if
$$
Z : \operatorname{Bord}_2 \to \operatorname{Vect}_k,
$$
then the vector space
$$
A=Z(S^1)
$$
comes equipped with multiplication, unit, comultiplication, and counit obtained from the pair-of-pants bordisms and disks, and these satisfy the Frobenius relations. Conversely, a commutative Frobenius algebra determines a $2$D TQFT.

This is a magnificent toy model because it shows how topological gluing laws become algebraic identities.

### 12.4. Extended TQFT and the cobordism hypothesis

The functorial viewpoint can be refined by assigning data not only to $(n-1)$-manifolds and $n$-bordisms, but also to corners of lower codimension. This leads to **extended TQFTs** and higher categories.

The cobordism hypothesis, in one modern formulation, says roughly that fully extended framed TQFTs are classified by fully dualizable objects in the target symmetric monoidal higher category.[^10]

For the present review, the main use of this idea is conceptual: it explains why local operators, line operators, surface operators, and boundary conditions in topological theories fit into one coherent algebraic structure.

---

## 13. Chern--Simons theory as a TQFT

### 13.1. Classical action

On a closed oriented $3$-manifold $M$ and a principal $G$-bundle with connection $A$, the Chern--Simons action is
$$
S_{\mathrm{CS}}[A]
=
\frac{k}{4\pi}
\int_M \operatorname{tr}\!\left(A\wedge dA + \frac{2}{3}A\wedge A\wedge A\right).
$$
Its Euler--Lagrange equation is
$$
F_A=0.
$$
Thus classical solutions are flat connections.

So the classical moduli space is
$$
\mathcal{M}_{\mathrm{cl}}(M,G)
=
\{A : F_A=0\}/\mathcal{G}
\cong
\operatorname{Hom}(\pi_1(M),G)/G.
$$
The topology of the manifold enters immediately via $\pi_1(M)$.[^5]

### 13.2. Gauge transformations and level quantization

For a gauge transformation $g : M \to G$ one has
$$
A \mapsto A^g = g^{-1}Ag + g^{-1}dg.
$$
The Chern--Simons form changes by an exact term plus a global term involving
$$
\operatorname{tr}(g^{-1}dg)^{\wedge 3}.
$$
On a closed manifold the exact term integrates to zero, leaving
$$
S_{\mathrm{CS}}[A^g]-S_{\mathrm{CS}}[A]
=2\pi k\, n(g),
$$
where $n(g)\in\mathbb{Z}$ is the winding number determined by the class $[g]\in\pi_3(G)$. Therefore the path integral phase
$$
e^{iS_{\mathrm{CS}}}
$$
is gauge invariant precisely when $k\in\mathbb{Z}$, assuming the standard normalization. The topological input is exactly the identification
$$
\pi_3(G)\cong \mathbb{Z}.
$$

### 13.3. Canonical quantization on a surface

Let spacetime be $\mathbb{R}\times\Sigma$, where $\Sigma$ is a closed oriented surface. The field equation says the spatial connection must be flat, so the reduced classical phase space is the moduli space of flat $G$-connections on $\Sigma$. As explained above, this moduli space carries a natural symplectic form. Quantizing that symplectic manifold produces the Hilbert space assigned by the TQFT to the surface:
$$
\mathcal{H}_\Sigma = Z(\Sigma).
$$
Thus the topology and symplectic geometry are not parallel stories. They are the classical and quantum halves of the same construction.

### 13.4. Wilson lines, holonomy, and braiding

Given a loop $\gamma$ in a representation $R$, the Wilson operator is
$$
W_R(\gamma)=\operatorname{Tr}_R \mathcal{P}\exp\left(\oint_\gamma A\right).
$$
Since the classical solutions are flat, Wilson loops are controlled by holonomy classes. In abelian Chern--Simons theory, correlators of Wilson loops reduce to linking numbers; in nonabelian theory they lead to quantum-group and knot-polynomial structures after quantization. The topology of loops in the $3$-manifold thus becomes encoded in quantum amplitudes.

---

## 14. Action-angle variables, monodromy, and global obstructions

Although not strictly required for basic Chern--Simons theory, it is useful to understand why monodromy is also a symplectic concept.

In an integrable Hamiltonian system with Lagrangian torus fibration,
$$
\pi : M \to B,
$$
local action-angle coordinates exist by the Arnold--Liouville theorem. Globally, however, there may be an obstruction to choosing them consistently. That obstruction is called monodromy.[^4]

Geometrically, one transports a basis of $H_1$ of the torus fibers around a loop in the base $B$; after returning, the basis may be transformed by an element of $GL(n,\mathbb{Z})$. This monodromy measures the twisting of the torus fibration. The moral is again the same: local triviality does not imply global triviality. The same principle reappears in flat bundles, modular functors, and families of Hilbert spaces in TQFT.

---

## 15. A compact checklist of the structures one repeatedly needs

For a Chern--Simons/TQFT review, the following list is worth having mentally available.

### Topological data

- $\pi_1(M)$ for holonomy of flat connections.
- $\pi_3(G)$ for large gauge transformations and level quantization.
- $H^2(M;\mathbb{Z})$ and higher cohomology groups for characteristic classes.
- Poincaré duality and linking pairings for Wilson-loop observables.

### Geometric data

- principal $G$-bundles and connections,
- curvature and Chern--Weil representatives,
- holonomy and monodromy,
- symplectic manifolds, moment maps, and reduction.

### Categorical/TQFT data

- bordism categories,
- symmetric monoidal functors,
- Frobenius algebras in $2$D,
- quantization of moduli spaces in $3$D,
- line operators and gluing laws.

---

## 16. The main logical chain

Let me end by writing the conceptual chain in one line.

1. A connection on a principal bundle gives parallel transport.
2. For flat connections, parallel transport descends to a representation of $\pi_1$.
3. The moduli space of flat connections on a surface is a symplectic quotient.
4. Quantizing that symplectic quotient gives the state space of Chern--Simons theory.
5. Large gauge transformations are classified by $\pi_3(G)$, forcing level quantization.
6. Wilson lines probe holonomy, and their correlators detect topological linking.
7. Functorially, the entire theory is encoded by a symmetric monoidal functor from bordisms.

This chain is the skeleton of a great deal of low-dimensional gauge theory.

## 17. Suggested minimum working background for the rest of the review

If one is reading a review centered on Chern--Simons theory, the minimum mathematical facts to be able to use fluently are these:

- the definition and elementary computation of $\pi_1$,
- covering spaces and winding number on $S^1$,
- de Rham cohomology and Stokes' theorem,
- principal bundles and gauge transformations,
- the Chern--Simons transgression identity,
- the symplectic structure on the moduli of flat connections on a surface,
- the functorial definition of a TQFT,
- the specific homotopy groups
$$
\pi_1(U(1))=\mathbb{Z},
\qquad
\pi_1(SO(3))=\mathbb{Z}_2,
\qquad
\pi_1(SU(n))=0,
\qquad
\pi_3(SU(n))=\mathbb{Z}.
$$

Once these facts are in hand, the rest of the subject stops looking like a collection of miraculous formulas and starts looking like a coherent interaction between topology, geometry, and quantum field theory.

---

## Footnotes

[^1]: Allen Hatcher, *Algebraic Topology*, Cornell University notes/PDF. https://pi.math.cornell.edu/~hatcher/AT/AT.pdf

[^2]: Raoul Bott and Loring W. Tu, *Differential Forms in Algebraic Topology* (online scan/PDF consulted for de Rham and characteristic-class background). https://poisson.phc.dm.unipi.it/~lmigliorini/tesi_tr/bott_tu_diff_forms_algtop.pdf

[^3]: Ralph Cohen, *Bundles, Manifolds, and Homotopy* and related Stanford bundle-topology notes. https://math.stanford.edu/~ralph/bookR4.pdf and https://math.stanford.edu/~ralph/fiber.pdf

[^4]: Eckhard Meinrenken, *Symplectic Geometry* lecture notes, University of Toronto. https://www.math.toronto.edu/mein/teaching/LectureNotes/symplectic.pdf

[^5]: David L. Duncan, *Flat connections and holonomy*. https://users.math.msu.edu/users/duncan42/FlatConnectionsAndHolonomy.pdf

[^6]: Lecture notes on connection, curvature, and holonomy consulted for the bundle/holonomy viewpoint: L. Ni, *Connexion, Holonomy and Covariant Derivatives* (UCSD notes), and J. M. F. notes on holonomy from Edinburgh. https://math.ucsd.edu/~lni/math250c/connection-curvature.pdf and https://empg.maths.ed.ac.uk/Activities/Spin/Lecture7.pdf

[^7]: Columbia and related university Lie-group notes consulted for maximal tori, $SU(n)$, and classical groups: John Morgan, *Lie Groups* lecture notes; Peter Woit, Lie group notes. https://www.math.columbia.edu/~jmorgan/LieGroups2025/2025LGLecture10.pdf and https://www.math.columbia.edu/~woit/LieGroups-2023/background-liegroupsandalgebras.pdf

[^8]: Peter Woit, *Clifford Algebras and Spin Groups*, for the topological relation between $SO(n)$ and $Spin(n)$. https://www.math.columbia.edu/~woit/LieGroups-2012/cliffalgsandspingroups.pdf

[^9]: John Baez, *Topological Quantum Field Theory* (expository article on Atiyah's axioms and bordism-functor viewpoint). https://math.ucr.edu/home/baez/planck/node3.html

[^10]: Nils Carqueville and Ingo Runkel, *Introductory lectures on topological quantum field theory*. https://arxiv.org/pdf/1705.05734

[^11]: Chiu-Chu Melissa Liu / Christopher Siegel notes consulted for Chern--Weil background and characteristic classes: https://www2.math.upenn.edu/~siegelch/Notes/at2.pdf ; also University of Chicago expository note on Chern--Weil theory: https://math.uchicago.edu/~may/REU2017/REUPapers/Rahman.pdf

[^12]: Richard Melrose's MIT notes and Hatcher's *Vector Bundles and K-Theory* page were consulted for Bott periodicity and the stable homotopy of classical groups. https://math.mit.edu/~rbm/18.157-F05-Chapter14.pdf and https://pi.math.cornell.edu/~hatcher/VBKT/VBpage.html
