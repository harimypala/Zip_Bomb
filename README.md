# Zip Bomb

Zip bomb is a potentially vulnerable file, which leads to computer crash.<br>
Zip bomb are of two types 
1.  Recursive
    - Can be built in Windows environment
3.  Non-recursive
    - Can be built in Linux environment using a tool called zip bomb.

https://www.youtube.com/watch?v=un9mTKMftSo

## How to create zip bomb _(Recursive)_ in Windows environment?

1) Open any text editor and insert null value (press ***ALT+255*** in keyboard) continued by < space >.
   ![image](https://user-images.githubusercontent.com/98635804/160275131-ba260370-30a9-4fba-b41a-fa86d336b780.png)

2) Save the file in a fresh folder and name the file as _a.txt_.
3) Now copy the file and paste the file for 10-20 times in he same folder.
   ![image](https://user-images.githubusercontent.com/98635804/160275238-f6792387-f79f-4fa2-9d70-7cb9d513a911.png)

4) Now club all the _a.txt_ files to one file.
   - Open cmd prompt and navigate to the file location.
   - Type in the command `copy * /b b.txt` and hit ***ENTER***.<br>
     ![image](https://user-images.githubusercontent.com/98635804/160275310-1f959868-f5de-41fa-b453-2dc573b9182a.png)

   - A new file is generated in the same folder called _b.txt_ by the above command.
     ![image](https://user-images.githubusercontent.com/98635804/160275379-5c919255-2c9c-49c7-95f5-6b89867abeb0.png)

   - Delete all the files other that _b.txt_ file.
   - Now repeat the same process from point 3(copy _b.txt_ file and paste for 10-20 times...).
   - Continue till _f.txt_ file with a solid file size of 1GB.
5) Now Zip the _f.txt_ file with `7ZIP` with the below options and name it as _exploit0.zip_ (zipping takes some time).
   ![image](https://user-images.githubusercontent.com/98635804/160275506-50a4826a-a7f6-4cfc-a457-d9f2df2f8c9b.png)

6) Now ***DELETE*** the _f.txt_ file and copy the _exploit0.zip_ file and paste for 10 times.
7) Select all and zip the files using `7ZIP` by following point 5 options and name it as _exploit1.zip_.
8) Now ***DELETE*** the _exploit0.zip_ files and repeat the same process as point 6.
9) Continue the same process till _exploit9.zip_ file with a size of 99KB.

**_Now the recursive Zip Bomb is ready._**

### Calculations


Size mentioned in the table to **original (uncompressed)** size of the file.


| a.txt | >>> | f.txt | exploit0.zip=1GB | exploit1.zip=10GB | exploit2.zip=100GB | >>> | exploit9.zip=1,000,000,000GB or 1000PB |
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


## How to create zip bomb _(Non-Recursive)_ in Linux environment?

1) Open Terminal and clone the zip bomb tool using this `git clone https://www.bamsoftware.com/git/zipbomb.git`.
2) Navigate to `zip bomb` folder and type in `python3 zipbomb --mode=quoted_overlap --num-files=250 --compressed-size=21179 > zbsm.zip`.
3) This will create a malicious zip file `zbsm.zip`.
4) Now the zip bomb is ready, you can also insert script in the malicious zip file.
5) For more information please refer to the README file in the tool. `cat README`

**_Now the non-recursive Zip Bomb is ready._**

## Scan with Virus Total

### Non-Recursive Zip Bomb

![image](https://user-images.githubusercontent.com/98635804/160274848-e0c8f102-6337-47f8-9529-c923d770ff84.png)
### Recursive Zip Bomb

![image](https://user-images.githubusercontent.com/98635804/160274797-683d8cfa-58f5-4ef1-8fa5-8406c3d4c085.png)


Reference: https://www.bamsoftware.com/hacks/zipbomb/
_**THANK YOU**_<br>
_**- Hari Mypala**_
