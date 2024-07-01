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
find / -user bandit7 -group bandit6 -size 33c 2>/dev/null -exec cat {} \;
```
</details>
<details>
<summary><a href="https://overthewire.org/wargames/bandit/bandit8.html">Level 7 → Level 8</a></summary>

```shell
sshpass -p morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj ssh bandit7@bandit.labs.overthewire.org -p 2220
grep -n "millionth" data.txt | cut -f2 -d:
cat data.txt | grep "millionth"
```
</details>
<details>
<summary><a href="https://overthewire.org/wargames/bandit/bandit9.html">Level 8 → Level 9</a></summary>

```shell
sshpass -p dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc ssh bandit8@bandit.labs.overthewire.org -p 2220
sort data.txt | uniq -u
```
</details>
<details>
<summary><a href="https://overthewire.org/wargames/bandit/bandit10.html">Level 9 → Level 10</a></summary>

```shell
sshpass -p 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM ssh bandit9@bandit.labs.overthewire.org -p 2220
strings data.txt | grep '=='
```
</details>
<details>
<summary><a href="https://overthewire.org/wargames/bandit/bandit11.html">Level 10 → Level 11</a></summary>

```shell
sshpass -p FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey ssh bandit10@bandit.labs.overthewire.org -p 2220
base64 --decode data.txt 
```
</details>
<details>
<summary><a href="https://overthewire.org/wargames/bandit/bandit12.html">Level 11 → Level 12</a></summary>

[Caesar cipher](https://en.wikipedia.org/wiki/Caesar_cipher)

```shell
sshpass -p dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr ssh bandit11@bandit.labs.overthewire.org -p 2220
cat data.txt | tr '[A-Za-z]' '[N-ZA-Mn-za-m]'
```
</details>
<details>
<summary><a href="https://overthewire.org/wargames/bandit/bandit13.html">Level 12 → Level 13</a></summary>

```shell
sshpass -p 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4 ssh bandit12@bandit.labs.overthewire.org -p 2220
rm -r /tmp/tmp_bandit12
mkdir /tmp/tmp_bandit12
cd /tmp/tmp_bandit12
cp ~/data.txt .
xxd -r data.txt > bdata
mv bdata bdata.gz
gunzip bdata.gz
mv bdata bdata.bz2
bzip2 -d bdata.bz2
mv bdata bdata.gz
gunzip bdata.gz
tar -xf bdata
tar -xf data5.bin
bzip2 -d data6.bin
tar -xf data6.bin.out
mv data8.bin data8.bin.gz
gunzip data8.bin.gz
cat data8.bin
rm -r /tmp/tmp_bandit12
```
</details>
<details>
<summary><a href="https://overthewire.org/wargames/bandit/bandit14.html">Level 13 → Level 14</a></summary>

```shell
sshpass -p FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn ssh bandit13@bandit.labs.overthewire.org -p 2220
ssh -o UserKnownHostsFile=/dev/null -o StrictHostKeyChecking=no -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220
cat /etc/bandit_pass/bandit14
```
</details>
<details>
<summary><a href="https://overthewire.org/wargames/bandit/bandit15.html">Level 14 → Level 15</a></summary>

```shell
sshpass -p MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS ssh bandit14@bandit.labs.overthewire.org -p 2220
telnet localhost 30000
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
```
</details>
<details>
<summary><a href="https://overthewire.org/wargames/bandit/bandit16.html">Level 15 → Level 16</a></summary>

```shell
sshpass -p 8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo ssh bandit15@bandit.labs.overthewire.org -p 2220
openssl s_client -connect localhost:30001
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
```
</details>
<details>
<summary><a href="https://overthewire.org/wargames/bandit/bandit17.html">Level 16 → Level 17</a></summary>

```text
PORT      STATE SERVICE     VERSION
31046/tcp open  echo
31518/tcp open  ssl/echo
31691/tcp open  echo
31790/tcp open  ssl/unknown
31960/tcp open  echo
```
```shell
sshpass -p kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx ssh bandit16@bandit.labs.overthewire.org -p 2220
#nmap -sV localhost -p 31000-32000
rm -r /tmp/sshme
mkdir /tmp/sshme && cd $_
echo kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx | openssl s_client -connect localhost:31790 -ign_eof > /tmp/sshme/rsa_key
chmod 600 rsa_key
ssh -o UserKnownHostsFile=/dev/null -o StrictHostKeyChecking=no -i rsa_key bandit17@bandit.labs.overthewire.org -p 2220
```
</details>
<details>
<summary><a href="https://overthewire.org/wargames/bandit/bandit18.html">Level 17 → Level 18</a></summary>

```shell
diff passwords.new passwords.old
```
</details>
<details>
<summary><a href="https://overthewire.org/wargames/bandit/bandit19.html">Level 18 → Level 19</a></summary>

```shell
sshpass -p x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme
```
</details>
<details>
<summary><a href="https://overthewire.org/wargames/bandit/bandit20.html">Level 19 → Level 20</a></summary>

```shell
sshpass -p cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8 ssh bandit19@bandit.labs.overthewire.org -p 2220
./bandit20-do cat /etc/bandit_pass/bandit20
```
</details>
<details>
<summary><a href="https://overthewire.org/wargames/bandit/bandit21.html">Level 20 → Level 21</a></summary>

```shell
sshpass -p 0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO ssh bandit20@bandit.labs.overthewire.org -p 2220
echo -n '0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO' | nc -l -p 1234 & [1] 24661
./suconnect 1234
```
</details>
<details>
<summary><a href="https://overthewire.org/wargames/bandit/bandit22.html">Level 21 → Level 22</a></summary>

```shell
sshpass -p EeoULMCra2q0dSkYj561DX7s1CpBuOBt ssh bandit21@bandit.labs.overthewire.org -p 2220
cd /etc/cron.d
cat /usr/bin/cronjob_bandit22.sh
cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
```
</details>
<details>
<summary><a href="https://overthewire.org/wargames/bandit/bandit23.html">Level 22 → Level 23</a></summary>

```shell
sshpass -p tRae0UfB9v0UzbCdn9cY0gQnds9GF58Q ssh bandit22@bandit.labs.overthewire.org -p 2220
cd /etc/cron.d/
cat /usr/bin/cronjob_bandit23.sh
echo I am user $myname | md5sum | cut -d ' ' -f 1
cat /tmp/$(!!)
cat /tmp/$(echo I am user bandit23 | md5sum | cut -d ' ' -f 1)
```
</details>
<details>
<summary><a href="https://overthewire.org/wargames/bandit/bandit24.html">Level 23 → Level 24</a></summary>

```shell
sshpass -p 0Zf11ioIjMVN551jX3CmStKLYqjk54Ga ssh bandit23@bandit.labs.overthewire.org -p 2220

```
</details>


## [Natas](https://overthewire.org/wargames/natas/)

<details>
<summary><a href="https://overthewire.org/wargames/natas/natas0.html">Level 0</a></summary>

```text
Username: natas0
Password: natas0
http://natas0.natas.labs.overthewire.org
```
```text
Solution:
view-source:http://natas0.natas.labs.overthewire.org
<!--The password for natas1 is 0nzCigAq7t2iALyvU9xcHlYN4MlkIwlq -->
```
</details>
<details>
<summary><a href="https://overthewire.org/wargames/natas/natas1.html">Level 0 → Level 1</a></summary>

```text
Username: natas1
Password: 0nzCigAq7t2iALyvU9xcHlYN4MlkIwlq
http://natas1.natas.labs.overthewire.org
```
```text
Solution:
view-source:http://natas1.natas.labs.overthewire.org
<!--The password for natas2 is TguMNxKo1DSa1tujBLuZJnDUlCcUAPlI -->
```
</details>
<details>
<summary><a href="https://overthewire.org/wargames/natas/natas2.html">Level 1 → Level 2</a></summary>

```text
Username: natas2
Password: TguMNxKo1DSa1tujBLuZJnDUlCcUAPlI
http://natas2.natas.labs.overthewire.org
```
```text
Solution:
http://natas2.natas.labs.overthewire.org/files/users.txt
natas3:3gqisGdR0pjm6tpkDKdIWO2hSvchLeYH
```
</details>