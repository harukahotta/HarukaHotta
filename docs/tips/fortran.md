---
layout: default
title: Fortran
parent: Tips 
---

# Fortran
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

I don't like Fortran 77  
Basically use gfortran


## Bug fix

### compile option

`gfortran -Wall -fbounds-check -O -Wuninitialized -ffpe-trap=invalid,zero,overflow -fbacktrace hoge.f90`

`-fbounds-check` Enable generation of **run-time checks for array subscripts** and against the declared minimum and maximum values. It also checks array indices for assumed and deferred shape arrays against the actual allocated bounds and ensures that all string lengths are equal for character array constructors without an explicit typespec.   
`-Wall`  Enables **commonly used warning options** pertaining to usage that we recommend avoiding and that we believe are easy to avoid.  
`-Wuninitialized` Warn if an automatic variable is used without first being initialized.  
`-ffpe-trap=invalid,zero,overflow` `invalid` invalid floating point operation. `zero` division by zero, `overflow` overflow in a floating point operation.  
`-fbacktrace` When a runtime error is encountered or a deadly signal is emitted (segmentation fault, illegal instruction, bus error or floating-point exception), the Fortran runtime library should **output a backtrace of the error**. This option only has influence for compilation of the Fortran main program.  
`-g`  

### size

`ulimit -s`  
`ulimit -s unlimited`

`gfororan -mcmodel=large hoge.f90`

## IO

### read file

```fortran
integer :: ios
open(..., iostat=ios, ...)
if (ios > 0) then
     write(*,*) 'Failed to open file for output'
   stop
if (ios < 0) then
     write(*,*) 'End of file'
   stop
end if
```


## character

### character length
`character(len=*), parameter :: text = 'initialization by this string'`

## function and subroutine

Variables defined in function/subroutine is independent from other function/subroutine and main program.

```fortran
program sample
  implicit none

  !main program
  stop
contains

real(4) function plus1(x)
  implicit none
  real(4) :: x

  plus1 = x + 1.0

  return
end function plus1

subroutine hello(name)
  implicit none
  character(len=*) :: name

  write(*,*) 'Hello ', name

  return
end subroutine hello

subroutine add(a, b, c)
  implicit none
  real(4), intent(in)  :: a, b
  real(4), intent(out) :: c

  c = a + b

end subroutine add

end program sample
```

