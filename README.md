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
3. top -b -n 1 예시 사진<img width="601" alt="리눅스 top" src="https://github.com/aswin0421/task_20233133/assets/133829776/2a222562-7997-4939-b858-d0139c17e098">

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
1.

