# Multi-threaded Event Reservation System

## Overview

This is a multi-threaded event reservation system implemented in C. The system allows multiple threads to perform various types of queries (inquiry, booking, cancellation) on events. It uses mutexes and condition variables to ensure synchronization and prevent conflicts among the threads.

## Features

- Supports concurrent queries (inquiry, booking, cancellation) on events.
- Manages available seats for each event.
- Ensures thread synchronization and prevents conflicts using mutexes and condition variables.
- Provides a time-based termination mechanism for threads.

## Code Structure

- `main.c`: The main program file containing the implementation of the event reservation system.
- `pthread.h`, `stdio.h`, `stdlib.h`, `stdbool.h`, `unistd.h`, `time.h`: Included header files for the C standard library and POSIX threads.

## How to Run

1. Compile the code: `gcc -o event_reservation main.c -lpthread`
2. Run the executable: `./event_reservation`

## Configuration

- `MAX_EVENTS`: Maximum number of events supported by the system.
- `CAPACITY`: Maximum capacity of each event.
- `BOOK_MIN`, `BOOK_MAX`: Minimum and maximum number of seats that can be booked.
- `MAX_THREADS`: Maximum number of worker threads.
- `MAX_ACTIVE_QUERIES`: Maximum number of active queries allowed.
- `MAX_TIME`: Time limit (in minutes) for which threads will run.

## Usage

1. Compile and run the program using the provided instructions.
2. The program will simulate multiple threads performing queries on events concurrently.
3. Queries include inquiry, booking, and cancellation of seats.
4. The program ensures synchronization and prevents conflicts using mutexes and condition variables.
5. Threads terminate after reaching the time limit specified in `MAX_TIME`.

## Notes

- This code is intended for educational purposes and may not be suitable for production use without further refinement.
- The time limit mechanism uses `clock()`, which might not be the most accurate way to track time.

## Disclaimer

This code was developed as a learning exercise and is not guaranteed to be free of errors or suitable for all scenarios. Use it at your own risk.

---

Feel free to modify and expand upon this README to include any additional details or explanations relevant to your specific use case and audience.
