# NAME: Justin Pank
# EMAIL: jtpank@g.ucla.edu
# ID: 204417822 
CC = gcc
FILES   = lab2_add.c lab2_list.c SortedList.c SortedList.h Makefile README 

build:
	$(CC) -std=gnu11 -g -Wall -Wextra -Wno-unused-parameter -pthread lab2_add.c -o lab2_add
	$(CC) -std=gnu11 -g -Wall -Wextra -Wno-unused-parameter -pthread SortedList.c lab2_list.c -o lab2_list
dist: graphs
	tar -zcvf lab2a-204417822.tar.gz $(FILES) *.gp *.png *.csv
graphs: tests
	gnuplot lab2_add.gp
	gnuplot lab2_list.gp
clean:
	rm -rf lab2_add lab2_list lab2a-204417822.tar.gz
#	5 tests to conduct
#       lab2_add-1.png  (--yield w/ range of threads (2, 4, 8, 12) & iterations 10, 20, 40, 80, 100, 1000, 100000, 1000000) plot of succesful 
#       lab2_add-2.png ... cost per operation of yielding
#       lab2_add-3.png ... cost per operation vs number of iterations
#       lab2_add-4.png ... threads and iterations that run (protected) w/o failure
#       lab2_add-5.png ... cost per operation vs number of threads
tests: clean build
	./lab2_add --threads=2 --iterations=100 	>> lab2_add.csv
	./lab2_add --threads=2 --iterations=1000 	>> lab2_add.csv	
	./lab2_add --threads=2 --iterations=10000 	>> lab2_add.csv
	./lab2_add --threads=2 --iterations=100000 	>> lab2_add.csv
	./lab2_add --threads=4 --iterations=100 	>> lab2_add.csv
	./lab2_add --threads=4 --iterations=1000 	>> lab2_add.csv	
	./lab2_add --threads=4 --iterations=10000 	>> lab2_add.csv
	./lab2_add --threads=4 --iterations=100000 	>> lab2_add.csv
	./lab2_add --threads=8 --iterations=100 	>> lab2_add.csv
	./lab2_add --threads=8 --iterations=1000 	>> lab2_add.csv	
	./lab2_add --threads=8 --iterations=10000 	>> lab2_add.csv
	./lab2_add --threads=8 --iterations=100000 	>> lab2_add.csv
	./lab2_add --threads=12 --iterations=100 	>> lab2_add.csv
	./lab2_add --threads=12 --iterations=1000 	>> lab2_add.csv	
	./lab2_add --threads=12 --iterations=10000 	>> lab2_add.csv
	./lab2_add --threads=12 --iterations=100000 	>> lab2_add.csv

	./lab2_add --threads=2 --iterations=10 --yield 		>> lab2_add.csv
	./lab2_add --threads=4 --iterations=10 --yield 		>> lab2_add.csv
	./lab2_add --threads=8 --iterations=10 --yield 		>> lab2_add.csv
	./lab2_add --threads=12 --iterations=10 --yield 	>> lab2_add.csv
	./lab2_add --threads=2 --iterations=20 --yield 		>> lab2_add.csv
	./lab2_add --threads=4 --iterations=20 --yield 		>> lab2_add.csv
	./lab2_add --threads=8 --iterations=20 --yield 		>> lab2_add.csv
	./lab2_add --threads=12 --iterations=20 --yield 	>> lab2_add.csv
	./lab2_add --threads=2 --iterations=40 --yield 		>> lab2_add.csv
	./lab2_add --threads=4 --iterations=40 --yield 		>> lab2_add.csv
	./lab2_add --threads=8 --iterations=40 --yield 		>> lab2_add.csv
	./lab2_add --threads=12 --iterations=40 --yield 	>> lab2_add.csv
	./lab2_add --threads=2 --iterations=80 --yield 		>> lab2_add.csv
	./lab2_add --threads=4 --iterations=80 --yield 		>> lab2_add.csv
	./lab2_add --threads=8 --iterations=80 --yield 		>> lab2_add.csv
	./lab2_add --threads=12 --iterations=80 --yield		>> lab2_add.csv
	./lab2_add --threads=2 --iterations=100 --yield	 	>> lab2_add.csv
	./lab2_add --threads=4 --iterations=100 --yield 	>> lab2_add.csv
	./lab2_add --threads=8 --iterations=100 --yield 	>> lab2_add.csv
	./lab2_add --threads=12 --iterations=100 --yield	>> lab2_add.csv
	./lab2_add --threads=2 --iterations=1000 --yield	>> lab2_add.csv
	./lab2_add --threads=4 --iterations=1000 --yield  	>> lab2_add.csv
	./lab2_add --threads=8 --iterations=1000 --yield  	>> lab2_add.csv
	./lab2_add --threads=12 --iterations=1000 --yield 	>> lab2_add.csv
	./lab2_add --threads=2 --iterations=10000 --yield 	>> lab2_add.csv
	./lab2_add --threads=4 --iterations=10000 --yield 	>> lab2_add.csv
	./lab2_add --threads=8 --iterations=10000 --yield 	>> lab2_add.csv
	./lab2_add --threads=12 --iterations=10000 --yield 	>> lab2_add.csv
	./lab2_add --threads=2 --iterations=100000 --yield 	>> lab2_add.csv
	./lab2_add --threads=4 --iterations=100000 --yield 	>> lab2_add.csv
	./lab2_add --threads=8 --iterations=100000 --yield 	>> lab2_add.csv
	./lab2_add --threads=12 --iterations=100000 --yield 	>> lab2_add.csv

	./lab2_add --threads=1 --iterations=100 		>> lab2_add.csv
	./lab2_add --threads=1 --iterations=1000 		>> lab2_add.csv
	./lab2_add --threads=1 --iterations=10000 		>> lab2_add.csv
	./lab2_add --threads=1 --iterations=100000 		>> lab2_add.csv
	./lab2_add --threads=1 --iterations=1000000 		>> lab2_add.csv
	./lab2_add --threads=2 --iterations=100 		>> lab2_add.csv
	./lab2_add --threads=2 --iterations=1000 		>> lab2_add.csv
	./lab2_add --threads=2 --iterations=10000 		>> lab2_add.csv
	./lab2_add --threads=2 --iterations=100000 		>> lab2_add.csv
	./lab2_add --threads=2 --iterations=1000000 		>> lab2_add.csv
	./lab2_add --threads=4 --iterations=100 		>> lab2_add.csv
	./lab2_add --threads=4 --iterations=1000 		>> lab2_add.csv
	./lab2_add --threads=4 --iterations=10000 		>> lab2_add.csv
	./lab2_add --threads=4 --iterations=100000 		>> lab2_add.csv
	./lab2_add --threads=4 --iterations=100000 		>> lab2_add.csv
	./lab2_add --threads=1 --iterations=100 --yield		>> lab2_add.csv
	./lab2_add --threads=1 --iterations=1000 --yield 	>> lab2_add.csv
	./lab2_add --threads=1 --iterations=10000 --yield 	>> lab2_add.csv
	./lab2_add --threads=1 --iterations=100000 --yield 	>> lab2_add.csv
	./lab2_add --threads=1 --iterations=1000000 --yield	>> lab2_add.csv
	./lab2_add --threads=2 --iterations=100 --yield		>> lab2_add.csv
	./lab2_add --threads=2 --iterations=1000 --yield	>> lab2_add.csv
	./lab2_add --threads=2 --iterations=10000 --yield	>> lab2_add.csv
	./lab2_add --threads=2 --iterations=100000 --yield 	>> lab2_add.csv
	./lab2_add --threads=2 --iterations=1000000 --yield 	>> lab2_add.csv
	./lab2_add --threads=4 --iterations=100 --yield 	>> lab2_add.csv
	./lab2_add --threads=4 --iterations=1000 --yield 	>> lab2_add.csv
	./lab2_add --threads=4 --iterations=10000 --yield 	>> lab2_add.csv
	./lab2_add --threads=4 --iterations=100000 --yield 	>> lab2_add.csv			
	./lab2_add --threads=4 --iterations=1000000 --yield 	>> lab2_add.csv

	./lab2_add --threads=2  --iterations=10000 --yield --sync=m  >> lab2_add.csv
	./lab2_add --threads=4  --iterations=10000 --yield --sync=m  >> lab2_add.csv
	./lab2_add --threads=8  --iterations=10000 --yield --sync=m  >> lab2_add.csv
	./lab2_add --threads=12 --iterations=10000 --yield --sync=m  >> lab2_add.csv
	./lab2_add --threads=2  --iterations=10000 --yield --sync=c  >> lab2_add.csv
	./lab2_add --threads=4  --iterations=10000 --yield --sync=c  >> lab2_add.csv
	./lab2_add --threads=8  --iterations=10000 --yield --sync=c  >> lab2_add.csv
	./lab2_add --threads=12 --iterations=10000 --yield --sync=c  >> lab2_add.csv
	./lab2_add --threads=2  --iterations=10000 --yield --sync=s  >> lab2_add.csv
	./lab2_add --threads=4  --iterations=10000 --yield --sync=s  >> lab2_add.csv
	./lab2_add --threads=8  --iterations=1000  --yield --sync=s  >> lab2_add.csv
	./lab2_add --threads=12 --iterations=1000  --yield --sync=s  >> lab2_add.csv

	./lab2_add --threads=1 --iterations=10000 --sync=m 	>> lab2_add.csv
	./lab2_add --threads=2 --iterations=10000 --sync=m 	>> lab2_add.csv
	./lab2_add --threads=4 --iterations=10000 --sync=m 	>> lab2_add.csv
	./lab2_add --threads=8 --iterations=10000 --sync=m 	>> lab2_add.csv
	./lab2_add --threads=12--iterations=10000 --sync=m 	>> lab2_add.csv
	./lab2_add --threads=1 --iterations=10000 --sync=m 	>> lab2_add.csv
	./lab2_add --threads=2 --iterations=10000 --sync=c 	>> lab2_add.csv
	./lab2_add --threads=4 --iterations=10000 --sync=c 	>> lab2_add.csv
	./lab2_add --threads=8 --iterations=10000 --sync=c 	>> lab2_add.csv
	./lab2_add --threads=12--iterations=10000 --sync=c 	>> lab2_add.csv
	./lab2_add --threads=1 --iterations=10000 --sync=m 	>> lab2_add.csv
	./lab2_add --threads=2 --iterations=10000 --sync=s 	>> lab2_add.csv
	./lab2_add --threads=4 --iterations=10000 --sync=s 	>> lab2_add.csv
	./lab2_add --threads=8 --iterations=10000 --sync=s 	>> lab2_add.csv
	./lab2_add --threads=12--iterations=10000 --sync=s 	>> lab2_add.csv

	-./lab2_list --threads=1 --iterations=10	>> lab2_list.csv
	-./lab2_list --threads=1 --iterations=100 	>> lab2_list.csv
	-./lab2_list --threads=1 --iterations=1000 	>> lab2_list.csv
	-./lab2_list --threads=1 --iterations=10000 	>> lab2_list.csv
	-./lab2_list --threads=1 --iterations=20000 	>> lab2_list.csv

	-./lab2_list --threads=2 --iterations=1	 	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=10 	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=100 	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=1000 	>> lab2_list.csv
	-./lab2_list --threads=4 --iterations=1	 	>> lab2_list.csv
	-./lab2_list --threads=4 --iterations=10 	>> lab2_list.csv
	-./lab2_list --threads=4 --iterations=100 	>> lab2_list.csv
	-./lab2_list --threads=4 --iterations=1000 	>> lab2_list.csv
	-./lab2_list --threads=8 --iterations=1	 	>> lab2_list.csv
	-./lab2_list --threads=8 --iterations=10 	>> lab2_list.csv
	-./lab2_list --threads=8 --iterations=100 	>> lab2_list.csv
	-./lab2_list --threads=8 --iterations=1000 	>> lab2_list.csv
	-./lab2_list --threads=12 --iterations=1 	>> lab2_list.csv
	-./lab2_list --threads=12 --iterations=10 	>> lab2_list.csv
	-./lab2_list --threads=12 --iterations=100 	>> lab2_list.csv
	-./lab2_list --threads=12 --iterations=1000 	>> lab2_list.csv

	-./lab2_list --threads=2 --iterations=1	--yield=i 	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=2	--yield=i	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=4	--yield=i	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=8	--yield=i	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=16--yield=i	>> lab2_list.csv
	-./lab2_list --threads=4 --iterations=1	--yield=i 	>> lab2_list.csv
	-./lab2_list --threads=4 --iterations=2	--yield=i	>> lab2_list.csv
	-./lab2_list --threads=4 --iterations=4	--yield=i	>> lab2_list.csv
	-./lab2_list --threads=4 --iterations=8	--yield=i	>> lab2_list.csv
	-./lab2_list --threads=4 --iterations=16--yield=i	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=1	--yield=i 	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=2	--yield=i	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=4	--yield=i	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=8	--yield=i	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=16--yield=i	>> lab2_list.csv

	-./lab2_list --threads=2 --iterations=1	--yield=d 	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=2 --yield=d	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=4 --yield=d	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=8 --yield=d	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=16--yield=d	>> lab2_list.csv
	-./lab2_list --threads=4 --iterations=1	--yield=d 	>> lab2_list.csv
	-./lab2_list --threads=4 --iterations=2 --yield=d	>> lab2_list.csv
	-./lab2_list --threads=4 --iterations=4 --yield=d	>> lab2_list.csv
	-./lab2_list --threads=4 --iterations=8 --yield=d	>> lab2_list.csv
	-./lab2_list --threads=4 --iterations=16--yield=d	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=1	--yield=d 	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=2 --yield=d	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=4 --yield=d	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=8 --yield=d	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=16--yield=d	>> lab2_list.csv

	-./lab2_list --threads=2 --iterations=1	--yield=il 	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=2 --yield=il	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=4 --yield=il	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=8 --yield=il	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=16--yield=il	>> lab2_list.csv
	-./lab2_list --threads=4 --iterations=1	--yield=il 	>> lab2_list.csv
	-./lab2_list --threads=4 --iterations=2 --yield=il	>> lab2_list.csv
	-./lab2_list --threads=4 --iterations=4 --yield=il	>> lab2_list.csv
	-./lab2_list --threads=4 --iterations=8 --yield=il	>> lab2_list.csv
	-./lab2_list --threads=4 --iterations=16--yield=il	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=1	--yield=il 	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=2 --yield=il	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=4 --yield=il	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=8 --yield=il	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=16--yield=il	>> lab2_list.csv

	-./lab2_list --threads=2 --iterations=1	--yield=dl 	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=2 --yield=dl	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=4 --yield=dl	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=8 --yield=dl	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=16--yield=dl	>> lab2_list.csv
	-./lab2_list --threads=4 --iterations=1	--yield=dl 	>> lab2_list.csv
	-./lab2_list --threads=4 --iterations=2 --yield=dl	>> lab2_list.csv
	-./lab2_list --threads=4 --iterations=4 --yield=dl	>> lab2_list.csv
	-./lab2_list --threads=4 --iterations=8 --yield=dl	>> lab2_list.csv
	-./lab2_list --threads=4 --iterations=16--yield=dl	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=1	--yield=dl 	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=2 --yield=dl	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=4 --yield=dl	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=8 --yield=dl	>> lab2_list.csv
	-./lab2_list --threads=2 --iterations=16--yield=dl	>> lab2_list.csv

	-./lab2_list --threads=12 --iterations=32 --yield=i  --sync=m >> lab2_list.csv
	-./lab2_list --threads=12 --iterations=32 --yield=d  --sync=m >> lab2_list.csv
	-./lab2_list --threads=12 --iterations=32 --yield=il --sync=m >> lab2_list.csv
	-./lab2_list --threads=12 --iterations=32 --yield=dl --sync=m >> lab2_list.csv
	-./lab2_list --threads=12 --iterations=32 --yield=i  --sync=s >> lab2_list.csv
	-./lab2_list --threads=12 --iterations=32 --yield=d  --sync=s >> lab2_list.csv
	-./lab2_list --threads=12 --iterations=32 --yield=il --sync=s >> lab2_list.csv
	-./lab2_list --threads=12 --iterations=32 --yield=dl --sync=s >> lab2_list.csv

	-./lab2_list --threads=1  --iterations=1000 		>> lab2_list.csv
	-./lab2_list --threads=1  --iterations=1000 --sync=m 	>> lab2_list.csv
	-./lab2_list --threads=2  --iterations=1000 --sync=m 	>> lab2_list.csv
	-./lab2_list --threads=4  --iterations=1000 --sync=m 	>> lab2_list.csv
	-./lab2_list --threads=8  --iterations=1000 --sync=m 	>> lab2_list.csv
	-./lab2_list --threads=12 --iterations=1000 --sync=m 	>> lab2_list.csv
	-./lab2_list --threads=16 --iterations=1000 --sync=m 	>> lab2_list.csv
	-./lab2_list --threads=24 --iterations=1000 --sync=m 	>> lab2_list.csv
	-./lab2_list --threads=1  --iterations=1000 --sync=s 	>> lab2_list.csv
	-./lab2_list --threads=2  --iterations=1000 --sync=s 	>> lab2_list.csv
	-./lab2_list --threads=4  --iterations=1000 --sync=s 	>> lab2_list.csv
	-./lab2_list --threads=8  --iterations=1000 --sync=s 	>> lab2_list.csv
	-./lab2_list --threads=12 --iterations=1000 --sync=s 	>> lab2_list.csv
	-./lab2_list --threads=16 --iterations=1000 --sync=s 	>> lab2_list.csv
	-./lab2_list --threads=24 --iterations=1000 --sync=s 	>> lab2_list.csv
