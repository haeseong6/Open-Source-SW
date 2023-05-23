# top, ps, jobs, kill 명령어
---


## top

* 현재 OS의 상태를 보여줌
* 3초 간격으로 업데이트하여 화면에 출력 됨
* 프로세스 목록을 CPU 사용률이 높은 것부터 보여줌

```
top -n [숫자] -> 실행 주기 설정, 3초 간격으로 [숫자]번 만큼 실행됨
```


## ps
_Process Status_
* 현재 구동 중인 프로세스 정보를 확인할 수 있음
```
__ps -e__ -> 다른 사용자들이 구동시킨 프로세스도 보여줌

__ps -f__ -> 정보를 상세하게 보여줌

__ps -l__ -> -f옵션보다 더 상세하게 보여줌 
```
![ps -efl](https://github.com/haeseong6/Open-Source-SW/assets/133829902/7433be55-5c49-485f-82f2-33806f7fa933)
> ps -efl
## jobs
* 현재 쉘 세션에서 실행시킨 백그라운드 작업의 목력이 축력됨

__jobs -l__ -> 프로세스 그룹 ID를 state 필드 앞에 출력

__jobs -n__ -> 프로세스 그룹 중에 대표 프로세스 ID를 출력

__jobs -p__ -> 각 프로세스 ID에 대해 한 행씩 출력


## kill
* 프로세스에 시그널을 보내는 명령어
  * 프로세스 종료에 주로 쓰임

kill [options] [pid]

kill -l -> 전체 시그널 목록을 보여줌

kill -9 [pid] -> pid에 해당하는 프로세스를 강제종료

| SIGNALS |   |    |   |   |
| :------- | :----- | :----- | :------ | :------- |
| 1) SIGHUP   |    2) SIGINT    |   3) SIGQUIT  |    4) SIGILL    |   5) SIGTRAP |
| 6) SIGABRT    |  7) SIGBUS    |   8) SIGFPE    |   9) SIGKILL   |  10) SIGUSR1 |
| 11) SIGSEGV    | 12) SIGUSR2   |  13) SIGPIPE   |  14) SIGALRM  |   15) SIGTERM |
| 16) SIGSTKFLT  | 17) SIGCHLD   |  18) SIGCONT  |   19) SIGSTOP  |   20) SIGTSTP |
| 21) SIGTTIN   |  22) SIGTTOU   |  23) SIGURG   |   24) SIGXCPU  |   25) SIGXFSZ |
| 26) SIGVTALRM  | 27) SIGPROF   |  28) SIGWINCH  |  29) SIGIO    |   30) SIGPWR |
| 31) SIGSYS    |  34) SIGRTMIN  |  35) SIGRTMIN+1 | 36) SIGRTMIN+2 | 37) SIGRTMIN+3 |
| 38) SIGRTMIN+4 | 39) SIGRTMIN+5 | 40) SIGRTMIN+6 | 41) SIGRTMIN+7 | 42) SIGRTMIN+8 |
| 43) SIGRTMIN+9 | 44) SIGRTMIN+10 | 45) SIGRTMIN+11 | 46) SIGRTMIN+12 | 47) SIGRTMIN+13 |
| 48) SIGRTMIN+14 | 49) SIGRTMIN+15 | 50) SIGRTMAX-14 | 51) SIGRTMAX-13 | 52) SIGRTMAX-12 |
| 53) SIGRTMAX-11 | 54) SIGRTMAX-10 | 55) SIGRTMAX-9 | 56) SIGRTMAX-8 | 57) SIGRTMAX-7 |
| 58) SIGRTMAX-6 | 59) SIGRTMAX-5  | 60) SIGRTMAX-4 | 61) SIGRTMAX-3 | 62) SIGRTMAX-2 |
| 63) SIGRTMAX-1 | 64) SIGRTMAX  |  |   |   |
