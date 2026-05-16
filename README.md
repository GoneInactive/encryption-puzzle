# Encryption Puzzle
Hello and welcome to my amazing encryption puzzle. Being an amateur encryption-ist and professional trader, I figured what better way to spend a Friday afternoon than to build a machine-learning encryption puzzle for my (hopefully) future intern. Godspeed.

# The Problem
I have created an advanced stochastic / random encryption algorithm called **STIR**. Your goal is to decrypt the following sentence:

```
eWR9s5k`nOF97AM\%`{ZR){jw)j)Vxw}n)Lj{ux)xw)\]R[0|)|nl~{r}#7)Jo}n{):9)|rv~uj}rxw|5)R)qjm)}qn)tn#7wF@<8 iP*s
```

I have provided you with `encrypted_data.csv` which contains ~500,000 observations of encrypted/decrypted sentence pairs. Use all the skills a quant would use to crack it. Reach out to me for a hint.


## The Goals

1. **(Easy)** Tell me what the decrypted message says.

2. **(Medium)** What structure, pattern, or signal can you identify in the encryption? How does it work at a high level?

3. **(Difficult)** Fully reverse-engineer the encryption algorithm. Implement a general decoder in Python.

## My Suggestion
There are many ways to go about this — try to approach it the same way you would a problem in markets.

**Observe -> Identify -> Model.**

- Use Python and Pandas. Start by just *looking* at the data.
- Think about what is signal and what is noise. There is a lot of noise.
- The key space is smaller than you think. Much smaller.

I would not call this an easy puzzle, but it is definitely solvable. Considerably easier than the markets.


## A Look At The Data

**The CSV has 3 columns:**

| encrypted_sentence | decrypted_sentence | check |
|---|---|---|
| `}$ab"2NN52S8N%mf{j%yt%...` | I have to go to sleep. | True |
| `=76rP1n65+kHWOZujg &oy&...` | Today is June 18th and it is Muiriel's birthday! | True |
| `'zT*~4t(Vc24*nlHOwktkgn...` | Muiriel is 20 now. | True |
| ... | ... | ... |

**A real example** — the sentence `This was encrypted using STIR!` encrypted three times:

```
Encryption 1:  !0nbe38T?17$in><83Uijt!xbt!fodszqufe!vtjoh!TUJS"n&Hc({=K&%
Encryption 2:  |0Zv.029+>r-Ho!-/Vjku"ycu"gpet{rvgf"wukpi"UVKT#]z"uH_^XSg
Encryption 3:  Hl|W~1;84}eqS\pq{( i{(mvkz"x|ml(}{qvo([\QZ)#lUDcl|2GB
```

Same input. Wildly different output each time. The dataset gives you many examples of the same sentence encrypted multiple ways — that's your biggest hint.

## An Obscure Little Hint Before You Go

Q: How does a person think?  
A: They have a brain.

Q: But how does the brain work?  
A: Well, it has neurons that connect and pass information.

Q: How does that work?  
A: Good question.

Q: What does any of this have to do with encryption?  
A: ...
