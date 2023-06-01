# OS-HW4
HW4_findeq: multithreaded search of files with equal data

## Description
findeq: It is a program that checks all the sub-directory files in the input directory for duplicate files using multi-threads. It consists of only the POSIX standard library in C.

## Build
You only need to compile findeq.c file.  

<pre><code>$ gcc findeq.c -o findeq -lpthread
</code></pre>
After compiling with the findeq.c file, you can run three options by option.  
Thread : -t=NUM (1-64)  
Filtering size: -m=NUM (byte)  
Create output file : -o=FILE (not necessary)  
<pre><code>$ ./findeq -t=[1-64] -m=[byte] -o=FILE [DIR]
</code></pre>
## Usage
### test1
```bash
$ ls
test1    test1.c    bmalloc.c    bmalloc.h         
$ ./test1
...
```
### test4
```bash
$ ls
test4    test4.c    bmalloc.c    bmalloc.h         
$ ./test4
...
```
### test2
```bash
$ ls
test2    test2.c    bmalloc.c    bmalloc.h         
$ ./test2
...
```

## Contact
If you have any questions about findeq then contact us.  
21801028 Park Soonyong, parksy3978@handong.ac.kr  
21900780 Jeongwon Ha, jeongwon19@handong.ac.kr  
22100237 Kim HyungJin, 22100237@handong.ac.kr  
