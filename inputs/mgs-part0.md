## Part I

### Lambda Calculus:
### a brief historical overview

---

<!-- ------ ALONZO CHURCH ------------ -->
<!-- .slide: data-background="inputs/img/17417-alonzo_church_photo.jpg" data-background-size="contain" data-state="img-right" -->
**Alonzo Church** 

(1903-1995)
	
<p class="fragment fade-left"> 
(~1930) <a class="highlight-blue">**Church**</a>
develops  
a system for logic and  
computation called the  
<a class="highlight-blue">**Lambda Calculus**</a>

<!-- <p style="text-align:right" class="fragment fade-left"> -->
<p class="fragment fade-left">
(~1935) argues that every  
*"effectively computable"*  
function on $\mathbb{N}$ can be  
computed in his calculus
</p>

---

<!-- ------ ALAN TURING ------------ -->
<!-- .slide: data-background="inputs/img/alan-turing.jpg" data-background-size="contain" data-state="dim" -->
**Alan Turing** 

(1912-1954)

<p class="fragment fade-left"> 
(~1935) <!-- independently,   -->
<a class="highlight-green">**Turing**</a> 
develops  
what is now called a  
<a class="highlight-green">**Turing Machine**</a>
</p>

<p class="fragment fade-left"> 
(~1936) also argues every  
*"effectively computable"*  
function on $\mathbb{N}$ can be   
computed by his machine...
</p> 
<p class="fragment fade-left"> 
...and proved the two models
equivalent--compelling evidence for <!-- *universality* of  -->
<!-- these computational models...  -->
<a class="highlight-green">**Church-Turing Thesis**</a>
</p> 

---

<!-- ---- Church-Turing Thesis Graphic ------ -->
<!-- .slide: data-background="inputs/img/Church-Turing-Thesis.png" data-background-size="contain" -->

---

### Algorithms vs. Languages

+ The <a class="highlight-green">*Church-Turing Thesis*</a> 
  is one of the most important ideas in computer science.
  
+ The impact of the models of Church and Turing goes 
  well beyond the thesis itself.
  <!-- .element: class="fragment fade-left" -->

+ But the two models have impacted two disparate communities.
  <!-- .element: class="fragment fade-left" -->

+ Turing Machine $\rightsquigarrow$ Algorithms and Complexity
  <!-- .element: class="fragment fade-left" -->

+ Lambda Calculus $\rightsquigarrow$ Programming Languages
  <!-- .element: class="fragment fade-left" -->

---

### Efficiency vs. Structure

The impact and separation is not accidental.

<p>Two sources of beauty in programs: </p><!-- .element: class="fragment fade-up" -->

<div><a class="highlight-red">*efficiency*</a></div><!-- .element: class="fragment fade-right" -->
<div><a class="highlight-blue">*structure*</a></div><!-- .element: class="fragment fade-left" -->

---

### Turing Machine $\leftrightsquigarrow$ Algorithms

<div><a class="highlight-blue">*efficiency*</a></div>
<!-- .element: class="fragment fade-up" -->
<p>Turing Machines are good at measuring resources</p>
<!-- .element: class="fragment fade-up" -->

+ <div>**Axiomatic complexity theory**  
  P vs. NP, polynomial hierarchy, P-space</div>
  <!-- .element: class="fragment fade-left" -->
+ <div>**asymptotic analysis** of algorithms</div>
  <!-- .element: class="fragment fade-left" -->
+ <div>**Cryptography** is based on complexity</div>
  <!-- .element: class="fragment fade-left" -->
+ <div>**Learning theory** based on learning power of Turing machines</div>
  <!-- .element: class="fragment fade-left" -->

---

### $\lambda$-Calculus $\leftrightsquigarrow$ Languages

<div><a class="highlight-blue">*structure*</a></div>
<!-- .element: class="fragment fade-up" -->
<p>$\lambda$-Calculus is good at composition and abstraction</p>
<!-- .element: class="fragment fade-up" -->

+ <div>**call-by-value**, **lexical scoping**, **recursion**</div>
  <!-- .element: class="fragment fade-left" -->
+ <div>**lambda abstractions, higher-order-functions**   
  (recently even in C++ and Java!)</div>
  <!-- .element: class="fragment fade-left" -->
+ <div>**denotational semantics** and **type theory**  
  the "theory of abstraction"</div>
  <!-- .element: class="fragment fade-left" -->
+ <div>**proof assistants** (e.g. Agda, Coq, NuPRL, Isabelle)</div>
  <!-- .element: class="fragment fade-left" -->
+ <div>**languages** (e.g., Lisp, SML, Haskell, Scala...</div>
  <!-- .element: class="fragment fade-left" -->
  <div style="text-align:right">...and now Java, Python, JavaScript)</div>
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

<div style="text-align:left">**Turing** was way ahead of his time</div>
<!-- .element: class="fragment fade-left" -->

<div style="text-align:right">**Church** was way *way* ahead of his time</div>
<!-- .element: class="fragment fade-right" -->

+ $\lambda$-calculus does not define a reduction order
  <!-- .element: class="fragment fade-left" -->

+ **Virtue:** $\lambda$-calculus is inherently parallel!
  <!-- .element: class="fragment fade-left" -->

+ **Problem:** no obvious cost model since   
  number of steps depends on reduction order  
  and some orders are very inefficient
  <!-- .element: class="fragment fade-left" -->

---

### Proposal of Acar, Bleloch, Harper, Reppy 

1. Fix an order that is parallel and cheap to evaluate.  
2. Base a cost model on it.  
3. Bound cost when mapped to standard models.  

Once we have an order, we can:
+ count number of reductions (work)  
+ count number of parallel steps (depth or span)

---

### Their Conclusion

+ **Next 50 years:** need to integrate Complexity/Algorithms and
  Programming Language Theory.

+ **Cost models:** should be based on languages, not machines. 
  Particularly important for parallelism.

+ **Other opportunities:** Verification, type-theory and complexity,
  probabilistic programming, programs-as-data, cryptography
  and PL, game-theory and PL.

---

### End of Part 1

Links to further reading on 

**Parallelism and Cost Semantics**

https://www.cs.cmu.edu/~rwh/papers.html

(time for a break)
<!-- .element: class="fragment fade-left" -->
