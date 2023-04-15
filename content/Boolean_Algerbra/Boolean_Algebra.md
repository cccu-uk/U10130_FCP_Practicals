# Workshop on Boolean Algebra

This **Workshop on Boolean Algebra** is designed for you to practice Boolean equations and Boolean Algebra laws.

## Minimising Boolean Expressions

We can use Commutative, Associative, and Distributive Laws to manipulate Boolean expressions.

---
### BOOLEAN LAWS

**Commutative Laws**

 - \\(A + B \Longleftrightarrow B + A\\)

 - \\(A.B \Longleftrightarrow B.A\\)

**Associative Laws**

 - \\((A + B) + C \Longleftrightarrow A + (B + C)\\)

 - \\((A.B).C \Longleftrightarrow A.(B.C)\\)

**Distributive Laws**

 - \\(A + (B + C) \Longleftrightarrow (A + B) + (A + C)\\)

 - \\(A.(B.C) \Longleftrightarrow (A.B) + (A.C)\\)

**Axioms**

The following rules (axioms) can also be used to minimise Boolean Expressions:

1\.  
  - A literal by itself cancels out any term that contains it
    (Absorption):

    - \\(A + A.B + A.B.C \Longrightarrow A + \\)~~A.B~~ + ~~A.B.C~~ \\(\Longrightarrow A\\)

2\.
  -  A literal by itself knocks out its NOT'ed opposite that appears in any 'minterm' (Absorption):

     - \\(\overline{A} + A.\overline{B} + A.C \Longrightarrow \overline{A} +\\)  ~~A~~ \\(.\overline{B} +\\) ~~A~~ \\(.C \Longrightarrow \overline{A} + \overline{B} + C\\)

---

## Exercise: One

Minimise the following Boolean Expressions:

1\.  \\(\hspace{1.75em}S = \overline{A} + A.C + \overline{B}.C\\)

---
<details>
<summary><b>Click for Solution</b></summary>
<p></p>

\\(S = \overline{A} + \\)~~A~~\\(.C + \overline{B}.C\\)

\\(S = \overline{A} + C +\\) ~~B.C~~

\\(S = \overline{A} + C\\)
</details>

---
2\.  \\(\hspace{1.75em}S = A.C + A.B.C + A.B.\overline{C}\\)

---
<details>
<summary><b>Click for Solution</b></summary>
<p></p>

\\(S = A.C + A.B.(C + \overline{C})\\)

\\(S = A.C + A.B.(1)\\)

\\(S = A.C + A.B\\)

</details>

---
3\.  \\(\hspace{1.75em}S = \overline{B} + A.B + A.\overline{B}.C\\)

---
<details>
<summary><b>Click for Solution</b></summary>
<p></p>

\\(S = \overline{B} + A.\\) ~~B~~ \\(+\\) ~~A.B.C~~

\\(S = \overline{B} + A\\)

</details>

---
4\.  \\(\hspace{1.75em}S = \overline{A}.\overline{B}.\overline{C} + A.\overline{B}.\overline{C} + A.C\\)

---
<details>
<summary><b>Click for Solution</b></summary>
<p></p>

\\(S = \overline{B}.\overline{C}.(A  + \overline{A}) + A.C\\)

\\(S = \overline{B}.\overline{C}.(1) + A.C\\)

\\(S = \overline{B}.\overline{C} + A.C\\)

</details>

---

5\.  \\(\hspace{1.75em}S = C + A.\overline{C} + B.C + A.B.C\\)

---
<details>
<summary><b>Click for Solution</b></summary>
<p></p>

\\(S = C + A.\\)~~C~~ \\(+\\) ~~B.C~~ \\(+\\) ~~A.B.C~~

\\(S = C + A\\)

</details>

---

6\.  \\(\hspace{1.75em}S = A.B.\overline{C} + A.B.C + A.\overline{B}.\overline{C} + A.\overline{B}.C + \overline{A}.B.C + \overline{A}.B.\overline{C}\\)

    
---
<details>
<summary><b>Click for Solution</b></summary>
<p></p>

\\(S = A.B.(\overline{C} + C) + A.\overline{B}.(\overline{C} + C) + \overline{A}.B.(C + \overline{C})\\)

\\(S = A.B.(1) + A.\overline{B}.(1) + \overline{A}.B.(1)\\)

\\(S = A.B + A.\overline{B} + \overline{A}.B\\)

\\(S = A.(B + \overline{B}) + \overline{A}.B\\)

\\(S = A.(1) + \overline{A}.B\\)

\\(S = A +\\)~~A~~\\(.B\\)

\\(S = A + B\\)

</details>

---


7\.  \\(\hspace{1.75em}S = A + B.C + \overline{A}.B.C\\)

---
<details>
<summary><b>Click for Solution</b></summary>
<p></p>

\\(S = A + B.C +\\) ~~A~~ \\(.B.C\\)

\\(S = A + B.C +\\) ~~B.C~~

\\(S = A + B.C\\)

</details>

---


8\.  \\(\hspace{1.75em}S = B + \overline{A}.B.\overline{C} + A.B.\overline{C} + \overline{A}.C\\)

---
<details>
<summary><b>Click for Solution</b></summary>
<p></p>

\\(S = B +\\) ~~A.B.C~~ \\(+\\) ~~A.B.C~~ \\(+ \overline{A}.C\\)

\\(S = B + \overline{A}.C\\)

</details>

---


## Exercise: Two

For each of the following truth tables produce the standard **Sum of the Product Terms** for the output \\(S\\), then reduce the Boolean expression to a simpler expression using Boolean algebra.

1\.

|**A**|**B**|**S**|
|-------|-------|-------|
|0| 0| 1|
|0| 1| 1|
|1| 0| 1|
|1| 1| 0|                
                  
 ---
<details>
<summary><b>Click for Solution</b></summary>
<p></p>

\\(S = \overline{A}.\overline{B} + \overline{A}.B + A.\overline{B}\\)

\\(S = \overline{A}.(\overline{B} + B) + A.\overline{B}\\)

\\(S = \overline{A}.(1) + A.\overline{B}\\)

\\(S = \overline{A} + A.\overline{B}\\)

\\(S = \overline{A} +\\) ~~A~~}\\(.\overline{B}\\)

\\(S = \overline{A} + \overline{B}\\)

</details>

---
                            
2\.

|**A** | **B** |**S**|
|-------|------|------|
|0 | 0|  0| 
|0 | 1|  1| 
|1 | 0|  1|
|1 | 1|  0|                
                  
 ---
<details>
<summary><b>Click for Solution</b></summary>
<p></p>

\\(S = \overline{A}B + A\overline{B}\\)

</details>

---
                 

3\.

|**A**|**B**|**C**|**S**|
|-------|-------|-------|-------|
|0 | 0 | 0 | 1|
|0 | 0 | 1 | 1|
|0 | 1 | 0 | 0|
|0 | 1 | 1 | 0|
|1 | 0 | 0 | 0|
|1 | 0 | 1 | 0|
|1 | 1 | 0 | 0|
|1 | 1 | 1 | 0|                        
                                                
  ---
<details>
<summary><b>Click for Solution</b></summary>
<p></p>
                        
\\(S = \overline{A}.\overline{B}.\overline{C} + \overline{A}.\overline{B}.C\\)

\\(S = \overline{A}.\overline{B}.(\overline{C} + C)\\)

\\(S = \overline{A}.\overline{B}.(1)\\)

\\(S = \overline{A}.\overline{B}\\)

</details>

---

4\.

|**A**|**B**|**C**|**S**|
|-----|-----|-----|-----|         
|0|  0 | 0 | 0|
|0|  0 | 1 | 1|
|0|  1 | 0 | 0|
|0|  1 | 1 | 1|
|1|  0 | 0 | 0|
|1|  0 | 1 | 1|
|1|  1 | 0 | 0|
|1|  1 | 1 | 1|                        
                                             
  ---
<details>
<summary><b>Click for Solution</b></summary>
<p></p>

\\(S = \overline{A}.\overline{B}.C + \overline{A}.B.C + A.\overline{B}.C + A.B.C\\)

\\(S = \overline{B}.C.(\overline{A} + A) + B.C.(\overline{A} + A)\\)

\\(S = \overline{B}.C.(1) + B.C.(1)\\)

\\(S = \overline{B}.C + B.C\\)

\\(S = C.(\overline{B} + B)\\)

\\(S = C.(1)\\)

\\(S = C\\)

</details>

---

5\.

|**A**  |**B**  |**C** |**S**|
|-------|-------|-------|-------|
|0|  0 | 0|  1|
|0|  0 | 1|  1|
|0|  1 | 0|  0|
|0|  1 | 1|  1|
|1|  0 | 0|  0|
|1|  0 | 1|  0|
|1|  1 | 0|  0|
|1|  1 | 1|  1|                          
                                                
 ---
<details>
<summary><b>Click for Solution</b></summary>
<p></p>

\\(S = \overline{A}.\overline{B}.\overline{C} + \overline{A}.\overline{B}.C + \overline{A}.B.C + A.B.C\\)

\\(S = \overline{A}.\overline{B}.(\overline{C} + C) + B.C.(\overline{A} + A)\\)

\\(S = \overline{A}.\overline{B}.(1) + B.C.(1)\\)

\\(S = \overline{A}.\overline{B} + B.C\\)

</details>

---
                         
6\.

|**A**|   **B**|   **C**|   **S**|
|-------|-------|-------|-------|
| 0|  0 | 0 | 0|
| 0|  0 | 1 | 0|
| 0|  1 | 0 | 1|
| 0|  1 | 1 | 1|
| 1|  0 | 0 | 0|
| 1|  0 | 1 | 1|
| 1|  1 | 0 | 1|
| 1|  1 | 1 | 1|                         
                                                                    
 ---
<details>
<summary><b>Click for Solution</b></summary>
<p></p>

\\(S = \overline{A}.\overline{B}.\overline{C} + \overline{A}.\overline{B}.C + \overline{A}.B.C + A.B.C\\)

\\(S = \overline{A}.\overline{B}.(\overline{C} + C) + B.C.(\overline{A} + A)\\)

\\(S = \overline{A}.\overline{B}.(1) + B.C.(1)\\)

\\(S = \overline{A}.\overline{B} + B.C\\)
</details>

---
                    

7\.

|**A** |  **B**|   **C**|   **S**|
|-------|-------|-------|-------|
|0|  0|  0 | 0|
|0|  0|  1 | 0|
|0|  1|  0 | 1|
|0|  1|  1 | 1|
|1|  0|  0 | 0|
|1|  0|  1 | 1|
|1|  1|  0 | 1|
|1|  1|  1 | 1|                         
                          
 ---
<details>
<summary><b>Click for Solution</b></summary>
<p></p>

\\(S = \overline{A}.B.\overline{C} + \overline{A}.B.C + A.\overline{B}.C + A.B.\overline{C} + A.B.C\\)

\\(S = \overline{A}.B.(\overline{C} + C) + A.\overline{B}.C + A.\overline{B}.(\overline{C} + C)\\)

\\(S = \overline{A}.B.(1) + A.\overline{B}.C + A.\overline{B}.(1)\\)

\\(S = \overline{A}.B + A.\overline{B}.C + A.\overline{B}\\)

\\(S = B.(\overline{A} + A) + A.\overline{B}.C\\)

\\(S = B.(1) + A.\overline{B}.C\\)

\\(S = B + A.\overline{B}.C\\)

\\(S = B + A.\\) ~~B~~ \\(.C\\)

\\(S = B + A.C\\)

</details>

---

 8\.  

|**A**|**B**|**C**|**S**|
|-------|-------|-------|-----|
|0|  0|  0|  0|
|0|  0|  1|  0|
|0|  1|  0|  0|
|0|  1|  1|  1|
|1|  0|  0|  1|
|1|  0|  1|  1|
|1|  1|  0|  1|
|1|  1|  1|  1|      

---
<details>
<summary><b>Click for Solution</b></summary>
<p></p>

\\(S = \overline{A}.B.C + A.\overline{B}.\overline{C} + A.\overline{B}.C + A.B.\overline{C} + A.B.C\\)

\\(S = \overline{A}.B.C + A.\overline{B}.(\overline{C} + C) + A.B.(\overline{C} + C)\\)

\\(S = \overline{A}.B.C + A.\overline{B}.(1) + A.B.(1)\\)

\\(S = \overline{A}.B.C + A.\overline{B} + A.B\\)

\\(S = \overline{A}.B.C + A.(\overline{B} + B)\\)

\\(S = \overline{A}.B.C + A.(1)\\)

\\(S = \overline{A}.B.C + A\\)

\\(S =\\) ~~A~~ \\(B.C + A\\)

\\(S = B.C + A\\)

</details>

---                          