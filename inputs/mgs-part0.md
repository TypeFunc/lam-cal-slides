### Algorithms vs. Languages

+ The <a class="highlight-green">*Church-Turing Thesis*</a> 
  is one of the most important ideas in computer science.
  
+ The impact of the models of Church and Turing goes 
  well beyond the thesis itself.
  <!-- .element: class="fragment fade-left" -->

+ The two models have impacted two distinct communities.
  <!-- .element: class="fragment fade-left" -->

+ Turing Machine $\rightsquigarrow$ Algorithms and Complexity
  <!-- .element: class="fragment fade-left" -->

+ $\lambda$-Calculus $\rightsquigarrow$ Programming Languages
  <!-- .element: class="fragment fade-left" -->

---

### Efficiency vs. Structure

The impact and separation is not accidental.

<p>Two sources of beauty in programs: </p><!-- .element: class="fragment fade-up" -->

<div><a class="highlight-red">Efficiency</a></div><!-- .element: class="fragment fade-right" -->
<div><a class="highlight-blue">Structure</a></div><!-- .element: class="fragment fade-left" -->

---

### Turing Machine $\leftrightsquigarrow$ Algorithms

<div><a class="highlight-blue">*efficiency*</a></div>
<!-- .element: class="fragment fade-up" -->
<p>Turing Machines are good at measuring resources.</p>
<!-- .element: class="fragment fade-up" -->

+ <div>**Axiomatic complexity theory**  
  P vs. NP, polynomial hierarchy, P-space</div>
  <!-- .element: class="fragment fade-left" -->
+ <div>**asymptotic analysis** of algorithms</div>
  <!-- .element: class="fragment fade-left" -->
+ <div>**Cryptography** is based on complexity</div>
  <!-- .element: class="fragment fade-left" -->
+ <div>**Learning theory**  
  based on learning power of Turing machines</div>
  <!-- .element: class="fragment fade-left" -->

---

### $\lambda$-Calculus $\leftrightsquigarrow$ Languages

<div><a class="highlight-blue">*structure*</a></div>
<!-- .element: class="fragment fade-up" -->
<p>$\lambda$-Calculus is good at composition and abstraction.</p>
<!-- .element: class="fragment fade-right" -->

+ <div>**Call-by-value**, **lexical scoping**, **recursion**</div>
  <!-- .element: class="fragment fade-left" -->
+ <div>**lambda abstractions, higher-order-functions**   
  (recently even in C++ and Java!)</div>
  <!-- .element: class="fragment fade-left" -->
+ <div>**denotational semantics**</div>
  <!-- .element: class="fragment fade-left" -->
+ <div>**type theory**  
  the "theory of abstraction"</div>
  <!-- .element: class="fragment fade-left" -->
+ <div>**proof assistants**  
  Agda, Coq, NuPRL, Isabelle</div>
  <!-- .element: class="fragment fade-left" -->
+ <div>**Languages** Lisp, FP, ML, Haskell, Scala (Java, Python, C++)</div>
  <!-- .element: class="fragment fade-left" -->

---

### The $\lambda$-Calculus

<a class="highlight-blue">**Syntax**</a>
<div>$e = x \mid \lambda x.e \mid e(e)$</div><!-- .element: class="fragment fade-left" -->

<a class="highlight-blue">**Computation**</a>
<div>repeat single rule called $\beta$-reduction:
$\lambda x.[\dots x \dots x \dots] (e_2 ) \Rightarrow [\dots e_2 \dots e_2 \dots]$
</div><!-- .element: class="fragment fade-left" -->

<a class="highlight-blue">**Finished** </a>
<div> when no expressions of the form $e(e)$</div><!-- .element: class="fragment fade-left" -->

---

### Examples

1. $(\lambda x . (2 \times x + 1))7$<!-- .element: class="fragment fade-left" -->

2. $((\lambda f . \lambda x . (f (f x))) \lambda x . (x + 3)) 2$<!-- .element: class="fragment fade-left" -->

3. $\lambda x.x(x) (\lambda x.x(x))$<!-- .element: class="fragment fade-left" -->

---

Turing was ahead of his time...

...but Church was <a class="highlight-blue">*way*</a> ahead of his time.

+ $\lambda$-calculus does not define a reduction order.

+ **Problem:** does not make for a good cost model because 
number of steps depends on the reduction order and 
some orders are not efficient to evaluate.

+ **Virtue:** it is inherently parallel!! 

---

### Church: <a class="highlight-blue">*way*</a> ahead of his time

**Key Idea:**

1. Fix an order that is parallel, and cheap to evaluate.  
2. Base a cost model on it.  
3. Bound cost when mapped to standard models.  

Once we have an order, we can:

+ count number of reductions (work)

+ count number of parallel steps (depth or span)

---

### Conclusion

+ **Next 50 years:** need to integrate Complexity/Algorithms and
  Programming Language Theory.

+ **Cost models:** should be based on languages, not machines. 
  Particularly important for parallelism.

+ **Other opportunities:** Verification, type-theory and complexity,
  probabilistic programming, programs-as-data, cryptography
  and PL, game-theory and PL.

---

### End of Part 1

(take a short break)
