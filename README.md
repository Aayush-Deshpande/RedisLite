# 🚀 RedisLite — In-Memory Key-Value Store

RedisLite is a lightweight, high-performance in-memory data store inspired by Redis.  
This project explores core system design concepts such as network programming, concurrency, and efficient data handling by building a Redis-like server from scratch.

---

## 🧠 Overview

RedisLite is designed to mimic the fundamental behavior of Redis by implementing:

- A TCP server capable of handling multiple client connections  
- Parsing and processing of the Redis Serialization Protocol (RESP)  
- Core Redis commands for data storage and retrieval  
- In-memory data structures optimized for low-latency access  

This project focuses on understanding **how real-world caching systems work internally**, rather than just using them.

---

## ⚙️ Features

### 🔹 Core Functionality
- Implemented a TCP server that listens for incoming client connections  
- Built support for handling multiple clients concurrently  
- Designed a command processing engine for:
  - `PING` — connectivity check  
  - `ECHO` — message reflection  
  - `SET` — store key-value pairs  
  - `GET` — retrieve stored values  

### 🔹 Protocol Handling
- Implemented parsing and encoding of the **Redis Serialization Protocol (RESP)**  
- Enabled seamless interaction with official Redis CLI (`redis-cli`)  

### 🔹 Data Management
- Designed an in-memory key-value store for O(1) data access  
- Added support for **automatic key expiration (TTL)**  

---

## 🚀 Advanced Concepts Implemented

- 🔁 Replication (master-replica architecture basics)  
- 💾 RDB-style persistence (snapshotting data to disk)  
- 🔒 Atomic operations for safe concurrent execution  
- 🧩 Extensible architecture for additional data structures  

---

## 🏗️ System Design Highlights

- Built using **low-level networking (TCP sockets)**  
- Implemented **concurrent client handling**  
- Designed modular components for:
  - Command parsing  
  - Data storage  
  - Client communication  

---

## 📦 Tech Stack

- Language: *Python*  
- Networking: TCP Sockets  
- Protocol: RESP (Redis Serialization Protocol)  
- Concepts: Concurrency, System Design, In-Memory Databases  

---

## ⚡ Why This Project Matters

Modern applications rely heavily on caching systems like Redis for:

- Reducing latency  
- Scaling backend systems  
- Handling high-throughput workloads  

RedisLite demonstrates a deep understanding of:
- How caching systems operate internally  
- How distributed systems manage data efficiently  
- How real-world infrastructure tools are built  

---

## 🧪 Example Usage

```bash
$ redis-cli
127.0.0.1:6379> PING
PONG

127.0.0.1:6379> SET name Aayush
OK

127.0.0.1:6379> GET name
"Aayush"
