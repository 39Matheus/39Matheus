- 👋 Hi, I’m @39Matheus
- 🎓 I’m an undergraduate student at UFRN, passionate about Data Science and Machine Learning
- 💻 Coding in C++, Python, and occasionally dabbling in assembly wizardry
- 📫 Reach me right here on GitHub! I will answer you between 1 second and 3 years ;)

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

<!---
39Matheus/39Matheus is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
