---
title: Lab Session 4
type: docs
weight: 4
BookToC: true
---
# Lab #4

## Agenda

- Recap: Pumping lemma
- Exercises  

## Pumping lemma

Given a regular language {{< katex >}} \bf L {{< /katex >}} \
there exists an integer (critical length) {{< katex >}} \bf m {{< /katex >}} such that \
for any string {{< katex >}} \bf w \isin L {{< /katex >}} with length {{< katex >}} \bf |w| \ge m {{< /katex >}} \
we can find a split {{< katex >}} \bf w = x \ y \ z {{< /katex >}} such that:
- {{< katex >}} \bf |x \ y| \leq m {{< /katex >}}
- {{< katex >}} {\bf |y|} \ge 1 {{< /katex >}}
- {{< katex >}} \bf x \ y^i \ z \isin L {{< /katex >}} for all {{< katex >}} i \ge 0 {{< /katex >}}

## Pumping lemma: contrapositive
Given a language {{< katex >}} \bf L {{< /katex >}}. If we show that \
**for any** integer {{< katex >}} m \ge 1 {{< /katex >}} \
**there exists** a string {{< katex >}} w \isin L {{< /katex >}} such that {{< katex >}} |w| \ge m {{< /katex >}} \
and **for all** possible splits {{< katex >}} x, y, z \isin \Sigma^* {{< /katex >}} with
- {{< katex >}} |x \ y| \leq m {{< /katex >}}
- {{< katex >}} |y| \ge 1 {{< /katex >}}
- {{< katex >}} x \ y^i \ z \isin L {{< /katex >}} \

**there exists**: {{< katex >}} i \isin \natnums {{< /katex >}}
such that {{< katex >}} x \ y^i \ z \notin L {{< /katex >}}. \
Then, applying the Pumping lemma for regular languages, one can
deduce that {{< katex >}} L {{< /katex >}} is not regular.

---
## Exercises
Using Pumping lemma prove that {{< katex >}} L_1, \ L_2, \ L_3 {{< /katex >}} and {{< katex >}} L_4 {{< /katex >}} are not regular
languages:
1. {{< katex >}} L_1 = \{vv^R | v \isin \Sigma_1^* \} \ {{< /katex >}}  where  {{< katex >}} \ \Sigma_1 = \{a, \ b\} {{< /katex >}}

{{< accordion title="Solution:" >}}
<br>
Let’s take an arbitrary integer {{< katex >}} m \ge 1 {{< /katex >}}. <br>
Let {{< katex >}} w = a^m b^m b^m a^m {{< /katex >}} <br>
{{< katex >}} |w| = 4m \ge m, \ w \isin L {{< /katex >}}. <br>
Split {{< katex >}} w {{< /katex >}} in the form {{< katex >}} xyz {{< /katex >}}: as {{< katex >}} |xy| \leq m {{< /katex >}}  
and <span style="white-space: nowrap;">{{< katex >}} w = a^m b^m b^m a^m{{</katex>}},</span> 
<span style="white-space: nowrap;">{{< katex >}}y = a^k {{< /katex >}},</span>
<span style="white-space: nowrap;">{{< katex >}}\ k \ge 1 {{< /katex >}}.</span> <br>
Let’s look at {{< katex >}} xy^2z {{< /katex >}}.
It will have the form {{< katex >}} a^{m+k} b^m b^m a^m {{< /katex >}}. <br>
As {{< katex >}} k \ge 1, xy^2z \notin L {{< /katex >}}. <br>
We have shown that for any {{< katex >}} m {{< /katex >}} we can find
<span style="white-space: nowrap;">{{< katex >}} w \isin L {{< /katex >}}</span>, such that
<span style="white-space: nowrap;">{{< katex >}} |w| \ge m {{< /katex >}} </span>
and for all
<span style="white-space: nowrap;">{{< katex >}} x, \ y, \ z \isin \Sigma^*{{< /katex >}}</span> with
<span style="white-space: nowrap;">{{< katex >}} |xy| \leq m {{< /katex >}}</span> and
<span style="white-space: nowrap;">{{< katex >}} |y| \ge 1 {{< /katex >}}</span> and
<span style="white-space: nowrap;">{{< katex >}} w = xyz {{< /katex >}}</span> there exists 
<span style="white-space: nowrap;">{{< katex >}} i \isin N {{< /katex >}}</span> such that
<span style="white-space: nowrap;">{{< katex >}}xy^iz \notin L {{< /katex >}}.</span> <br>
So, applying Pumping lemma we can deduce that {{< katex >}} L {{< /katex >}} is <strong>not regular</strong>.

{{< /accordion >}}

2. {{< katex >}} L_2 = \{ v| v {{< /katex >}} has an equal number of {{< katex >}} a {{< /katex >}}’s and {{< katex >}} b {{< /katex >}}’s
{{< katex >}} \} \ {{< /katex >}} over {{< katex >}} \ \Sigma_2 = \{ a, \ b \} {{< /katex >}}

{{< accordion title="Solution:" >}}
<br>
Let’s take an arbitrary integer {{< katex >}} m \ge 1 {{< /katex >}}. <br>
Let {{< katex >}} w = a^m b^m {{< /katex >}} <br>
{{< katex >}} |w| = 2m \ge m, \ w \isin L {{< /katex >}}. <br>
Split {{< katex >}} w {{< /katex >}} in the form {{< katex >}} xyz {{< /katex >}}: 
as {{< katex >}} |xy| \leq m {{< /katex >}} and {{< katex >}} w = a^m b^m {{< /katex >}},
<span style="white-space: nowrap;">{{< katex >}} y = a^k {{< /katex >}},</span>
<span style="white-space: nowrap;">{{< katex >}}k \ge 1 {{< /katex >}}.</span> <br>
Let’s look at {{< katex >}} xy^2z {{< /katex >}}. It will have the form
{{< katex >}} a^{m+k}b^m {{< /katex >}}. As 
<span style="white-space: nowrap;">{{< katex >}} k \ge 1 {{< /katex >}},</span>
<span style="white-space: nowrap;">{{< katex >}} xy^2z \notin L {{< /katex >}}.</span> <br>
We have shown that for any {{< katex >}} m {{< /katex >}} we can find 
{{< katex >}} w \isin L {{< /katex >}}, such that
<span style="white-space: nowrap;">{{< katex >}} |w| \ge m {{< /katex >}}</span> and for all
<span style="white-space: nowrap;">{{< katex >}} x, y, z \isin \Sigma^* {{< /katex >}}</span> with
<span style="white-space: nowrap;">{{< katex >}} |xy| \leq m {{< /katex >}}</span> and
<span style="white-space: nowrap;">{{< katex >}} |y| \ge 1 {{< /katex >}}</span> and
<span style="white-space: nowrap;">{{< katex >}} w = xyz {{< /katex >}}</span> there exists
<span style="white-space: nowrap;">{{< katex >}} i \isin N {{< /katex >}} </span> such that
<span style="white-space: nowrap;">{{< katex >}} xy^iz \notin L {{< /katex >}}.</span> <br>
So, applying Pumping lemma we can deduce that {{< katex >}} L {{< /katex >}} is <strong>not regular</strong>.
{{< /accordion >}}

3. {{< katex >}} L_3 = \{ a^{n!} | n \ge 0 \} \ {{< /katex >}}  over {{< katex >}} \ \Sigma_3 = \{ a \} {{< /katex >}}

{{< accordion title="Solution:" >}}
<br>
Let’s take an arbitrary integer {{< katex >}} m \ge 1 {{< /katex >}}. <br>
Let {{< katex >}} w = a^{m!}{{< /katex >}} <br>
{{< katex >}} |w| = m! \ge m,w \isin L {{< /katex >}}. <br>
Split {{< katex >}}w{{< /katex >}} in the form {{< katex >}}xyz{{< /katex >}}:
as {{< katex >}}|xy| \leq m {{< /katex >}} and
<span style="white-space: nowrap;">{{< katex >}} \ w = a^{m!}{{</katex>}}, </span>
<span style="white-space: nowrap;">{{<katex>}}\ y = a^k{{</katex>}},</span>
<span style="white-space: nowrap;">{{<katex>}}\ m \ge k \ge 1 {{< /katex >}}.</span> <br>
Let’s look at {{< katex >}} xy^2z{{< /katex >}}. It will have the form
{{< katex >}} a^{m!+k} {{< /katex >}}. <br>
As {{< katex >}} k \ge 1, \ m! < m! + k {{< /katex >}}. <br>
As {{< katex >}} m \ge k, \ m! + k \leq m! + m {{< /katex >}}. <br>
By algebra, {{< katex >}} m! + m < (m + 1)!^1 {{< /katex >}}, as
<span style="white-space: nowrap;">{{< katex >}}(m + 1)! = m! + m! ∗ m {{< /katex >}}</span> <br>
So for {{< katex >}} m > 1 {{< /katex >}} we get that
{{< katex >}} m! < m! + k < (m + 1)! {{</katex >}},
which means  that there is no such
<span style="white-space: nowrap;">{{< katex >}} p \isin \natnums {{< /katex >}}</span> that
<span style="white-space: nowrap;">{{< katex >}} (m! + k) = p!{{< /katex >}}, </span>
so <span style="white-space: nowrap;">{{< katex >}} xy^2z \notin L {{< /katex >}}</span><br>
For {{< katex >}} m = 1,w = a, {{< /katex >}} 
so {{< katex >}} y = a {{< /katex >}}, and the string
<span style="white-space: nowrap;">{{< katex >}} xy^3 z = aaa \notin L {{< /katex >}}</span>
Applying Pumping lemma we can deduce that {{< katex >}}L_3{{</katex >}} is <strong>not regular</strong>. <br> <br>
<span style="font-size: 14px;"> {{< katex >}} ^1{{< /katex >}}for {{< katex >}}m > 1{{< /katex >}} </span>
{{< /accordion >}}

4. {{< katex >}} L_4 = \{ a^n b^l c^{n+l} | n, l \ge 0 \} \ {{< /katex >}} over {{< katex >}} \ \Sigma_4 = \{ a, b, c \} {{< /katex >}}

{{< accordion title="Solution:" >}}
<br>
Let’s take an arbitrary integer {{< katex >}}m \ge 1{{< /katex >}}. <br>
Let {{< katex >}} w = a^mb^mc^{2m} {{< /katex >}}<br>
{{< katex >}} |w| = 4m \ge m,w \isin L{{< /katex >}}. <br>
Split {{< katex >}}w{{< /katex >}} in the form {{< katex >}}xyz{{< /katex >}}:
as {{< katex >}} |xy| \leq m {{< /katex >}} and
<span style="white-space: nowrap;">{{< katex >}} w = a^mb^mc^{2m}{{</katex>}},</span>
<span style="white-space: nowrap;">{{<katex>}}\ y = a^k{{</katex>}},</span>
<span style="white-space: nowrap;">{{<katex>}}\ k \ge 1 {{< /katex >}}.</span> <br>
Let’s look at {{< katex >}} xy^2 z {{< /katex >}}. 
It will have the form {{< katex >}} a^{m+k} b^mc^{2m}{{< /katex >}}. <br>
As {{< katex >}}k \ge 1, \ xy^2z \notin L{{< /katex >}}, applying Pumping lemma we can deduce that
{{< katex >}} L_4{{< /katex >}} is <strong>not regular</strong>.
{{< /accordion >}}