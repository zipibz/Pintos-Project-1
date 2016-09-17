Muhammad Ibrahim Butt
CIS520 Fall 2016
proj0

In order to incorporate the alarm-mega test I executed the following tests:

1. Created a new .ck file called alarm-mega in cis520/pintos/src/tests/threads

# -*- perl -*-
use tests::tests;
use tests::threads::alarm;
check_alarm (70);

2. Added {"alarm-mega", test_alarm_mega} to tests.c in cis520/pintos/src/tests/thread

3. Added "extern test_func test_alarm_mega;" to tests.h in cis520/pintos/src/tests/thread

4. Added a function called test_alarm_mega to alarm-wait.c 

void
test_alarm_mega (void) 
{
  test_sleep (5, 70);
}

5. Ran the command "make" in terminal under src/threads

6. Ran the command "pintos -v -- run alarm-mega > log-mega.txt" 

7. Rubric.Alarm was unchanged even though grep indicated a change was needed.




