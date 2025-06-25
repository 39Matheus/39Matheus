- 👋 Hi, I’m @39Matheus
- 🎓 I’m an undergraduate student at UFRN, passionate about Data Science and Machine Learning
- 💻 Coding in C++, Python, and occasionally dabbling in assembly wizardry
- 📫 Reach me right here on GitHub! I will answer you between 1 second and 3 years ;)

![Python](https://img.shields.io/badge/-Python-3776AB?style=flat&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/-C++-00599C?style=flat&logo=c%2B%2B&logoColor=white)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=000)](#)
![Assembly](https://img.shields.io/badge/-🛠️%20Assembly-6E4C1E?style=flat&logo=assembly)
[![Go](https://img.shields.io/badge/Go-%2300ADD8.svg?&logo=go&logoColor=white)](#)

[![MARS IDE](https://img.shields.io/badge/MARS-IDE-blue?style=flat&logo=linux)](http://courses.missouristate.edu/kenvollmar/mars/)
[![Google Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?logo=googlecolab&logoColor=fff)](#)


```asm
.data
input: .asciiz "curious one"
output: .space 100

.text
.globl main
main:
    la $t0, input
    la $t1, output
loop:
    lb $t2, 0($t0)
    beqz $t2, done
    li $t3, 97
    li $t4, 122
    blt $t2, $t3, copy
    bgt $t2, $t4, copy
    addi $t2, $t2, 1
    ble $t2, $t4, store
    li $t2, 97
store:
    sb $t2, 0($t1)
    j cont
copy:
    sb $t2, 0($t1)
cont:
    addi $t0, $t0, 1
    addi $t1, $t1, 1
    j loop
done:
    li $t2, 0
    sb $t2, 0($t1)
    li $v0, 4
    la $a0, output
    syscall
    li $v0, 10
    syscall
```
<!---
39Matheus/39Matheus is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
