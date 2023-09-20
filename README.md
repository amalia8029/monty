# Project 0x19 - C - Stacks, Queues - LIFO, FIFO

This project was developed by [Elmehdi Bouslam](https://github.com/Mido-Hyuga) and [Amal Hadraoui](https://github.com/amalia8029).

## About

In this project, we have created a simple interpreter for Monty ByteCodes. The interpreter reads a bytecode file and executes the bytecode commands.

The Monty Language

Monty 0.98 is a scripting language that is first compiled into Monty byte codes (similar to Python). It relies on a unique stack, with specific instructions to manipulate it.

## Monty Byte Code Files

Files containing Monty byte codes usually have the .m extension. While most of the industry follows this standard, it is not required by the language specification. There should not be more than one instruction per line. There can be any number of spaces before or after the opcode and its argument.

## Objectives

- To understand what LIFO and FIFO mean.
- To understand what a stack is and when to use it.
- To understand what a queue is and when to use it.
- To understand common implementations of stacks and queues.
- To understand the most common use cases of stacks and queues.
- To know how to properly use global variables.

## Resources

- [Difference between Stack and Queue Data Structures](https://www.geeksforgeeks.org/difference-between-stack-and-queue-data-structures/)

## General Requirements

- Allowed editors: vi, vim, emacs.
- All files are compiled on Ubuntu 20.04 LTS using gcc, using the options `-Wall -Werror -Wextra -pedantic -std=gnu89`.
- All files end with a new line.
- There is a README.md file at the root of the alx-low_level_programming.
- A maximum of one global variable is allowed.
- No more than 5 functions per file.
- The C standard library is allowed.
- The prototypes of all the functions are included in the header file called `monty.h`.
- All header files are include guarded.

## Instructions Given

To use the following data structures for this project, and to also include them in the header file:

``c
/**
 * struct stack_s - doubly linked list representation of a stack (or queue)
 * @n: integer
 * @prev: points to the previous element of the stack (or queue)
 * @next: points to the next element of the stack (or queue)
 * Description: doubly linked list node structure
 * for stack, queues, LIFO, FIFO
 */
typedef struct stack_s
{
    int n;
    struct stack_s *prev;
    struct stack_s *next;
} stack_t;

/**
 * struct instruction_s - opcode and its function
 * @opcode: the opcode
 * @f: function to handle the opcode
 * Description: opcode and its function
 * for stack, queues, LIFO, FIFO
 */
typedef struct instruction_s
{
    char *opcode;
    void (*f)(stack_t **stack, unsigned int line_number);
} instruction_t;

## Compilation & Output

These codes were compiled using:
 gcc -Wall -Werror -Wextra -pedantic -std=c89 *.c -o monty

