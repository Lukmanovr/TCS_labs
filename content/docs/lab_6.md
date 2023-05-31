---
title: Lab 6 - PDT
type: docs
weight: 6
BookToC: true
---

# **Lab Session #6**

# Agenda

- PDT - Push-Down Transducer

------

## PD transducer
### **Formal definition**

A Pushdown Transducer (PDT) is a tuple {{< katex >}} T = ⟨Q, I, Γ, δ, q_0, Z_0, F⟩ {{< /katex >}} where:

- {{< katex >}}Q{{< /katex >}} is a finite set of states;

- {{< katex >}}I{{< /katex >}} and {{< katex >}}Γ{{< /katex >}} are the finite sets, the input and stack alphabets.;

- {{< katex >}}δ{{< /katex >}}, the transition function, is a partial function from {{< katex >}} (Q)×(I \cup \{ε\}) × (Γ) {{< /katex >}} to the set of finite subsets of {{< katex >}}(Q)×(Γ^*){{< /katex >}}

- {{< katex >}}q_0 \in Q{{< /katex >}} is the initial state;

- {{< katex >}}Z_0 \in Γ{{< /katex >}} is the initial stack symbol;

- {{< katex >}}F \subseteq Q{{< /katex >}} is the set of accepting states.

- {{< katex >}}O{{< /katex >}} is the output alphabet

- {{< katex >}}η : Q×(I \cup \{ε\})× Γ → Q^*{{< /katex >}}

------

### **Exercises - Part 1**

1. Build PDT that accepts {{< katex >}} x \in L_1 {{< /katex >}} where 
{{< katex >}}L_1 = \{a^nb^m | n \geq 1 \wedge n \leq m\}{{< /katex >}} and translates it into {{< katex >}} a^nb^n {{< /katex >}}

2. Build PDT that recognizes {{< katex >}} L_2 = \{xc | x \in \{a, b\}^+\} {{< /katex >}} and reverses it

------

**Solutions**:

{{< expand >}}

**Solution(1)**:

<p> A PDT that accepts {{< katex >}} x \in L_1 {{< /katex >}} where {{< katex >}}L_1 = \{a^nb^m | n \geq 1 \wedge n \leq m\}{{< /katex >}} and translates it into {{< katex >}} a^nb^n {{< /katex >}} </p>

![Solution 1](/images/lab6/ex1_sol.svg)

**Solution(2)**:
<p> A PDT that recognizes {{< katex >}} L_2 = \{xc | x \in \{a, b\}^+\} {{< /katex >}} and reverses it </p>

![Solution 2](/images/lab6/ex_1.2_sol.svg)
{{< /expand >}}

------

### **Exercises - Part 2**

Build DPDT that accepts the following laguages:

- {{< katex >}} L_1 = \{a^nb^ma^n | n \geq 1 \wedge m \leq 1\}{{< /katex >}}, and translates it into {{< katex >}}a^nb^m {{< /katex >}}

- {{< katex >}} L_2 = \{a^ib^ic^k | i, j, k \in \mathbb{N} {{< /katex >}} and {{< katex >}} i + k = j\} {{< /katex >}}, and translates it into {{< katex >}}a^ib^ic^k{{< /katex >}}

- {{< katex >}}L_3 = \{xcy | x, y \in \{a, b\}^* \wedge |x| > 0 \wedge |y| > 0 \wedge y \neq x^R\} {{< /katex >}}, (where {{< katex >}} x^R {{< /katex >}}) is the reversed string {{< katex >}} x {{< /katex >}}, the alphabet is {{< katex >}}I = \{a, b, c\} {{< /katex >}} and translates it into {{< katex >}} y {{< /katex >}}

- {{< katex >}}L_4 = \{a^mb^m | m, n \in \mathbb{N} {{< /katex >}} and {{< katex >}} n \leq m \leq 2n\} {{< /katex >}}, and translates it into {{< katex >}}a^nb^n{{< /katex >}}

------

**Solutions**:

{{< expand >}}

**Solution(1)**:

<p> A PDT that accepts {{< katex >}} L_1 = \{a^nb^ma^n | n \geq 1 \wedge m \leq 1\}{{< /katex >}}, and translates it into {{< katex >}}a^nb^m {{< /katex >}} </p>

![Solution 2_1](/images/lab6/ex_2.1_sol.svg)

**Solution(2)**:

<p> A PDT that accepts {{< katex >}} L_2 = \{a^ib^ic^k | i, j, k \in \mathbb{N}\ and\ i + k = j\} {{< /katex >}}, and translates it into {{< katex >}}a^ib^ic^k{{< /katex >}}

![Solution 2_2](/images/lab6/ex_2.2_sol.svg)

{{< /expand >}}

------

### **Extra exercise (optional)**

Consider the language of well-formed parentheses of the arithmetic expressions (binary operations). Examples of strings belonging to the language are:

- {{< katex >}} (a + b) {{< /katex >}}

- {{< katex >}} ((a) + (b + c)) {{< /katex >}}

- {{< katex >}} ((a + b)) {{< /katex >}}

Build PDT that recognises this language and translates it into reverse polish notation. For simplicity, consider the following alphabet {{< katex >}} I = \{a, (, ), +\} -- {{< /katex >}} a single symbol ('a') that represents terms 'a', 'b', 'c', {{< katex >}} \ldots {{< /katex >}}. And a single operator ('+').

------