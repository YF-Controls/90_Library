# PLC Coding Style

--------

## 1. Data

### 1.1. Constants

* CONSTANT_NAME
* F_CONSTANT_NAME

#### Rules

>1. Snake case
>2. Always in upper case
>3. Words must be separated by underscores
>4. Name must always begin with a letter

### 1.2. Variables

* variableName
* F_variableName

#### Rules

>1. Camel case
>2. Name must always begin with a lower case letter

### 1.3 Structures

* structureName
* F_structureName

#### Rules

>1. Camel case
>2. Name must always begin with a lower case letter

### 1.4. Data Containers

_Applicable in Siemens Datablock: DB or DI_

* CONTAINER_NAME
* F_CONTAINER_NAME

#### Rules

>1. Snake case
>2. Always in upper case
>3. Words must be separated by underscores
>4. Name must always begin with a letter

--------

## 2. Code

### 2.1. Interruptions / Main Subroutines

* INTERRUPTION_NAME
* MAIN_PROGRAM_NAME
* OB000_NAME _'Applicable in Siemens OB'_

#### Rules


### 2.2. Subroutines

* SubroutineName
* F_SubroutineName

#### Rules


### 2.3. Functions

* _functionName
* F_functionName

#### Rules


### 2.4. Modules

* _M_ModuleName
* _FM_ModuleName

#### Rules

----

## 3. Program Folder Hierarchy

| ID | Folder |
|:---|:-------|
| 00_FSP | Fail-Safe Program |
| 01_SCP | System Control Program |
| 02_MCP | Motion Control Program |
| 03_HMI | Human-Machine Interface |
| 04_DAD | Data Acquisition Devices |
| 05_IT  | Information Technology |
| 06_LLDX | Low-Level Data Exchange |
| 07_ALARM | Alarms |
| - | - |
| 90_Library | Standar Library |
| 91_Vendor | Vendor Libraries |
| 92_Custom | Custom Library |

----

## 4. Variable enumations

### 4.1. Operating mode

| usint | Operating mode |
|:-----:|:---------------|
| 0 | Control off |
| 1 | Warm restart |
| 2 | Stop mode |
| 3 | Maintenance mode |
| 4 | Semiautomatic mode |
| 5 | Automatic mode |
| 6 | Emergency stop unacknowledged |
| 7 | Emergency stop triggered |

### 4.2. Operating cycle

| usint | Operating cycle |
|:-----:|:----------------|
| 0 | No cycle |
| 3 | Maintenance movement |
| 4 | Manual movement |
| 5 | Semiautomatic step |
| 6 | Automatic cycle |

### 4.3. Command cycles

| int | Operating cycle |
|:---:|:----------------|
| -1 | No cycle |
| 0..N | Cycle number |

### 4.4. Alarm levels

| usint | Alarm levels |
|:---:|:----------------|
| 0 | No alarm |
| 1 | Information alarm |
| 2 | Warning alarm |
| 3 | Error alarm |
| 4 | Emergency alarm |

### 4.5. State machine

| int | State machine |
|:---:|:--------------|
| 0 | Wait |
| 0x0001..0x6FFF | Normal step |
| 0x7000..0x7FFF | Warning step |
| 0x8000..0x8FFF | Error step |

### 4.6. Synchronous function status

| int | Status |
|:---:|:-------|
| 0 | Done |
| 0x8000..0x8FFF | Error |

### 4.7. Asynchronous function status

| int | Status |
|:---:|:-------|
| 0 | Wait |
| 1 | Request |
| 2 | Busy |
| 3 | Done |
| 0x8000..0x8FFF | Error |

### 4.8. HMI Commands

| uint | HMI Command |
|:----:|:------------|
| 0 | Null |
| 1..N | Command number |

### 4.9. Drive action

| usint | HMI Command |
|:----:|:------------|
| 0 | Stopped |
| 1 | Running forward |
| 3 | Running backward |
