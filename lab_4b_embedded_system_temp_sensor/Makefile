# NAME: Justin Pank
# EMAIL: jtpank@g.ucla.edu
# ID: 204417822 

default:
	gcc -Wextra -Wall -g -std=gnu99 main.c -o lab4b -lm -lmraa
sanity:
	./P4B_sanity.sh
setenv: 
	TZ='America/Los_Angeles'; export TZ; . ~/.profile; 
check: setenv test sanity

clean:
	rm -f lab4b lab4b-204417822.tar.gz
dist:
	tar -czvf lab4b-204417822.tar.gz main.c README Makefile
test:
	echo | ./lab4b --bogus &> /dev/null; \
	if [[ $? -ne 1 ]]; then \
	echo "Test FAILED: bad argument returns wrong exit code"; \
	else \
	echo "Test PASSED: bad argument returns correct exit code"; \
	fi
