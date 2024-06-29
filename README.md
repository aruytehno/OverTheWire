# [OverTheWire](https://overthewire.org/)
![alt text](img/workplace.png)

## [Bandit](https://overthewire.org/wargames/bandit/)

<details>
<summary><a href="https://overthewire.org/wargames/bandit/bandit0.html">Level 0</a></summary>

```shell
sshpass -p bandit0 ssh bandit0@bandit.labs.overthewire.org -p 2220
```
</details>
<details>
<summary><a href="https://overthewire.org/wargames/bandit/bandit1.html">Level 0 → Level 1</a></summary>

```shell
sshpass -p bandit0 ssh bandit0@bandit.labs.overthewire.org -p 2220
cat readme
```
</details>
<details>
<summary><a href="https://overthewire.org/wargames/bandit/bandit2.html">Level 1 → Level 2</a></summary>

```shell
sshpass -p ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If ssh bandit1@bandit.labs.overthewire.org -p 2220
cat ./-
```
</details>
<details>
<summary><a href="https://overthewire.org/wargames/bandit/bandit3.html">Level 2 → Level 3</a></summary>

```shell
sshpass -p 263JGJPfgU6LtdEvgfWU1XP5yac29mFx ssh bandit2@bandit.labs.overthewire.org -p 2220
cat spaces\ in\ this\ filename 
```
</details>
<details>
<summary><a href="https://overthewire.org/wargames/bandit/bandit4.html">Level 3 → Level 4</a></summary>

```shell
sshpass -p MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx ssh bandit3@bandit.labs.overthewire.org -p 2220
cd inhere/
cat ...Hiding-From-You
```
</details>
<details>
<summary><a href="https://overthewire.org/wargames/bandit/bandit5.html">Level 4 → Level 5</a></summary>

```shell
sshpass -p 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ ssh bandit4@bandit.labs.overthewire.org -p 2220
cd inhere/
find . -type f -exec file {} + | grep ASCII | cut -d: -f1 | xargs cat
```
</details>
<details>
<summary><a href="https://overthewire.org/wargames/bandit/bandit6.html">Level 5 → Level 6</a></summary>

```shell
sshpass -p 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw ssh bandit5@bandit.labs.overthewire.org -p 2220
find . -type f -size 1033c -exec cat {} + | sed 's/ //g'
```
</details>
<details>
<summary><a href="https://overthewire.org/wargames/bandit/bandit7.html">Level 6 → Level 7</a></summary>

```shell
sshpass -p HWasnPhtq9AVKe0dmk45nxy20cvUa6EG ssh bandit6@bandit.labs.overthewire.org -p 2220
find / -size 33c -user bandit7 -group bandit6 2> /dev/null -exec cat {} +
```
</details>
<details>
<summary><a href="https://overthewire.org/wargames/bandit/bandit8.html">Level 7 → Level 8</a></summary>

```shell
sshpass -p morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj ssh bandit7@bandit.labs.overthewire.org -p 2220
grep -n "millionth" data.txt | cut -f2 -d:
```
</details>
<details>
<summary><a href="https://overthewire.org/wargames/bandit/bandit9.html">Level 8 → Level 9</a></summary>

```shell
sshpass -p dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc ssh bandit8@bandit.labs.overthewire.org -p 2220
sort data.txt | uniq -u
```
</details>