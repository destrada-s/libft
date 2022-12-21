# libft

**1. check for alpha**
<br>
int		ft_isalpha(int c);

**2. check for digits**
<br>
int		ft_isdigit(int c);

**3. check for alphanumeric**
<br>
int		ft_isalnum(int c);

**4. check for 7 bit ascii(0 - 127) not extended**
<br>
int		ft_isascii(int c);

**5. check for printable chars**
<br>
int		ft_isprint(int c);

**6. function computes the length of the string s**
<br>
size_t	ft_strlen(const char *s);

**7. writes len bytes of value c(unsigned char) to string b**
<br>
void	*ft_memset(void *b, int c, size_t len);

**8. bzeero writes in string 's' 'n' zeroed bytes**
<br>
void	ft_bzero(void *s, size_t n);

**9. copies n bytes from memory area(src) to memory area(dst)
If theres overlapping behaviour is undefined**
<br>
void	*ft_memcpy(void *dst, const void *src, size_t n);

/*copies n bytes from memory area(src) to memory area(dst)*/
/*Used when there can be overlapping*/
void	*ft_memmove(void *dst, const void *src, size_t len);
<br>
/* copy string src to dst making sure room in dst */
size_t	ft_strlcpy(char *dst, const char *src, size_t dstsize);

/* concatenate string src to dst making sure room in dst */
size_t	ft_strlcat(char *dst, const char *src, size_t dstsize);
<br>
/* letter to uppper case */
int		ft_toupper(int c);

/* letter to lower case */
int		ft_tolower(int c);
<br>
/* locate char in string */
char	*ft_strchr(const char *s, int c);

/* locate char in string from back to beginning */
char	*ft_strrchr(const char *s, int c);
<br>
/* function compares not more than n characters. */
int		ft_strncmp(const char *s1, const char *s2, size_t n);

/* The memchr() function locates the first occurrence of c 
(converted to an unsigned char)in string s. */
void	*ft_memchr(const void *s, int c, size_t n);
<br>
/* function compares byte string s1 against byte string s2. */
int		ft_memcmp(const void *s1, const void *s2, size_t n);

/* strnstr() function locates the first occurrence of the
null-terminated string needle in the string haystack, 
where not more than len characters are searched.
Characters that appear after a '\0' character are not searched. */
char	*ft_strnstr(const char *haystack, const char *needle, size_t len);
<br>
/* The atoi() function converts the initial portion of the string pointed to
 by str to int representation. */
int		ft_atoi(const char *str);

/* calloc allocates memory and assigns bytes with value zero->returns a pointe*/
void	*ft_calloc(size_t count, size_t size);
<br>
/* allocates sufficient memory for a copy of the string s1, does the copy, and
returns a pointer to it. */
char	*ft_strdup(const char *s1);

/*reserva con malloc, devuelve una substring de la string ’s’.
La substring empieza desde el índice ’start’ y
tiene una longitud máxima ’len’.*/
char	*ft_substr(char const *s, unsigned int start, size_t len);
<br>
/* Reserva malloc y devuelve una nueva
string, formada por la concatenación de ’s1’ y ’s2’.*/
char	*ft_strjoin(char const *s1, char const *s2);

/* Elimina todos los caracteres de la string ’set’
desde el principio y desde el final de ’s1’, hasta
encontrar un caracter no perteneciente a ’set devuelve resultado 
con malloc */
char	*ft_strtrim(char const *s1, char const *set);
<br>
/*Reserva con malloc un array de strings
resultante de separar la string ’s’ en substrings
utilizando el caracter ’c’ como delimitador */
char** ft_split(char const *s, char c);

/* Utilizando malloc, genera una string que
represente el valor integer recibido */
char	*ft_itoa(int n);
<br>
/* A cada carácter de la string ’s’, aplica la
función ’f’ dando como parámetros el índice de cada
carácter dentro de ’s’ y el propio carácter. Genera
una nueva string con el resultado del uso sucesivo
de ’f’ */
char	*ft_strmapi(char const *s, char (*f)(unsigned int, char));

/* a cada caracter de string s aplica la función
’f’ dando como parámetros el índice de cada
carácter dentro de ’s’ y la dirección del propio
carácter, que podrá modificarse si es necesario. */
void	ft_striteri(char *s, void (*f)(unsigned int, char*));
<br>
/* Envía el carácter ’c’ al file descriptor especificado. */
void	ft_putchar_fd(char c, int fd);

/*Envía la string ’s’ al file descriptor especificado */
void	ft_putstr_fd(char *s, int fd);
<br>
/* Envía la string ’s’ al file descriptor dado, seguido de un salto de línea.*/
void	ft_putendl_fd(char *s, int fd);

/* Envía el número ’n’ al file descriptor dado. */
void	ft_putnbr_fd(int n, int fd);
<br>
/*crear nodo nuevo para la lista */
t_list	*ft_lstnew(void *content);

/* conectas el nodo new a la lista lst al prinicipio*/
void	ft_lstadd_front(t_list** lst, t_list *new);
<br>
/* Cuenta el número de nodos de una lista.*/
int		ft_lstsize(t_list *lst);
/* Devuelve el último nodo de la lista. */
t_list	*ft_lstlast(t_list *lst);

/* Añade el nodo ’new’ al final de la lista ’lst’ */
void	ft_lstadd_back(t_list** lst, t_list *new);
<br>
/* elimina un nodo con free */
void	ft_lstdelone(t_list *lst, void (*del)(void *));

/* elimina un la lista y todos los nodo con free */
void	ft_lstclear(t_list** lst, void (*del)(void *));
<br>
/* Itera la lista ’lst’ y aplica la función ’f’ en el contenido de cada nodo.*/
void	ft_lstiter(t_list *lst, void (*f)(void *));

/*  Crea una lista resultante de la aplicación correcta y sucesiva de la 
función ’f’ sobre cada nodo.*/
t_list	*ft_lstmap(t_list *lst, void *(*f)(void *), void (*del)(void *));
