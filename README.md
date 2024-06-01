# chosun_opensource



## 1. `top` 명령어

`top` 명령어는 시스템의 실시간 성능 상태를 모니터링하는 데 사용됩니다. CPU 사용량, 메모리 사용량, 실행 중인 프로세스 목록 등을 실시간으로 보여줍니다.

### 기본 사용법
```bash
top
-d: 화면 갱신 주기를 설정합니다. 예: top -d 2 (2초마다 갱신)
-p: 특정 PID의 프로세스를 모니터링합니다. 예: top -p 1234

## 2. `ps` 명령어

`ps` 명령어는 현재 시스템에서 실행 중인 프로세스를 스냅샷 형태로 보여줍니다. 특정 프로세스의 상태를 확인하거나 필터링된 정보를 얻는 데 유용합니다.

### 기본 사용법
```bash
ps

-e: 모든 프로세스를 출력합니다.
-f: 풀 포맷으로 출력합니다.
-u [사용자 이름]: 특정 사용자의 프로세스를 출력합니다.
-aux: 시스템의 모든 프로세스를 상세하게 출력합니다.

ps 명령어는 현재 실행 중인 프로세스의 일회성 스냅샷을 제공합니다. 실시간으로 프로세스를 모니터링하려면 top 명령어를 사용하는 것이 더 적합할 수 있습니다. 프로세스 ID(PID), 사용자, CPU 및 메모리 사용량 등의 정보를 확인할 때 유용합니다.


## 3. `jobs` 명령어

`jobs` 명령어는 현재 쉘 세션에서 백그라운드 작업의 목록을 보여줍니다. 작업 번호, 상태, 명령어 등을 확인할 수 있습니다.

### 기본 사용법
```bash
jobs

-l: 프로세스 ID를 포함한 세부 정보를 출력합니다. 예: jobs -l
-n: 최근에 상태가 변경된 작업만 출력합니다.
-p: 각 작업의 프로세스 ID만 출력합니다.

jobs 명령어는 백그라운드 작업을 관리하고 모니터링하는 데 유용합니다. 백그라운드 작업을 전경으로 가져오려면 fg 명령어를, 백그라운드에서 실행 중인 작업을 종료하려면 kill 명령어를 사용할 수 있습니다. 작업 번호는 bg 명령어와 함께 사용할 수 있으며, 이를 통해 백그라운드 작업을 재개할 수 있습니다.

bash


## 4. `kill` 명령어

`kill` 명령어는 특정 프로세스를 종료할 때 사용됩니다. 프로세스 ID(PID)를 사용하여 특정 프로세스에 시그널을 보냅니다.

### 기본 사용법
```bash
kill [PID]

-9: 강제 종료 시그널(SIGKILL)을 보냅니다. 예: kill -9 1234
-l: 사용 가능한 시그널 목록을 출력합니다. 예: kill -l

kill 명령어는 프로세스를 종료할 때 유용하지만, 강제 종료(SIGKILL, -9 옵션)를 사용할 경우 프로세스가 데이터를 저장하지 못할 수 있으므로 주의가 필요합니다. 일반적으로 kill [PID] 명령어로 먼저 종료를 시도하고, 실패할 경우 kill -9 [PID]를 사용하여 강제 종료하는 것이 좋습니다.
