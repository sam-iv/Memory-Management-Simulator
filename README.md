# Non-Contiguous Segmented Memory Manager Simulation

This project is a Java-based simulation of a non-contiguous segmented memory manager, demonstrating key concepts of operating system memory management. It was developed as university coursework, and has since been archived.

The report for this coursework can be found [here](report.pdf)

The simulation includes features like:
*   **Segmentation:** Memory is divided into segments of varying sizes.
*   **Non-Contiguous Allocation:** Segments of a process can be stored in different parts of memory.
*   **Dynamic Allocation and Deallocation:** Processes and segments can be allocated and deallocated from memory at runtime.
*   **Process Resizing:** The size of a process's segments can be changed dynamically.
*   **Memory Protection:** Segments have read, write, and execute permissions.
*   **Translation Lookaside Buffer (TLB):** A TLB is used to cache virtual-to-physical address translations to speed up memory access.
*   **Error Handling:** The simulation includes robust error handling for invalid operations and inputs.

## Getting Started

This project is built with Apache Maven. Please ensure you have JDK 11 (or newer) and Maven installed on your system.

1.  Clone the repository:
    ```bash
    git clone https://github.com/sam-iv/Memory-Management-Simulator.git
    ```
2.  Go to the project directory and run the application using Maven:
    ```bash
    # For Windows, macOS, or Linux
    mvn clean compile exec:java
    ```

## Usage

The program's output displays a step-by-step simulation of the memory manager's operations. Here's how to interpret the key parts of the output:

*   **Memory State:** The `[OS size] | [Hole size]` line shows the amount of memory allocated to the operating system and the amount of free memory (holes).
*   **Segment Tables:** The segment tables show the details of each segment, including its ID (SID), base address, limit (size), valid-invalid bit, and permissions.
*   **TLB Hits and Misses:** The output indicates whether a memory access results in a Translation Lookaside Buffer (TLB) hit or miss. A TLB hit means the address translation was found in the TLB, while a miss means it had to be fetched from the segment table.

## Technologies Used

This project is built using Java 11 and Maven.

- ### Core Language & Build Tool:
    - **Java 11** - Core Language for the application.
    - **Maven** - Build and dependency management tool.
