<div id="header" align="center">
  <img src="https://media.giphy.com/media/ztl9x7JlhSlU4MWD6h/giphy.gif" width="200"/>
</div>

<h1 align="center">libft</h1>

**1. int		ft_isalpha(int c);** 
<br>
- check for alpha


**2. int		ft_isdigit(int c);**
<br>
- check for digits

**3. int		ft_isalnum(int c);**
<br>
- check for alphanumeric


**4. int		ft_isascii(int c);**
<br>
- check for 7 bit ascii(0 - 127) not extended


**5. int		ft_isprint(int c);**
<br>
- check for printable chars


**6. size_t	ft_strlen(const char *s);**
<br>
- function computes the length of the string


**7. void	*ft_memset(void *b, int c, size_t len);**
<br>
- writes len bytes of value c(unsigned char) to string b


**8. void	ft_bzero(void *s, size_t n);**
<br>
- bzeero writes in string 's' 'n' zeroed bytes


**9. void	*ft_memcpy(void *dst, const void *src, size_t n);**
<br>
- copies n bytes from memory area(src) to memory area(dst)
If theres overlapping behaviour is undefined

**10. void	*ft_memmove(void *dst, const void *src, size_t len);**
<br>
- copies n bytes from memory area(src) to memory area(dst)
Used when there can be overlapping

**11. size_t	ft_strlcpy(char *dst, const char *src, size_t dstsize);**
- copy string src to dst making sure room in dst */


**11. size_t	ft_strlcat(char *dst, const char *src, size_t dstsize);**
- concatenate string src to dst making sure room in dst

**12. int		ft_toupper(int c);**
- letter to uppper case


**11. **
/* letter to lower case */
int		ft_tolower(int c);
<br>
**11. **
/* locate char in string */
char	*ft_strchr(const char *s, int c);

**11. **
/* locate char in string from back to beginning */
char	*ft_strrchr(const char *s, int c);
<br>
**11. **
/* function compares not more than n characters. */
int		ft_strncmp(const char *s1, const char *s2, size_t n);

**11. **
/* The memchr() function locates the first occurrence of c 
(converted to an unsigned char)in string s. */
void	*ft_memchr(const void *s, int c, size_t n);
<br>

**11. **
/* function compares byte string s1 against byte string s2. */
int		ft_memcmp(const void *s1, const void *s2, size_t n);

**11. **
/* strnstr() function locates the first occurrence of the
null-terminated string needle in the string haystack, 
where not more than len characters are searched.
Characters that appear after a '\0' character are not searched. */
char	*ft_strnstr(const char *haystack, const char *needle, size_t len);
<br>

**11. **
/* The atoi() function converts the initial portion of the string pointed to
 by str to int representation. */
int		ft_atoi(const char *str);

**11. **
/* calloc allocates memory and assigns bytes with value zero->returns a pointe*/
void	*ft_calloc(size_t count, size_t size);
<br>
/* allocates sufficient memory for a copy of the string s1, does the copy, and
returns a pointer to it. */
char	*ft_strdup(const char *s1);

**11. **
/*reserva con malloc, devuelve una substring de la string ’s’.
La substring empieza desde el índice ’start’ y
tiene una longitud máxima ’len’.*/
char	*ft_substr(char const *s, unsigned int start, size_t len);
<br>

**11. **
/* Reserva malloc y devuelve una nueva
string, formada por la concatenación de ’s1’ y ’s2’.*/
char	*ft_strjoin(char const *s1, char const *s2);

**11. **
/* Elimina todos los caracteres de la string ’set’
desde el principio y desde el final de ’s1’, hasta
encontrar un caracter no perteneciente a ’set devuelve resultado 
con malloc */
char	*ft_strtrim(char const *s1, char const *set);
<br>

**11. **
/*Reserva con malloc un array de strings
resultante de separar la string ’s’ en substrings
utilizando el caracter ’c’ como delimitador */
char** ft_split(char const *s, char c);

**11. **
/* Utilizando malloc, genera una string que
represente el valor integer recibido */
char	*ft_itoa(int n);
<br>

**11. **
/* A cada carácter de la string ’s’, aplica la
función ’f’ dando como parámetros el índice de cada
carácter dentro de ’s’ y el propio carácter. Genera
una nueva string con el resultado del uso sucesivo
de ’f’ */
char	*ft_strmapi(char const *s, char (*f)(unsigned int, char));

**11. **
/* a cada caracter de string s aplica la función
’f’ dando como parámetros el índice de cada
carácter dentro de ’s’ y la dirección del propio
carácter, que podrá modificarse si es necesario. */
void	ft_striteri(char *s, void (*f)(unsigned int, char*));
<br>
**11. **
/* Envía el carácter ’c’ al file descriptor especificado. */
void	ft_putchar_fd(char c, int fd);

**11. **
/*Envía la string ’s’ al file descriptor especificado */
void	ft_putstr_fd(char *s, int fd);
<br>
**11. **
/* Envía la string ’s’ al file descriptor dado, seguido de un salto de línea.*/
void	ft_putendl_fd(char *s, int fd);

**11. **
/* Envía el número ’n’ al file descriptor dado. */
void	ft_putnbr_fd(int n, int fd);
<br>
**11. **
/*crear nodo nuevo para la lista */
t_list	*ft_lstnew(void *content);

**11. **
/* conectas el nodo new a la lista lst al prinicipio*/
void	ft_lstadd_front(t_list** lst, t_list *new);
<br>
**11. **
/* Cuenta el número de nodos de una lista.*/
int		ft_lstsize(t_list *lst);

**11. **
/* Devuelve el último nodo de la lista. */
t_list	*ft_lstlast(t_list *lst);

**11. **
/* Añade el nodo ’new’ al final de la lista ’lst’ */
void	ft_lstadd_back(t_list** lst, t_list *new);
<br>

**11. **
/* elimina un nodo con free */
void	ft_lstdelone(t_list *lst, void (*del)(void *));

**11. **
/* elimina un la lista y todos los nodo con free */
void	ft_lstclear(t_list** lst, void (*del)(void *));
<br>

**11. **
/* Itera la lista ’lst’ y aplica la función ’f’ en el contenido de cada nodo.*/
void	ft_lstiter(t_list *lst, void (*f)(void *));

**11. **
/*  Crea una lista resultante de la aplicación correcta y sucesiva de la 
función ’f’ sobre cada nodo.*/
t_list	*ft_lstmap(t_list *lst, void *(*f)(void *), void (*del)(void *));
