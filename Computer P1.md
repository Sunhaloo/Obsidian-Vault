---
Alias: Computer Defintions
Tag: Note_CS, Definitions
Author: S.Sunhaloo
Type: Definitions
Date: 29-09-2023
Status: In-Progress
---

# Computer Paper 1 Definitions

# Number Representation

## Uses Binary Coded Decimal ( BCD )

- In calculators where each digit needs to be represented
    - Where decimal fractions can be accurately represented
- In digital watches

# Database

## Database Management System ( DBMS )

### Query Processor

- Allows the developer to extract data from a database
- Processes and executes queries written in SQL

### Developer Interface

- Allows the developer to create user-friendly items such as tables, forms and reports

### Data Dictionary

- Meta data about the database
	- Examples of what it holds:
		- Fields Names
		- Table Names
		- Data Types
		- Primary Key*

## Normalisation

### 1NF

- There is no duplication of data

### 2NF

- There are no partial dependencies

### 3NF

- There are no transitive dependencies

### What is meant by Candidate Key?

- A fields that could have become the Primary Key

## Name and Describe 2 Levels of Schema of a Database

- External

    - The individual's view of the database

- Internal

    - Describes how the data will be stored on physical media

- Logical

- It is the overview of a database structure
- It will model the problem
- It is independant of any particular DBMS
- It shows how relationships will be implemented 
	- By use of ER Diagrams

## What is meant by the term *data redundancy*

- Duplication of data

## How *relational database* help to reduce data redundancy

- Use of **Primary Keys** and **Foreign Keys**
- Applying the normalisation process
- Enforcing referential integrity
- Each data is stored once and is referred / referenced by the primary key

## Advantages of using a Relational Database over a Flat File Database

1. There is not duplication of data
2. There is improved security
	1. Passwords
	2. Database Views
3. Reduced Data Dependancy

## Data Validation

- To ensure that data is reasonable
- Example

    1. Range Check
    2. Length Check
    3. Check Digit

## Data Verification

- To ensure that data matches the orginal data
- Example:

    - Double Entry

## Differences between Data *Integrity* and Data *Security*

| Integrity | Security |
| ------ | ------- |
| Deals with validity of data | Deal with protection of data |
| Makes sure that data has not been corrupted during transmission | Proctects data from illegal access |

## Ways of maintaining data integrity *during data transmission*

### Parity Check

- Parity bit is added to data
- Either uses odd / even parity
- Count number of 1's
- Parity bit is sent with data
- Parity bit is checked at receiver's end
- If value is the ... else ...

### Checksum

- A calculation is performed  on data
- It is send with data
- Value is calculated again at receiver's end
- If value is the ... else ...

# Operating System

## What is meant by Dynamic Link Library ( DLL )

- A collection of self-contained programs that are already compiled
- Linked to main program during execution
- Library program code is separated from .EXE file
- A DDL file can be made available to several applications at the same time

# Video

## Describe Interlaced Encoding

- The data from a single frame is split into serparate fields
- One field has data for the odd numbered rows and another has data for even numbered rows
- Odd numbered rows alternate with even numbered rows
- The viewer sees data from 2 frames simultaneously
- Example:

    - 1080i

## Describe Progressive Encoding

- Stores all the scan lines for an entire frame
- Complete frames are displayed into sequence
- The rate of picture display is the same as frame rate
- Example:

    - 720p

# Input and Output Device

## Describe the Internal Workings of a Microphone

- The microphone has a diaphragm
- Vibrations for sound waves causes the diaphragm to move
- This causes a coil to move past a magnet ( similar to Faraday's law )
- This deforms a crystal; hence, an electrical signal is produced.

## Describe the Internal Working of a Laser Printer

- A revolving drum is initially given a charge
- A laser scans back and forth across the drum
- The drum is then coated with oppositely charged toner
- Electro-statically charged paper is fed towards the drum
- The pattern on the drum is transferred to the paper
- The paper is passed through the fuser to seal image
- Hence image is obtained on paper

## Touch Screen

### Capacitive

- Has several layers
- When user touches
- There is a change in electric field
- Microprocessor calculates the coordinates

### Resistive

- Has 2 layers
- When user touches, it brings the 2 layers together
- This completes a circuit
- Microprocessor calculates the coordinates

## Hardware

### Network

#### Sub Network

- Each device on a sub network has the **same** *Network* ID
- Each device on a sub network has the same Network ID but **different** *Host* ID
	- Benefits:
		- Improve network speed
		- Improve network security
		- Allows for easier maintenance

#### Types of servers

1. Email Server
2. File Server
3. Print Server
4. Web Server

#### WAN and LAN

Differences:

| WAN | LAN |
| --- | --- |
| Covers a large geographical area | Covers a small geographical area |
| Ownership can be public or private | Ownership is private |
| Difficult to implement security | Easy to implement security $\Rightarrow$ More secure |
| It is mostly virtual | Physical as devices need to be connected to each other |

#### Describe Mesh Topology

- All computers are connected to at least one other device
- There are multiple routes between devices
- Computer acts as relays, passing packets towards final destination

##### Advantages of mesh over bus ( can also be used on other topologies )

1. No collision of data
2. More secure because data is sent over a dedicated connection
3. If one line goes down, there are more routes available

#### What is meant by the Ethernet

- It is a protocol suite
- Used for transmission of data over standard connection
- Uses Carrier Sense Multiple Access / Collision Detection ( CSMA / CD )
- Data transmitted in frames

#### Routers and Gateways

| Router | Gateway |
| ------ | ------- |
| Connects 2 or more networks | Connects 2 or more networks |
| Acts as a single access point | Acts as a single access point |
| Receives packets and forwards towards destination | Receives packets and forwards towards destination |
| Assigns private IP | Assigns private IP |
| ---| --- |
Difference:
| Connects networks using the **same** protocol | Connects networks that uses **different** protocols |

#### Firewall

- Sits between computer and internet
- Permits or Blocks traffic From or To networks
- Can be software or hardware
- Helps against unauthorised access / Hacking

##### How firewall protects a computer

- It will monitor the incoming and outgoing traffic
- It will check against set of rules
- It will block transmission that does meet criteria

#### Authentication

- Process of determining whether somebody is who they claim to be
- Frequently done though log on passwords
- Also helps in unauthorised access

#### Explain the format of IP Address

- Composed of 4 denary integers
- Each in the range of 0-255
- Each stored in 1 byte $\Rightarrow$ 8 Bits
- Separated into host ID  and network ID by full stops
- Example:
    - 192.168.0.1

#### Public vs Private IP Address

| Public | Private |
| ------ | ------- |
| Address provided by ISP | Address issued by router to each device |
| Address is unique throughout internet | Address only unique in the network and cannot be accessed through the internet |
| Allow 2 computer to identify each other |

#### Thick Client v/s Thin Client Server Model

| Thin Client | Thick Client |
| ------------ | ----------- |
| Server performs most of the data processing required by task | Server performs minimal data processing for client |
| Client only send request to the server and display the return results | Has most of the resources installed locally |

### RAM and ROM

| RAM | ROM |
| --- | --- |
| Random Access Memory | Read Only Memory |
| Volatile Memory | **Non**-Volatile Memory |
| Used to store data of program while using | Store the Start--Up Program / **BIOS** |
| Can read and write data | Data can only be read from |

#### Explain the reasons why ROM is used in embedded systems

- It is a non-volatile
	- Does not change when device is turned off
- Data does not change
	- Data can only be read from ROM
- Store the BIOS

### DRAM and SRAM

| DRAM | SRAM |
| ---- | ---- |
| Dynamic Random Access Memory | Static Random Access Memory |
| Has to be refreshed | Does not need to be refreshed |
| Consumes more power as it needs to be refreshed | Consumes less power as it does **not** need to be refreshed |
| Uses single transistor and capacitor | Uses more than 1 transitor |
| Less expensive | More Expensive |
| Used in main memory | Uses in cache memory |
| Has higher data storage | Has lower data storage |

# Ethics and Stuff

## Copyright 

- The intellectual property rights to the program

# Von Neuman Model

## Address Bus

- Used to transfer address of data to memory
    - Unidirectional

## Data Bus

- Used to carry data between processor and memory
    - Bidirectional

## Control Bus

- Used to transmit Signals
- Dedicated bus since all timings are generated according to control signals
	- Types of Signal:
		- Interrupt
		- Timing
		- Write
		- Read

## Program Counter ( PC )

- Stores the address of the next instruction to be fetched

## Memory Address Register ( MAR )

- Stores the address of the data that contains a piece of instruction to be used

## Memory Data Register ( MDR )

 - Acts like a buffer
 - Stores data that is about to be written to memory

## Current Instruction Register ( CIR )

- Holds the instruction to be executed

## State the function of the *System Clock* is a processor

- To generate the timing signals to synchronise fetch-decode-execute cyle

# Interrupt

## How interrupt is detected

- During fetch-execute cycle
- It checks for an iterrupt
- If an interrupt flag is set;
- All the contents of the register is saved
- PC is loaded with the address of the Interrupt Service Routine

# Security

## Disk Mirroring

- Data are written on 2 or more disk at the same time ( simultaneously )

## Encryption

- Contents of data is scrambled so that they cannot be understood without a decryption key

## Backup

- Data is copied and stored in another location

# Operating System

## Task performed by OS to manage Main Memory

- Read/Writes data to/from RAM
- Allocates Virtual Memory ( Like the thing I used to create YT videos on )
- Paging ( Like the thing I used to create YT videos on )
- Segmentation

## Describe the purpose of Utility Software in a Computer

- Help to set-up and maintain the computer
- Example:
	- To check for system faults

# Compiler / Interpreter

## Drawbacks of Compiler

- Slow to produce executable file
	- Takes a lot of computer resources
- The **program** will not run if there are any errors
- Code needs to be recompiled to be able to see changes
- Cannot easily test unfinished code

## Explain why HLL Programs might be *partially*  compiled and *partially* interpreted

- Code is optimised CPU as machine code is generated at run time
- Partially compiled program can be used on different platforms as they are interpreted when run
