# Libft

Reimplementação em C de funções essenciais da biblioteca padrão (`libc`), além de funções utilitárias adicionais. Projeto desenvolvido na **42 Barcelona** como base para os projetos futuros do currículo.

---

## Funções

## Checagem de Caracteres

### **ft_isalpha**

```c
int ft_isalpha(int c)
```
Verifica se o caractere é uma letra (a–z / A–Z).
Retorna `1` se verdadeiro, `0` se falso.

---

### **ft_isdigit**

```c
int ft_isdigit(int c)
```
Verifica se o caractere é um dígito (0–9).
Retorna `1` se verdadeiro, `0` se falso.

---

### **ft_isalnum**

```c
int ft_isalnum(int c)
```
Verifica se o caractere é alfanumérico (letra ou dígito).
Retorna `1` se verdadeiro, `0` se falso.

---

### **ft_isascii**

```c
int ft_isascii(int c)
```
Verifica se o valor está na tabela ASCII (0–127).
Retorna `1` se verdadeiro, `0` se falso.

---

### **ft_isprint**

```c
int ft_isprint(int c)
```
Verifica se o caractere é imprimível (32–126).
Retorna `1` se verdadeiro, `0` se falso.

---

## Conversão de Caracteres

### **ft_toupper**

```c
int ft_toupper(int c)
```
Converte uma letra minúscula em maiúscula.
Retorna o caractere convertido, ou o original caso não seja minúscula.

---

### **ft_tolower**

```c
int ft_tolower(int c)
```
Converte uma letra maiúscula em minúscula.
Retorna o caractere convertido, ou o original caso não seja maiúscula.

---

## Manipulação de Memória

### **ft_memset**

```c
void *ft_memset(void *s, int c, size_t n)
```
Preenche os primeiros `n` bytes da área de memória `s` com o valor `c`.
Retorna ponteiro para `s`.

---

### **ft_bzero**

```c
void ft_bzero(void *s, size_t n)
```
Zera os primeiros `n` bytes da área de memória apontada por `s`.
Retorna `void`.

---

### **ft_memcpy**

```c
void *ft_memcpy(void *dest, const void *src, size_t n)
```
Copia `n` bytes de `src` para `dest`. As áreas não devem se sobrepor.
Retorna ponteiro para `dest`.

---

### **ft_memmove**

```c
void *ft_memmove(void *dest, const void *src, size_t n)
```
Copia `n` bytes de `src` para `dest`, tratando corretamente regiões sobrepostas.
Retorna ponteiro para `dest`.

---

### **ft_memchr**

```c
void *ft_memchr(const void *s, int c, size_t n)
```
Busca a primeira ocorrência do byte `c` nos primeiros `n` bytes de `s`.
Retorna ponteiro para o byte encontrado, ou `NULL` se não encontrado.

---

### **ft_memcmp**

```c
int ft_memcmp(const void *s1, const void *s2, size_t n)
```
Compara os primeiros `n` bytes de duas áreas de memória.
Retorna a diferença entre o primeiro byte divergente; `0` se iguais.

---

### **ft_calloc**

```c
void *ft_calloc(size_t nmemb, size_t size)
```
Aloca memória para `nmemb` elementos de `size` bytes e inicializa tudo com zero.
Retorna ponteiro para a memória alocada, ou `NULL` em caso de erro.

---

## Manipulação de Strings

### **ft_strlen**

```c
size_t ft_strlen(const char *s)
```
Calcula o comprimento da string, sem contar o caractere nulo `\0`.
Retorna o número de caracteres da string.

---

### **ft_strlcpy**

```c
size_t ft_strlcpy(char *dst, const char *src, size_t dsize)
```
Copia `src` para `dst` com no máximo `dsize` bytes, garantindo terminação com `\0`.
Retorna o tamanho de `src`.

---

### **ft_strlcat**

```c
size_t ft_strlcat(char *dst, const char *src, size_t dsize)
```
Concatena `src` ao final de `dst`, respeitando o limite total de `dsize` bytes.
Retorna o tamanho total que a string teria se não houvesse limite.

---

### **ft_strchr**

```c
char *ft_strchr(const char *s, int c)
```
Busca a primeira ocorrência do caractere `c` na string `s`.
Retorna ponteiro para o caractere encontrado, ou `NULL` se não encontrado.

---

### **ft_strrchr**

```c
char *ft_strrchr(const char *s, int c)
```
Busca a última ocorrência do caractere `c` na string `s`.
Retorna ponteiro para o caractere encontrado, ou `NULL` se não encontrado.

---

### **ft_strncmp**

```c
int ft_strncmp(const char *s1, const char *s2, size_t n)
```
Compara os primeiros `n` caracteres de duas strings.
Retorna a diferença entre o primeiro caractere divergente; `0` se iguais.

---

### **ft_strnstr**

```c
char *ft_strnstr(const char *big, const char *little, size_t len)
```
Busca a string `little` dentro de `big`, limitando a busca aos primeiros `len` caracteres.
Retorna ponteiro para o início de `little` em `big`, ou `NULL` se não encontrado.

---

### **ft_strdup**

```c
char *ft_strdup(const char *s)
```
Cria uma cópia da string `s` alocando nova memória com `malloc`.
Retorna ponteiro para a nova string, ou `NULL` em caso de erro.

---

## Conversão de Tipos

### **ft_atoi**

```c
int ft_atoi(const char *nptr)
```
Converte uma string para inteiro, ignorando espaços iniciais e respeitando sinal.
Retorna o valor inteiro convertido.

---

### **ft_itoa**

```c
char *ft_itoa(int n)
```
Converte um inteiro para string, alocando memória para o resultado.
Retorna ponteiro para a string gerada, ou `NULL` em caso de erro.

---

## Funções Adicionais de String

### **ft_substr**

```c
char *ft_substr(char const *s, unsigned int start, size_t len)
```
Extrai uma substring de `s` a partir do índice `start` com comprimento máximo `len`.
Retorna ponteiro para a nova string, ou `NULL` em caso de erro.

---

### **ft_strjoin**

```c
char *ft_strjoin(char const *s1, char const *s2)
```
Concatena `s1` e `s2` em uma nova string alocada.
Retorna ponteiro para a nova string, ou `NULL` em caso de erro.

---

### **ft_strtrim**

```c
char *ft_strtrim(char const *s1, char const *set)
```
Remove todos os caracteres presentes em `set` do início e do fim de `s1`.
Retorna ponteiro para a string resultante, ou `NULL` em caso de erro.

---

### **ft_split**

```c
char **ft_split(char const *s, char c)
```
Divide a string `s` usando o caractere `c` como delimitador.
Retorna array de strings terminado em `NULL`, ou `NULL` em caso de erro.

---

### **ft_strmapi**

```c
char *ft_strmapi(char const *s, char (*f)(unsigned int, char))
```
Cria uma nova string aplicando a função `f` a cada caractere de `s`, passando o índice.
Retorna ponteiro para a nova string, ou `NULL` em caso de erro.

---

### **ft_striteri**

```c
void ft_striteri(char *s, void (*f)(unsigned int, char*))
```
Aplica a função `f` a cada caractere de `s` modificando-o diretamente (in-place), passando o índice.
Retorna `void`.

---

## Saída em File Descriptor

### **ft_putchar_fd**

```c
void ft_putchar_fd(char c, int fd)
```
Escreve o caractere `c` no file descriptor `fd`.
Retorna `void`.

---

### **ft_putstr_fd**

```c
void ft_putstr_fd(char *s, int fd)
```
Escreve a string `s` no file descriptor `fd`.
Retorna `void`.

---

### **ft_putendl_fd**

```c
void ft_putendl_fd(char *s, int fd)
```
Escreve a string `s` seguida de uma quebra de linha no file descriptor `fd`.
Retorna `void`.

---

### **ft_putnbr_fd**

```c
void ft_putnbr_fd(int n, int fd)
```
Escreve o inteiro `n` no file descriptor `fd`.
Retorna `void`.

---

## Como compilar e usar

### Compilar a biblioteca

```bash
make
```

Gera o arquivo `libft.a` no diretório raiz.

### Limpar arquivos objeto

```bash
make clean
```

### Remover tudo (objetos + biblioteca)

```bash
make fclean
```

### Recompilar do zero

```bash
make re
```

### Usar em seu projeto

Copie `libft.a` e `lib/libft.h` para o diretório do seu projeto, inclua o header:

```c
#include "libft.h"
```

E compile linkando a biblioteca:

```bash
cc -Wall -Wextra -Werror main.c -L. -lft -o programa
```

---

*Projeto desenvolvido por [gabde-so](https://profile-v3.intra.42.fr/users/gabde-so) na [42 Barcelona](https://www.42barcelona.com/)*
