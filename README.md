# TryHackMe SQL Injection Lab

This repository contains solutions for the TryHackMe SQL Injection Lab. The lab aims to help users understand how SQL injection attacks work and how to exploit this vulnerability effectively.

## Description

SQL injection is a common web security vulnerability that allows an attacker to interfere with the queries that an application makes to its database. This can result in unauthorized access to sensitive data, manipulation of database contents, and even execution of administrative operations on the database server.

In this lab, we explore different techniques and tools used to exploit SQL injection vulnerabilities. The repository provides both a binary search solution and the original script for retrieving passwords from a vulnerable web application.

## Binary Search Solution

The binary search solution is an optimized approach to retrieve passwords from a vulnerable web application using a binary search algorithm. This algorithm efficiently narrows down the search space for each character of the password, significantly reducing the number of requests needed to find each character. The solution employs recursive binary search to efficiently locate each character of the password, making it faster and more scalable for longer passwords. 

**Improvement in Time Complexity:** 
The time complexity of the binary search algorithm is O(log n), where n is the number of possible characters in the character set. This is a significant improvement over the linear search approach, which has a time complexity of O(n).

**Improvement in Space Complexity:** 
The space complexity of the binary search algorithm is O(1), as it does not require additional space proportional to the input size. In contrast, the linear search approach may require O(n) space to store intermediate results.

The binary approach is able to capture the flag in under 2 minutes, demonstrating its effectiveness in real-world scenarios.

## Original Script

The original script provided in this repository demonstrates a basic approach to retrieve passwords from a vulnerable web application using a linear search method. While functional, this approach is less efficient, especially for longer passwords, as it iterates through all possible characters for each position in the password. Despite its simplicity, the script provides valuable insights into the concept of exploiting SQL injection vulnerabilities and serves as a starting point for understanding more advanced techniques.

## Usage

1. Clone the repository:
   ```
   git clone https://github.com/TreezCode/TryHackMe-SQL-Injection-Lab.git
   ```

2. Navigate to the cloned directory:
   ```
   cd TryHackMe-SQL-Injection-Lab
   ```

3. Run the script:
   ```
   python challenge3-exploit-binary.py MACHINE_IP:PORT
   ```
   or
   ```
   python challenge3-exploit.py MACHINE_IP:PORT
   ```

Replace `MACHINE_IP:PORT` with the IP address and port number of the vulnerable web application.

## Contributors

- [TreezCode](https://github.com/TreezCode)

## License

This project is licensed under the [MIT License](LICENSE).
