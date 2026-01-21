# 🚀 SyntaX for Fortran
**Modernizing Fortran development with a clean and intuitive syntax.**

SyntaX for Fortran is a lightweight, high-performance module designed to simplify standard Fortran procedures. Built for **Fortran 2018** standards, it bridges the gap between classic scientific computing and modern coding simplicity.

---

## 📊 Development Comparison

See how **SyntaX** simplifies standard Fortran 90/2018 operations:

| Feature | Standard Fortran | **SyntaX for Fortran** |
| :--- | :--- | :--- |
| **Output** | `print *, "Message"` | `call print_s("Message")` |
| **User Input** | `read(*, '(A)') var` | `call input_s("Name:", var)` |
| **Sleep/Wait** | `call system_clock(...)` (Complex) | `call sleep_s(2.0)` |
| **Clear Screen** | `call execute_command_line('cls')` | `call clear_s()` |

---

## 🛠️ Features
- **Simplified I/O:** No more worrying about complex format strings for basic tasks.
- **Modern Timing:** High-precision sleep function using `system_clock`.
- **Clean Architecture:** Built as a standalone module for easy integration.
- **Optimized for GCC 15+:** Fully compatible with the latest `gfortran` compilers.

---

## 🚀 Quick Start

### 1. Installation
Copy `bettersyntax.f90` into your project directory.

### 2. Compilation
To use the library, compile the module first, then link it with your source code:

$ gfortran -c bettersyntax.f90
$ gfortran samples.f90 bettersyntax.o -o my_program

### 3. Usage Example (samples.f90)

program samples
    use bettersyntax
    implicit none
    
    character(len=32) :: username

    call clear_s()
    call print_s("SyntaX for Fortran Initialized!")
    
    call input_s("Enter your name:", username)
    call print_s("Welcome, " // trim(username))
    
    call sleep_s(1.5)
    call print_s("Done.")
end program samples

---

## 📜 License
This project is licensed under the **GPL-3.0 License**.  
Copyright (c) 2026 **hypernova-developer**.
