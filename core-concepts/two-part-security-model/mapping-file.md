# Mapping File

<figure><img src="../../.gitbook/assets/json file icon.png" alt="" width="188"><figcaption></figcaption></figure>

## Definition

A Mapping File is a private file that serves as the only key to recover the [Original Keys](../original-secret-vs-decoy-text.md) from the Decoy Text. It stores mapping information in the form of structured technical data, not the original sensitive data itself.

Without the correct Mapping File, recovering the Original Secret is impossible, even if the Decoy Text is fully available.

## Characteristics

A Mapping File has the following key characteristics:

* Stored as a `.json` file
* Does not contain the Original Secret
* Contains structured ASCII data, not secret text
* Safe when standing alone
* Highly sensitive as a recovery component
* Deterministic and sequential

The Mapping File is designed so that it cannot be interpreted or used directly, even if the file is exposed.

## What it contains

Technically, a Mapping File contains:

* **95 standard ASCII characters repeated in a controlled manner**

> The Mapping File includes all 95 standard ASCII characters (A-Z, a-z, space, 0-9, and symbols), where each character is repeated up to the highest frequency of any character found in the original seed phrase or sensitive data.

```
A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
a b c d e f g h i j k l m n o p q r s t u v w x y z
(space)
0 1 2 3 4 5 6 7 8 9
! " # $ % & ' ( ) * + , - . /
: ; < = > ?
@ [ \ ] ^ _
` { | } ~
```

* **The data is arranged sequentially**

This structure ensures that:

* The Mapping File does not contain only the characters used in the sensitive data
* There is no way to determine which characters are relevant
* There is no information about the order, value, or content of the Original Secret

With this approach, the Mapping File remains safe even when standing alone, because its contents are a complete character set obscured through frequency and ordering, not a direct representation of sensitive data.

#### Mapping File Formula

The Mapping File is defined as:

$$
M = \Sigma_{95} \times F_{max}(K)
$$

> The mapping file equals the full set of 95 ASCII characters multiplied by the highest character frequency of the original key.

Where:

* _**M**_: Mapping File
* **Σ₉₅**: All 95 printable ASCII characters
* **Fₘₐₓ**: Highest character frequency in K
* **K**: Original key

<details>

<summary><strong>Example: Mapping File Implementation</strong></summary>

#### Step 1: Frequency Analysis

From the input:

{% code title="User's Original Key" lineNumbers="true" %}
```
password123
```
{% endcode %}

Character frequency:

* `s` → appears **2 times** (highest frequency)

Therefore:

* **High-frequency count = 2**
* Mapping dimension multiplier = **2**&#x20;

#### Step 2: ASCII Mapping Slots

Decoy Phrase uses the **95 standard ASCII characters**, which include:

* Uppercase letters (A–Z)
* Lowercase letters (a–z)
* Numbers (0–9)
* Space
* Symbols

Because the highest frequency is **2**, the mapping slots becomes:

{% code title="Uppercase Letters (A–Z)" lineNumbers="true" %}
```
A
A
B
B
C
C
D
D
E
E
F
F
G
G
H
H
I
I
J
J
K
K
L
L
M
M
N
N
O
O
P
P
Q
Q
R
R
S
S
T
T
U
U
V
V
W
W
X
X
Y
Y
Z
Z
```
{% endcode %}

{% code title="Lowercase Letters (a–z)" lineNumbers="true" %}
```
a
a
b
b
c
c
d
d
e
e
f
f
g
g
h
h
i
i
j
j
k
k
l
l
m
m
n
n
o
o
p
p
q
q
r
r
s
s
t
t
u
u
v
v
w
w
x
x
y
y
z
z
```
{% endcode %}

{% code title="Space" lineNumbers="true" %}
```
(space)
(space)
```
{% endcode %}

{% code title="Numbers (0–9)" lineNumbers="true" %}
```
0
0
1
1
2
2
3
3
4
4
5
5
6
6
7
7
8
8
9
9
```
{% endcode %}

{% code title="Symbols (Printable ASCII, excluding space)" lineNumbers="true" %}
```
!
!
"
"
#
#
$
$
%
%
&
&
'
'
(
(
)
)
*
*
+
+
,
,
-
-
.
.
/
/
:
:
;
;
<
<
=
=
>
>
?
?
@
@
[
[
\
\
]
]
^
^
_
_
`
`
{
{
|
|
}
}
~
~
```
{% endcode %}

</details>

## Where it can be store

A Mapping File can be stored anywhere that supports `.json` files, with one primary rule:

{% hint style="danger" %}
It must be stored separately from its related Decoy Text.
{% endhint %}

Example storage locations include:

* Local devices (computers, mobile phones, flash drives, external drives)
* Offline media
* General digital storage
* Permanent storage for long-term archiving or inheritance purposes
