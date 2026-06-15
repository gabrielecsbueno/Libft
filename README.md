# Libft

Reimplementation in C of essential functions from the standard library (`libc`), along with additional utility functions. Project developed at **42 Barcelona** as a foundation for future curriculum projects.

---

## Functions

## Character Checks

### **ft_isalpha**

```c
int ft_isalpha(int c)
```
Checks whether the character is a letter (a–z / A–Z).
Returns `1` if true, `0` if false.

---

### **ft_isdigit**

```c
int ft_isdigit(int c)
```
Checks whether the character is a digit (0–9).
Returns `1` if true, `0` if false.

---

### **ft_isalnum**

```c
int ft_isalnum(int c)
```
Checks whether the character is alphanumeric (letter or digit).
Returns `1` if true, `0` if false.

---

### **ft_isascii**

```c
int ft_isascii(int c)
```
Checks whether the value is within the ASCII table (0–127).
Returns `1` if true, `0` if false.

---

### **ft_isprint**

```c
int ft_isprint(int c)
```
Checks whether the character is printable (32–126).
Returns `1` if true, `0` if false.

---

## Character Conversion

### **ft_toupper**

```c
int ft_toupper(int c)
```
Converts a lowercase letter to uppercase.
Returns the converted character, or the original if it is not a lowercase letter.

---

### **ft_tolower**

```c
int ft_tolower(int c)
```
Converts an uppercase letter to lowercase.
Returns the converted character, or the original if it is not an uppercase letter.

---

## Memory Manipulation

### **ft_memset**

```c
void *ft_memset(void *s, int c, size_t n)
```
Fills the first `n` bytes of the memory area `s` with the value `c`.
Returns a pointer to `s`.

---

### **ft_bzero**

```c
void ft_bzero(void *s, size_t n)
```
Zeros the first `n` bytes of the memory area pointed to by `s`.
Returns `void`.

---

### **ft_memcpy**

```c
void *ft_memcpy(void *dest, const void *src, size_t n)
```
Copies `n` bytes from `src` to `dest`. The areas must not overlap.
Returns a pointer to `dest`.

---

### **ft_memmove**

```c
void *ft_memmove(void *dest, const void *src, size_t n)
```
Copies `n` bytes from `src` to `dest`, correctly handling overlapping regions.
Returns a pointer to `dest`.

---

### **ft_memchr**

```c
void *ft_memchr(const void *s, int c, size_t n)
```
Searches for the first occurrence of byte `c` in the first `n` bytes of `s`.
Returns a pointer to the byte found, or `NULL` if not found.

---

### **ft_memcmp**

```c
int ft_memcmp(const void *s1, const void *s2, size_t n)
```
Compares the first `n` bytes of two memory areas.
Returns the difference between the first differing byte; `0` if equal.

---

### **ft_calloc**

```c
void *ft_calloc(size_t nmemb, size_t size)
```
Allocates memory for `nmemb` elements of `size` bytes and initializes everything to zero.
Returns a pointer to the allocated memory, or `NULL` on error.

---

## String Manipulation

### **ft_strlen**

```c
size_t ft_strlen(const char *s)
```
Calculates the length of the string, not counting the null character `\0`.
Returns the number of characters in the string.

---

### **ft_strlcpy**

```c
size_t ft_strlcpy(char *dst, const char *src, size_t dsize)
```
Copies `src` to `dst` with at most `dsize` bytes, guaranteeing null termination.
Returns the length of `src`.

---

### **ft_strlcat**

```c
size_t ft_strlcat(char *dst, const char *src, size_t dsize)
```
Appends `src` to the end of `dst`, respecting the total limit of `dsize` bytes.
Returns the total length the string would have had without the limit.

---

### **ft_strchr**

```c
char *ft_strchr(const char *s, int c)
```
Searches for the first occurrence of character `c` in string `s`.
Returns a pointer to the character found, or `NULL` if not found.

---

### **ft_strrchr**

```c
char *ft_strrchr(const char *s, int c)
```
Searches for the last occurrence of character `c` in string `s`.
Returns a pointer to the character found, or `NULL` if not found.

---

### **ft_strncmp**

```c
int ft_strncmp(const char *s1, const char *s2, size_t n)
```
Compares the first `n` characters of two strings.
Returns the difference between the first differing character; `0` if equal.

---

### **ft_strnstr**

```c
char *ft_strnstr(const char *big, const char *little, size_t len)
```
Searches for string `little` inside `big`, limiting the search to the first `len` characters.
Returns a pointer to the start of `little` in `big`, or `NULL` if not found.

---

### **ft_strdup**

```c
char *ft_strdup(const char *s)
```
Creates a copy of string `s` by allocating new memory with `malloc`.
Returns a pointer to the new string, or `NULL` on error.

---

## Type Conversion

### **ft_atoi**

```c
int ft_atoi(const char *nptr)
```
Converts a string to an integer, skipping leading whitespace and respecting sign.
Returns the converted integer value.

---

### **ft_itoa**

```c
char *ft_itoa(int n)
```
Converts an integer to a string, allocating memory for the result.
Returns a pointer to the generated string, or `NULL` on error.

---

## Additional String Functions

### **ft_substr**

```c
char *ft_substr(char const *s, unsigned int start, size_t len)
```
Extracts a substring from `s` starting at index `start` with a maximum length of `len`.
Returns a pointer to the new string, or `NULL` on error.

---

### **ft_strjoin**

```c
char *ft_strjoin(char const *s1, char const *s2)
```
Concatenates `s1` and `s2` into a newly allocated string.
Returns a pointer to the new string, or `NULL` on error.

---

### **ft_strtrim**

```c
char *ft_strtrim(char const *s1, char const *set)
```
Removes all characters present in `set` from the beginning and end of `s1`.
Returns a pointer to the resulting string, or `NULL` on error.

---

### **ft_split**

```c
char **ft_split(char const *s, char c)
```
Splits string `s` using character `c` as a delimiter.
Returns a null-terminated array of strings, or `NULL` on error.

---

### **ft_strmapi**

```c
char *ft_strmapi(char const *s, char (*f)(unsigned int, char))
```
Creates a new string by applying function `f` to each character of `s`, passing the index.
Returns a pointer to the new string, or `NULL` on error.

---

### **ft_striteri**

```c
void ft_striteri(char *s, void (*f)(unsigned int, char*))
```
Applies function `f` to each character of `s`, modifying it directly in-place, passing the index.
Returns `void`.

---

## Output to File Descriptor

### **ft_putchar_fd**

```c
void ft_putchar_fd(char c, int fd)
```
Writes character `c` to file descriptor `fd`.
Returns `void`.

---

### **ft_putstr_fd**

```c
void ft_putstr_fd(char *s, int fd)
```
Writes string `s` to file descriptor `fd`.
Returns `void`.

---

### **ft_putendl_fd**

```c
void ft_putendl_fd(char *s, int fd)
```
Writes string `s` followed by a newline to file descriptor `fd`.
Returns `void`.

---

### **ft_putnbr_fd**

```c
void ft_putnbr_fd(int n, int fd)
```
Writes integer `n` to file descriptor `fd`.
Returns `void`.

---

## How to Compile and Use

### Compile the library

```bash
make
```

Generates the `libft.a` file in the root directory.

### Remove object files

```bash
make clean
```

### Remove everything (objects + library)

```bash
make fclean
```

### Recompile from scratch

```bash
make re
```

### Use in your project

Copy `libft.a` and `lib/libft.h` to your project directory, include the header:

```c
#include "libft.h"
```

And compile linking the library:

```bash
cc -Wall -Wextra -Werror main.c -L. -lft -o program
```

---

*Projeto desenvolvido por [gabde-so](https://profile-v3.intra.42.fr/users/gabde-so) na [42 Barcelona](https://www.42barcelona.com/)*
