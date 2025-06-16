# Principles of Computer Science (1e, 1st printing) Errata

Table of Contents Page 3:
Bibliography 729 => Bibliography 731

Page 69:
Figure 4.11: The state q2 should not be labeled as a final state. (Credit: Diego Costa)

Page 141:
The footnote should say "A left-Riemann sum *over*approximates the area, whereas a right-Riemann sum provides an *under*approximation."

Page 150:
Figure 5.15: Four Cloclwise Rotations => Figure 5.15: Four Clockwise Rotations

Page 162:
Listing 5.136: The newline and spaces between the two parts of the `symbol` rule should be removed.

Page 313:
Listing 7.153: should have 60 and 80 swapped.

Page 329:
Footnote 1 is, in fact, **not** presented as an exercise.

Page 336:
Listing 7.201: "firsttesian-product?" => "cartesian-product?"

Page 347:
Footnote 1 should be on the next page.

Page 477:
Figure 8.7: Add a space after the `"include"` string.

Page 531:
Add this as a 5 star exercise. This should also serve as an explanation for why <code>gensym</code> doesn't always work.
Unfortunately not all of the problems are resolved with our "semi-hygienic macro" solution. Consider the following macro in our system:
<pre>
(define-macro (unhygienic-macro z)
  (let ([q 100])
    (set! z (+ q z))))
</pre>

But then we, sloppily so, redefine <code>set!</code> in our system to be something else outside the macro:
<pre>
(define set! +)
</pre>
Our macro system is only semi-hygienic for bound variables. Free variables or identifiers can be captured by other definitions outside the macro, and are therefore not hygienic.
If we wanted the macro to be truly hygienic, then all identifiers/symbols/variables would need to be uninterned. We leave this as a very challenging exercise to the reader.


Page 591:
Listing 9.19: "syscallN the address" => "syscall" 
