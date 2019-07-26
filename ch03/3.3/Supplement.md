# Exercises for Section 3.3
## Supplement of problems only in Second Edition(Also named Dragon Book Two)

### 3.3.8
Proof:
For regexs with complemented character class, we replace all complemented character class with a character class with no ^.
Now prove that such replacement is always feasible.

Let class A denotes the original complemented character class we want to replace.
For all characters in Σ, if it does not appear in A, add it to character class B.
Then, we prove class A is equivalent to class B.
Any character can be matched to A iff it does not appear in A.
Any character can be matched to B iff it appears in B.
Every character appears in B iff it does not appear in A.
Q.E.D.

### 3.3.11
We define a function f
If c is not a special character in Regex, f(c)=c
Otherwise, f(c)=\c
Define C shorthand of a|b|c|d|..|A|B|C|...|0|1|2|...|,|\.|\*|...
(Which means, we replace C by a|b|c|d|..|A|B|C|...|0|1|2|...|,|\.|\*|... )

's':
Write s as cS' (concatenation)
's' can be recursively translated as f(c)f(S')  (concatenation)

'\c' can be translated as f(c)

* can be translated as C*

? can be translated as C

[s]:
Write s as cS' (concatenation)
[s] can be recursively translated as f(c)|f(S')

### 3.3.12

_ can be translated as .
% can be translated as .*
Suppose e is a escape character.
e_ e% and ee can be translated as e.
e can be writen as what it means in SQL. Then we translated the sequence from SQL into Regex.
