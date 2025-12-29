# Parallel File Encryptor & Decryptor 

A **high-performance file encryptor and decryptor** built in **C++**, designed using **Operating System concepts** such as **multiprocessing**, **shared memory**, and **process synchronization**.  
This project focuses on encrypting and decrypting files **in parallel** to improve performance on multi-core systems.

---

## About the Project

**Parallel File Encryptor & Decryptor** demonstrates how real-world systems can leverage:
- **Multiple processes**
- **Shared memory**
- **Process management**
- **File I/O handling**

to efficiently encrypt and decrypt large files.

The project is structured cleanly with modular components for **encryption**, **file handling**, and **process management**, making it easy to extend and understand.

---

##  Key Features

- **Parallel Encryption & Decryption**
- Uses **multiprocessing** (OS-level processes)
- **Shared memory** for inter-process communication
- Modular project structure
- Written in **modern C++**
- Test files included
- Easy to extend for new encryption algorithms

---

## OS Concepts Used

- **Multiprocessing**
- **Shared Memory**
- **Semaphores**
- **Mutex/Locks**
- **Process Synchronization**
- **File System I/O**
- **Task Management**

---

## Project Structure

```

File-encryptor-decryptor/
│
├── .vscode/                            # for debugging purpose
│   ├── launch.json
│   ├── settings.json
│   └── tasks.json
│
├── src/
│   └── app/
│       ├── encryptDecrypt/             # encrypt/decrypt logic
│       │   ├── Cryption.cpp
│       │   ├── Cryption.hpp
│       │   └── CryptionMain.cpp
│       │
│       ├── fileHandling/               # reading from file 
│       │   ├── IO.cpp
│       │   ├── IO.hpp
│       │   └── ReadEnv.cpp
│       │
│       └── processes/                  # executes multiple processes parallelly
│           ├── ProcessManagement.cpp
│           ├── ProcessManagement.hpp
│           └── Task.hpp
│
├── test/                               # test files can be generated using .py script
│   ├── test1.txt
│   └── test2.txt
│
├── .env                                # encryption secret key 
├── main.cpp                            # main file to run 
├── makeDirs.py                         # to automate test/
└── Makefile                            # to run 

````

---

## How It Works

-  Input files are split into chunks  
- Multiple processes are spawned  
- Each process encrypts/decrypts a chunk  
- Shared memory is used to coordinate data  
- Final output is merged efficiently  

---

## 🛠 Build & Run

### Prerequisites
- Linux (tested on **Ubuntu / WSL**)
- `g++`
- `make`

### Build
```bash
make
````

### Run

```bash
./encrypt_decrypt
```

---

## Testing

Sample test files are provided in the `test/` directory:

```bash
test/test1.txt
test/test2.txt
```

Use them to verify encryption and decryption behavior.

---

## Performance

* Faster than single-threaded encryption for large files
* Scales with number of CPU cores
* Demonstrates real OS-level parallelism (not just threads)

---
