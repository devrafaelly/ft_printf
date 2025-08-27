# ft_printf – 42 C Library

---

## Description

The **ft_printf** project is a custom implementation of the standard C `printf` function.  
It allows formatting and printing of different types of data to the standard output.  
The goal is to understand **variadic functions**, **format parsing**, and **output handling in C**.

---

## Compilation

Clone the repository and compile with `make`:

```bash
git clone https://github.com/devrafaelly/ft_printf.git
cd ft_printf
make
````

This will generate the library `libftprintf.a`.

---

## Usage

Include the header and link the library in your C project:

```c
#include "ft_printf.h"

int main(void)
{
    int ret;

    ret = ft_printf("Hello %s, number: %d\n", "libft", 42);
    ft_printf("Printed %d characters.\n", ret);
    return 0;
}
```

Compile with:

```bash
cc _Wall -Werror -Wextra main.c -L. -lftprintf
```

---

## Features

* Handles format specifiers:

  * `%c` → character
  * `%s` → string
  * `%p` → pointer
  * `%d`, `%i` → integer
  * `%u` → unsigned integer
  * `%x`, `%X` → hexadecimal
  * `%%` → percent sign

* Returns the number of characters printed (like the standard `printf`).

* Supports multiple arguments using variadic functions (`stdarg.h`).

---

## Project Structure

```
ft_printf/
├── Makefile
├── ft_printf.h
└── ft_*.c
```

---

## 🎯 Goals

* Learn how `printf` works internally
* Master variadic functions in C
* Handle string parsing and formatting
* Provide a reusable function for formatted output in C projects

---

## 👤 Author

Project developed by [**Rafaelly Diniz**](https://github.com/devrafaelly) as part of the **42 curriculum**.
