# findeq: multithreaded search of files with equal data

## Description
It is a program that checks all the sub-directory files in the input directory for duplicate files using multi-threads. It consists of only the POSIX standard library in C.

## Build
You only need to compile findeq.c file.  

<pre><code>$ gcc findeq.c -o findeq -lpthread
</code></pre>
After compiling with the findeq.c file, you can run by three options and input directory(relative path and absolute path).  
Thread : -t=NUM (1-64)  
Filtering size: -m=NUM (byte)  
Create output file : -o=FILE (If you need standard output)  
<pre><code>$ ./findeq -t=1 -m=1024 -o=FILE [DIR]
</code></pre>
## Usage
You can manage the number of threads and the size of the files you want to ignore. You can exit the program with the SIGINT signal (i.e. CTRL+C), and when you enter -o, a list of duplicate directories with standard output appears in the txt file. The number and size of duplicated files and the computation time are additionally printed per every 5 seconds.
### test1
```bash
$ ls
findeq  findeq.c  test         
$ ./findeq -t=1 -m=1024 -o=FILE ./test
...
```
### test2
```bash
$ ls
findeq  findeq.c  test         
$ ./findeq -t=4 -m=4096 -o=FILE /home/s21801028/OS+2023/OS-HW4/test
...
```
### test3
```bash
$ ls
findeq  findeq.c  test         
$ ./findeq -t=16 -m=8192 -o=FILE ./test
...
```

## Contact
If you have any questions about findeq then contact us.  
21801028 Park Soonyong, parksy3978@handong.ac.kr  
21900780 Jeongwon Ha, jeongwon19@handong.ac.kr  
22100237 Kim HyungJin, 22100237@handong.ac.kr  
