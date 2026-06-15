# Libft

Reimplementación en C de funciones esenciales de la biblioteca estándar (`libc`), junto con funciones utilitarias adicionales. Proyecto desarrollado en **42 Barcelona** como base para los proyectos futuros del currículo.

---

## Funciones

## Comprobación de Caracteres

### **ft_isalpha**

```c
int ft_isalpha(int c)
```
Comprueba si el carácter es una letra (a–z / A–Z).
Devuelve `1` si es verdadero, `0` si es falso.

---

### **ft_isdigit**

```c
int ft_isdigit(int c)
```
Comprueba si el carácter es un dígito (0–9).
Devuelve `1` si es verdadero, `0` si es falso.

---

### **ft_isalnum**

```c
int ft_isalnum(int c)
```
Comprueba si el carácter es alfanumérico (letra o dígito).
Devuelve `1` si es verdadero, `0` si es falso.

---

### **ft_isascii**

```c
int ft_isascii(int c)
```
Comprueba si el valor está dentro de la tabla ASCII (0–127).
Devuelve `1` si es verdadero, `0` si es falso.

---

### **ft_isprint**

```c
int ft_isprint(int c)
```
Comprueba si el carácter es imprimible (32–126).
Devuelve `1` si es verdadero, `0` si es falso.

---

## Conversión de Caracteres

### **ft_toupper**

```c
int ft_toupper(int c)
```
Convierte una letra minúscula en mayúscula.
Devuelve el carácter convertido, o el original si no es una letra minúscula.

---

### **ft_tolower**

```c
int ft_tolower(int c)
```
Convierte una letra mayúscula en minúscula.
Devuelve el carácter convertido, o el original si no es una letra mayúscula.

---

## Manipulación de Memoria

### **ft_memset**

```c
void *ft_memset(void *s, int c, size_t n)
```
Rellena los primeros `n` bytes del área de memoria `s` con el valor `c`.
Devuelve un puntero a `s`.

---

### **ft_bzero**

```c
void ft_bzero(void *s, size_t n)
```
Pone a cero los primeros `n` bytes del área de memoria apuntada por `s`.
Devuelve `void`.

---

### **ft_memcpy**

```c
void *ft_memcpy(void *dest, const void *src, size_t n)
```
Copia `n` bytes de `src` a `dest`. Las áreas no deben solaparse.
Devuelve un puntero a `dest`.

---

### **ft_memmove**

```c
void *ft_memmove(void *dest, const void *src, size_t n)
```
Copia `n` bytes de `src` a `dest`, tratando correctamente las regiones solapadas.
Devuelve un puntero a `dest`.

---

### **ft_memchr**

```c
void *ft_memchr(const void *s, int c, size_t n)
```
Busca la primera ocurrencia del byte `c` en los primeros `n` bytes de `s`.
Devuelve un puntero al byte encontrado, o `NULL` si no se encuentra.

---

### **ft_memcmp**

```c
int ft_memcmp(const void *s1, const void *s2, size_t n)
```
Compara los primeros `n` bytes de dos áreas de memoria.
Devuelve la diferencia entre el primer byte divergente; `0` si son iguales.

---

### **ft_calloc**

```c
void *ft_calloc(size_t nmemb, size_t size)
```
Reserva memoria para `nmemb` elementos de `size` bytes e inicializa todo a cero.
Devuelve un puntero a la memoria reservada, o `NULL` en caso de error.

---

## Manipulación de Cadenas

### **ft_strlen**

```c
size_t ft_strlen(const char *s)
```
Calcula la longitud de la cadena, sin contar el carácter nulo `\0`.
Devuelve el número de caracteres de la cadena.

---

### **ft_strlcpy**

```c
size_t ft_strlcpy(char *dst, const char *src, size_t dsize)
```
Copia `src` en `dst` con un máximo de `dsize` bytes, garantizando la terminación con `\0`.
Devuelve la longitud de `src`.

---

### **ft_strlcat**

```c
size_t ft_strlcat(char *dst, const char *src, size_t dsize)
```
Añade `src` al final de `dst`, respetando el límite total de `dsize` bytes.
Devuelve la longitud total que tendría la cadena sin el límite.

---

### **ft_strchr**

```c
char *ft_strchr(const char *s, int c)
```
Busca la primera ocurrencia del carácter `c` en la cadena `s`.
Devuelve un puntero al carácter encontrado, o `NULL` si no se encuentra.

---

### **ft_strrchr**

```c
char *ft_strrchr(const char *s, int c)
```
Busca la última ocurrencia del carácter `c` en la cadena `s`.
Devuelve un puntero al carácter encontrado, o `NULL` si no se encuentra.

---

### **ft_strncmp**

```c
int ft_strncmp(const char *s1, const char *s2, size_t n)
```
Compara los primeros `n` caracteres de dos cadenas.
Devuelve la diferencia entre el primer carácter divergente; `0` si son iguales.

---

### **ft_strnstr**

```c
char *ft_strnstr(const char *big, const char *little, size_t len)
```
Busca la cadena `little` dentro de `big`, limitando la búsqueda a los primeros `len` caracteres.
Devuelve un puntero al inicio de `little` en `big`, o `NULL` si no se encuentra.

---

### **ft_strdup**

```c
char *ft_strdup(const char *s)
```
Crea una copia de la cadena `s` reservando nueva memoria con `malloc`.
Devuelve un puntero a la nueva cadena, o `NULL` en caso de error.

---

## Conversión de Tipos

### **ft_atoi**

```c
int ft_atoi(const char *nptr)
```
Convierte una cadena en un entero, ignorando los espacios iniciales y respetando el signo.
Devuelve el valor entero convertido.

---

### **ft_itoa**

```c
char *ft_itoa(int n)
```
Convierte un entero en una cadena, reservando memoria para el resultado.
Devuelve un puntero a la cadena generada, o `NULL` en caso de error.

---

## Funciones Adicionales de Cadena

### **ft_substr**

```c
char *ft_substr(char const *s, unsigned int start, size_t len)
```
Extrae una subcadena de `s` a partir del índice `start` con una longitud máxima de `len`.
Devuelve un puntero a la nueva cadena, o `NULL` en caso de error.

---

### **ft_strjoin**

```c
char *ft_strjoin(char const *s1, char const *s2)
```
Concatena `s1` y `s2` en una nueva cadena reservada con `malloc`.
Devuelve un puntero a la nueva cadena, o `NULL` en caso de error.

---

### **ft_strtrim**

```c
char *ft_strtrim(char const *s1, char const *set)
```
Elimina todos los caracteres presentes en `set` del inicio y del final de `s1`.
Devuelve un puntero a la cadena resultante, o `NULL` en caso de error.

---

### **ft_split**

```c
char **ft_split(char const *s, char c)
```
Divide la cadena `s` usando el carácter `c` como delimitador.
Devuelve un array de cadenas terminado en `NULL`, o `NULL` en caso de error.

---

### **ft_strmapi**

```c
char *ft_strmapi(char const *s, char (*f)(unsigned int, char))
```
Crea una nueva cadena aplicando la función `f` a cada carácter de `s`, pasando el índice.
Devuelve un puntero a la nueva cadena, o `NULL` en caso de error.

---

### **ft_striteri**

```c
void ft_striteri(char *s, void (*f)(unsigned int, char*))
```
Aplica la función `f` a cada carácter de `s` modificándolo directamente (in-place), pasando el índice.
Devuelve `void`.

---

## Salida a File Descriptor

### **ft_putchar_fd**

```c
void ft_putchar_fd(char c, int fd)
```
Escribe el carácter `c` en el file descriptor `fd`.
Devuelve `void`.

---

### **ft_putstr_fd**

```c
void ft_putstr_fd(char *s, int fd)
```
Escribe la cadena `s` en el file descriptor `fd`.
Devuelve `void`.

---

### **ft_putendl_fd**

```c
void ft_putendl_fd(char *s, int fd)
```
Escribe la cadena `s` seguida de un salto de línea en el file descriptor `fd`.
Devuelve `void`.

---

### **ft_putnbr_fd**

```c
void ft_putnbr_fd(int n, int fd)
```
Escribe el entero `n` en el file descriptor `fd`.
Devuelve `void`.

---

## Cómo Compilar y Usar

### Compilar la biblioteca

```bash
make
```

Genera el archivo `libft.a` en el directorio raíz.

### Eliminar archivos objeto

```bash
make clean
```

### Eliminar todo (objetos + biblioteca)

```bash
make fclean
```

### Recompilar desde cero

```bash
make re
```

### Usar en tu proyecto

Copia `libft.a` y `lib/libft.h` al directorio de tu proyecto, incluye el header:

```c
#include "libft.h"
```

Y compila enlazando la biblioteca:

```bash
cc -Wall -Wextra -Werror main.c -L. -lft -o programa
```

---

*Proyecto desarrollado en [42 Barcelona](https://www.42barcelona.com/)*
