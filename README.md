# Linux 명령어

### Linux top 명령어
1. Linux top 이란?
- 시스템의 상태를 전반적으로 가장 빠르게 파악 할 수 있는 명령어(cpu, memory, process)
- 옵션을 주지않고 입력한다면 interval(3초) 간격으로 화면을 갱신하여 정보를 보여준다.
- top 실행 전 옵션 (순간의 정보를 확인하는 -b, 실행 주기를 설정하는 -n)
2. top 실행 후 명령어
- shift + p : cpu 사용률을 내림차순으로 보여준다
- shift + m : 메모리 사용률을 내림차순으로 보여준다
- shift + t: 프로세스가 돌아가고 있는 시간순으로 보여준다
- k: kill.k 입력 후 PID 번호를 작성
- f: sort filed 선택 화면이 나온다(q를 누르면 RES순으로 정렬)
- a: 메모리 사용량에 따라 정렬한다
- b: Batch 모드로 작동한다
- 1: CPU Core별로 사용량을 보여준다
3. top -b -n 1 예시 사진
<img width="601" alt="리눅스 top" src="https://github.com/aswin0421/task_20233133/assets/133829776/2a222562-7997-4939-b858-d0139c17e098">

4. VIRT,RES,SHR
-현재 프로세스가 사용하고 있는 메모리
- VIRT
-프로세스가 사용하고 있는 visual memory의 전체 용량
-프로세스가 할당된 가상 메모리 전체
-SWAP + RES
- RES
-현재 프로세스가 사용하고 있는 물리 메모리의 양
-실제로 메모리에 올려서 사용하고 있는 물리 메모리
-실제로 메모리를 쓰고 있는 RES가 핵심
- SHR
-다른 프로세스와 공유하고 있는 shred memory의 양
---
### Linux ps 명령어
1. Linux ps란?
- 현재 실행중인 프로세스 목록과 상태를 보여준다
- 정확한 옵션 사용이 중요하다(a와 -a의 옵션이 다른것처럼)
- ps [option]의 사용
2. ps 옵션들
- -A: 모든 프로세스 출력
- a: 터미널과 관련된 프로세스를 출력
- -a: 세션 리더를 제외하고 데몬 프로세스처럼 터미널에 종속되지 않은 모든 프로세스를 출력
- -e: 커널 프로세스를 제외한 모든 프로세스를 출력
- -f: 풀 포맷을 보여줌
- -o: 출력 포맷을 지정하는 옵션(pid,tty,time,cmd)
- -m: 64비트 프로세스를 보여줌
- -p 특정 PID를 지정할때 사용
- -r: 실행중인 프로세스를 보여줌
- -u:특정 사용자의 프로세스 정보를 확인할 때 사용(사용자를 지정하지 않으면 현재를 기준)
- -x: 로그인 상태에 있는 동안 아직 완료되지 않은 프로세스를 보여줌
3. ps 명령어 사용 예시
- ps 단독 사용 
<img width="220" alt="image" src="https://github.com/aswin0421/task_20233133/assets/133829776/9f900b0f-1c8f-45fe-9592-5b04c164e4a1">


-기본적으로는 프로세스 번호(PID), 프로세스가 연결된 터미널(TTY),TIME,CMD이 출력

- ps ax 사용 
<img width="401" alt="image" src="https://github.com/aswin0421/task_20233133/assets/133829776/197a9e89-c98d-44c0-85f7-25041a79291b">


-시스템에 동작중인 모든 프로세스를 보고싶은 때 사용
(PID,TTY,STAT,TIME,COMMAND 출력)_

- ps aux 사용 
<img width="548" alt="image" src="https://github.com/aswin0421/task_20233133/assets/133829776/57f957b4-4ec3-44a6-9cba-2c76d932dc26">


-시스템에 동작중인 모든 프로세스를 소유자 정보와 함께 다양한 정보를 같이 출력(특정 프로세스는 ps aux|grep apache)


4. ps 명령어 사용시 나타낼수 있는 항목
<img width="498" alt="image" src="https://github.com/aswin0421/task_20233133/assets/133829776/f2d274e0-fcd4-4922-b7ff-f0235cf2fc75">


---


### Linux jobs 명령어
1. Linux jobs란?
- 백그라운드에서 실행된 프로그램이나 작업 목록을 보여주는 명렁어
- jobs [옵션] [작업번호] 명령어로 사용
2. Linux jobs 사용 후 상태
 <img width="570" alt="image" src="https://github.com/aswin0421/task_20233133/assets/133829776/05c59f47-2752-44eb-a319-33e5d6850d89">
 
3. Linux jobs 옵션
 <img width="573" alt="image" src="https://github.com/aswin0421/task_20233133/assets/133829776/67a90250-372f-4738-bd7c-a94182b13ab2">
 
 ---
 
 ### Linux kill 명령어
 1. Linux kill이란?
 - kill 명령어를 통해서 프로세스에 시그널을 보내서 제어하는 명령어
 - kill인 이유는 아무런 시그널이 없다면 종료하는 명렁어이기 때문이다
 - kill [옵션] [PID]
 
 2. Linux kill 옵션
 - -9: 프로세스 PID를 직접 지정하여 종료
 - -l: 시그널로 사용할 수 있는 시그널들을 보여줌
 
 3. kill 명령어의 시그널 종류
 | 신호이름 | SIGNUP | SIGHT | SIGKILL | SIGSEGV | SIGTERM | SIGCONT | SIGSTOP | SIGTSTP |
 |-------|--------|---------|---------|---------|---------|----------|--------|
 | 신호 | HUP | INT | KILL | SEGV | TERM | CONT | STOP |TSTP|
 






