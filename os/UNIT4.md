# Deadlock

## Deadlock Characterization

- **Definition**: A situation where a set of processes are blocked because each process holds a resource and is waiting for another resource acquired by some other process in the set.

- **Necessary Conditions (Coffman Conditions)**:
  1. **Mutual Exclusion**: Only one process can use a resource at any given time.
  2. **Hold and Wait**: A process holding at least one resource is waiting to acquire additional resources held by other processes.
  3. **No Preemption**: Resources cannot be forcibly taken away from a process; they must be released voluntarily.
  4. **Circular Wait**: A circular chain of two or more processes, each waiting for a resource held by the next one in the chain.

## Handling of Deadlocks

### Deadlock Prevention

- **Strategy**: Ensure that at least one of the four conditions of deadlock can't hold.
  - **Eliminate Mutual Exclusion**: Use resources that can be shared.
  - **Hold and Wait**: Require processes to request all needed resources at once or none at all.
  - **Preemption**: Allow resources to be forcibly taken away from processes.
  - **Circular Wait**: Order resources by ID and require processes to request them in that order.

### Deadlock Avoidance

- **Strategy**: Only grant resource requests if they lead to safe states, where there's always a sequence of execution that avoids deadlock.

  - **Banker's Algorithm**: 
    - **Safe State**: If there's at least one sequence where all processes can get all resources they need without deadlock.
    - **Resource Allocation Graph**: Graphical method for deadlock avoidance, but complex for large systems.

### Deadlock Detection

- **Strategy**: Let deadlock occur but use algorithms to detect it periodically.
  - **Detection Algorithm**: Check for cycles in the resource allocation graph or use a matrix approach to see if there's a sequence for resource allocation.

- **Detection Frequency**: 
  - More frequent detection increases overhead but catches deadlocks quicker.

### Deadlock Recovery

- **Process Termination**: 
  - **Abort all deadlocked processes** - Simple but costly.
  - **Abort one process at a time** until deadlock is resolved - More efficient but requires multiple checks.

- **Resource Preemption**:
  - **Selectively preempt resources** from processes, considering factors like cost of preemption, process priority, and how much work has been done.

## Starvation

- **Starvation**: A process is indefinitely postponed due to resource allocation to other processes.
  - **Contrast with Deadlock**: In starvation, processes are not blocked waiting on each other but simply never get scheduled.
  
- **Mitigation**: 
  - **Aging**: Increase the priority of waiting processes over time.
  - **Fair Scheduling**: Implement scheduling algorithms that ensure each process gets some CPU time.

# Protection and Security

## Need for Security

- **Protection**: Mechanisms to control access to resources by users/processes.
- **Security**: Protecting data from unauthorized access or alteration, ensuring integrity, confidentiality, and availability.

## Security Vulnerabilities

- **Buffer Overflow**: Writing data beyond the boundary of allocated memory, potentially allowing code execution.
- **Trapdoors**: Secret entry points into a program for debugging or maintenance, which can be exploited if known.
- **Backdoors**: Similar to trapdoors but intentionally left for malicious access.
- **Cache Poisoning**: Manipulating cached data to serve incorrect or malicious content.

## Authentication

### Password-based Authentication

- **Mechanism**: Users prove identity via secrets only they should know.
- **Challenges**: 
  - **Strength of Passwords**: Complex enough to resist guessing or cracking.
  - **Hashing**: Storing passwords in a hashed form; use salt to prevent rainbow table attacks.

### Password Maintenance

- **Policies**: Expiration, complexity requirements, lockout after failed attempts.
- **Secure Communication**: Use secure protocols like TLS for password transmission.

## Application Security

- **Virus**: Malicious code that replicates by copying itself into other programs.
  - **Countermeasures**: Antivirus software, sandboxing, and regular updates.

- **Program Threats**: 
  - **Trojan Horses**: Malicious code hidden within legitimate software.
  - **Logic Bombs**: Code that executes under certain conditions to cause harm.
  - **Worms**: Self-replicating malware that spreads over networks.

## Goals of Protection

- **Confidentiality**: Prevent unauthorized disclosure of information.
- **Integrity**: Protection against unauthorized data modification.
- **Availability**: Ensure that authorized users have access to resources when needed.

## Principles of Protection

- **Least Privilege**: Users should have only the minimum necessary rights to perform their job.
- **Separation of Duties**: Distribute critical tasks among different people to prevent fraud or errors.
- **Defense in Depth**: Use multiple layers of security controls.

## Domain of Protection

- **Domains**: A set of objects (resources) to which access is controlled. Processes can switch domains.

## Access Matrix

- **Concept**: A table where rows represent domains/subjects, columns represent objects/resources, and entries define permissions.
- **Implementation**:
  - **Access Lists**: Each object has a list of subjects and their access rights.
  - **Capability Lists**: Each subject has a list of capabilities (tokens) that grant access to objects.

## System and Network Threats

- **System Threats**: 
  - **Malware**: Viruses, worms, trojans.
  - **Rootkits**: Conceal malware by modifying OS internals.

- **Network Threats**:
  - **Denial of Service (DoS)**: Overwhelming network resources to make services unavailable.
  - **Man-in-the-Middle Attacks**: Intercepting communication to eavesdrop or alter data.

## Examples of Attacks

- **Phishing**: Tricking individuals into revealing sensitive information by posing as a trustworthy entity.
- **SQL Injection**: Exploiting vulnerabilities in database queries to execute unauthorized commands.
- **Cross-Site Scripting (XSS)**: Injecting malicious scripts into web pages viewed by other users.

These notes provide a comprehensive look at the complexities of managing deadlocks and ensuring security within computing environments. Understanding these concepts is vital for designing and maintaining secure and efficient systems.
