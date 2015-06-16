# mkg-minsoc
mkg-minsoc is a soc design learning tutorial for Hardware engineer or student.
Firstlys we all kown,A soc for users is :
  
  1、can run codes and have simple periperat

  2、have debug interface for users to debug codes or download codes

  3、codes can auto start 

In this tutorial I will build and introduce three architecture of soc based on openriscv2 from simple to complex which can compile these three function

  mkg-minsoc0:can cover the first function,can run codes and have simple periperat

  mkg-minsoc1:based on mkg-minsoc0 and added debug interface

  mkg-minsoc2:based on mkg-minsoc1 and can codes auto start 

##mkg-minsoc Archtecture introduce

###mkg-minsoc0

![image](https://github.com/lx324310/mkg-minsoc/blob/master/doc/mkg-minsoc0.png)

####mkg-minsoc0 top 
1、clkgen offer a system clock

2、OR1200_top(contains openriscv2(CPU),cache,mmu,store buffer,wishbone interface unit(BIU) and so on,the purple parts are not prerequisite for OR1200_top)

3、whibone arbiter 

4、wb_ram(on_chip ram acts as memory)

5、uart and gpio control(are not prerequisite for mkg-minsoc0)

####mkg-minsoc bench top

1、mkg-minsoc0（design under test[DUT])

2、or1200-monitor(used to display and save openriscv2 status such as gpsr value,time of inst excute,exception occur and so on)

3、preload_ram

2、

