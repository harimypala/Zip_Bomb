# Zip Bomb

Zip bomb is a potentially vulnerable file, which leads to computer crash.<br>
Zip bomb are of two types 
1.  Recursive
    - Can be built in Windows environment
3.  Non-recursive
    - Can be built in Linux environment using a tool called zip bomb.

### How to create zip bomb _(Recursive)_ in Windows environment?
1) Open any text editor and insert null value (press ***ALT+255*** in keyboard) continued by < space >.
2) Save the file in a fresh folder and name the file _a.txt_.
3) Now copy the file and paste the file for 10-20 times in he same folder.
4) Now club all the _a.txt_ files to one file.
   - Open cmd prompt and navigate to the file location.
   - Type in the command `copy * /b b.txt` and hit ***ENTER***.
   - A new file is generated in the same folder called _b.txt_ as the the above command.
   - Delete all the files other that _b.txt_ file.
   - Now repeat the same process from point 3(copy _b.txt_ file and paste ffor 10-20 times.....).
   - Continue till _f.txt_ file with a solid size.
5) Now Zip the _f.txt_ file with `7ZIP` with the below options and name it as _exploit0.zip_ (zipping takes some time).
6) Now ***DELETE*** the _f.txt_ file and copy the _exploit0.zip_ file and paste for 10 times.
7) Select all and zip the files using `7ZIP` by following point 5 options and name it as _exploit1.zip_.
8) Now ***DELETE*** the _exploit0.zip_ files and repeat the same process as point 6.
9) Continue the same process till _exploit9.zip_ file.

**_Now the Zip Bomb is ready._**

### Calculations

| a.txt | >>> | f.txt | exploit0=1GB | exploit1=10GB | exploit2=100GB | >>> | exploit9=1,000,000,000GB or 1000PB |
| :---- | :---: | :---: | :--------: | :-----------: | :------------: | :---: | ---: |
| 1KB   | >>> | 1GB   | 1GB          | 1GB           | 100GB          | >>> | 100PB |
|       |     |       |              | 1GB           | 100GB          | >>> | 100PB |
|       |     |       |              | 1GB           | 100GB          | >>> | 100PB |
|       |     |       |              | 1GB           | 100GB          | >>> | 100PB |
|       |     |       |              | 1GB           | 100GB          | >>> | 100PB |
|       |     |       |              | 1GB           | 100GB          | >>> | 100PB |
|       |     |       |              | 1GB           | 100GB          | >>> | 100PB |
|       |     |       |              | 1GB           | 100GB          | >>> | 100PB |
|       |     |       |              | 1GB           | 100GB          | >>> | 100PB |
|       |     |       |              | 1GB           | 100GB          | >>> | 100PB |
