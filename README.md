# 🖨️ ft_printf - Because ft_putstr isn't enough

<p align="center">
  <img src="https://img.shields.io/badge/Language-C-blue.svg" alt="Language C">
  <img src="https://img.shields.io/badge/School-42-black.svg" alt="School 42">
  <img src="https://img.shields.io/badge/Score-100%2F100-success.svg" alt="Score">
  <img src="https://img.shields.io/badge/Concept-Variadic%20Functions-orange.svg" alt="Variadic Functions">
</p>

> *"Reinventing the wheel just to understand how it rolls."*

## 🌟 About the Project

**ft_printf** is a project from the **School 42** curriculum that requires recoding the famous `printf` function from the C standard library (`libc`). 

The main challenge and learning objective of this project is to discover and implement **variadic functions** in C (using `stdarg.h`), allowing a function to accept an indefinite number of arguments. It also reinforces clean code architecture and efficient string parsing.

## 🎯 Supported Conversions

This lightweight clone handles the following core format specifiers perfectly:

| Specifier | Description |
| :---: | :--- |
| `%c` | Prints a single character. |
| `%s` | Prints a string (as defined by the common C convention). |
| `%p` | The `void *` pointer argument has to be printed in hexadecimal format. |
| `%d` | Prints a decimal (base 10) number. |
| `%i` | Prints an integer in base 10. |
| `%u` | Prints an unsigned decimal (base 10) number. |
| `%x` | Prints a number in hexadecimal (base 16) lowercase format. |
| `%X` | Prints a number in hexadecimal (base 16) uppercase format. |
| `%%` | Prints a literal `%` sign. |

## 🛠️ Architecture

Instead of a monolithic spaghetti-code function, this project is built with modularity in mind:
* **Main Parser:** Iterates through the string and identifies format tags.
* **Dispatcher:** Routes the argument to the correct specific printing function based on the specifier.
* **Formatters:** Dedicated isolated functions for handling numbers, hexadecimals, memory addresses, and strings.

## ⚙️ Build and Usage

The library is compiled via `Makefile` into a static library (`libftprintf.a`), making it plug-and-play for any C project.

**1. Clone the repository:**
```bash
git clone [https://github.com/YOUR_USERNAME/ft_printf.git](https://github.com/YOUR_USERNAME/ft_printf.git)
cd ft_printf
