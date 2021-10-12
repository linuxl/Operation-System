编译命令为： gcc calculateNum.c -lpthread -Wall -std=c99 -o calculateNum
执行命令为： taskset -c 0,1,2,3 ./calculateNum