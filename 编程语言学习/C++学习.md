# C++学习
## 一、指针
### 1、内存
指针:用来存放首地址和长度，会占用一定的内存，且占用内存只和系统有关，32位占有32位，4bytes，64位占有64位，8bytes。
### 2、用途
- **函数传参**：  当传递较大的数据结构时，比如说class等，其占较大的内存，可以用指针进行传参。
- **跨函数的值修改**
- **数组**：是一个const指针，常量指针。
- **数据结构**：如链表、树、图等。
### 3、二级指针
指向指针的指针，用来修改指针指向的地址。
### 4、void*万能指针
void\*代表地址，没有长度。void\*可以指向任何类型的地址，也仅仅代表地址。在某些场景中可以完成一些复杂的任务。  
如利用指针完成任意值的交换：  
用到的函数及引用的头文件：  

- include < stdlib.h >或< malloc.h > ：该头文件中的malloc函数，原型`extern void *malloc(unsigned int num_bytes);`，声明`void *malloc(size_t size);`，函数返回为void型指针，因此必要时要进行类型转换。它能向系统申请分配一个长度为num_bytes（或size）个字节的内存块。一般它需和free函数配对使用。free函数能释放某个动态分配的地址，表明不再使用这块动态分配的内存了，实现把之前动态申请的内存返还给系统。
- include < cstring >：函数原型`void *memcpy(void *dest, const void *src, size_t n);`；从源src所指的内存地址的起始位置开始拷贝n个字节到目标dest所指的内存地址的起始位置中。
<pre name="code" class="C++">
#include < cstring >
#include < stdlib.h >
void swap(void * lhs,void * rhs,size_t sz)
{
    void *temp =malloc(sz);
    memcpy(temp,lhs,sz);
    memcpy(lhs,rhs,sz);
    memcpy(rhs,temp,sz);
    free(temp);
}
</pre>
## 二、