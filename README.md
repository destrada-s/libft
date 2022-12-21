<div id="header" align="center">
  <img src="https://media.giphy.com/media/ztl9x7JlhSlU4MWD6h/giphy.gif" width="200"/>
</div>

<h1 align="center">libft</h1>

<p> El proyecto libft, el primer proyecto del cursus 42, te quiere familiarizar con la programacion en C y asentar los conceptos que aprendiste en la piscina, recreando funciones de la standard library de C entre otras librerias como string.h</p>
<p> Ademas se crea una libreria.a y se aprende a utilizar el makefile para compilar muchos archivos</p>
<p> Esta libreria ira creciendo junto a tu progreso en 42, ya que, la idea es que la utilizemos para guardarnnos funciones de utilidad 👾 </p> 

## Conceptos Aprendidos
- Entender funcionamiento de las funciones basicas
- Soltura con C
- Makefile
- file.h
- lib.a

## Useful Resources
1. [recreate lib](https://www.asidesigned.com/project-libft.html)
2. [IBM Doc](https://www.ibm.com/docs/en)
3. [GeekforGeeks](https://www.geeksforgeeks.org/)

<h2 align="center">Funciones libft</h2>

<b> 1. int		ft_isalpha(int c);</b>
<br>
- check for alpha

<b>2. int		ft_isdigit(int c);</b>
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

<b>6. size_t	ft_strlen(const char *s);</b>
<br>
- function computes the length of the string

<b>7. void	*ft_memset(void *b, int c, size_t len);</b>
<br>
- writes len bytes of value c(unsigned char) to string b

<b>8. void	ft_bzero(void *s, size_t n);</b>
<br>
- bzeero writes in string 's' 'n' zeroed bytes

<b>9. void	*ft_memcpy(void *dst, const void *src, size_t n);</b>
<br>
- copies n bytes from memory area(src) to memory area(dst)
If theres overlapping behaviour is undefined

<b>10. void	*ft_memmove(void *dst, const void *src, size_t len);</b>
<br>
- copies n bytes from memory area(src) to memory area(dst)
Used when there can be overlapping

<b>11. size_t	ft_strlcpy(char *dst, const char *src, size_t dstsize);</b>
<br>
- copy string src to dst making sure room in dst

<b>12. size_t	ft_strlcat(char *dst, const char *src, size_t dstsize);</b>
<br>
- concatenate string src to dst making sure room in dst

<b>13. int		ft_toupper(int c);</b>
<br>
- letter to uppper case

<b>14. int		ft_tolower(int c);</b>
<br>
- letter to lower case

<b>15. char	*ft_strchr(const char *s, int c);</b>
<br>
- locate char in string 

<b>16. char	*ft_strrchr(const char *s, int c);</b>
<br>
- locate char in string from back to beginning

<b>17. int		ft_strncmp(const char *s1, const char *s2, size_t n);</b>
<br>
- function compares not more than n characters.


<b>18. void	*ft_memchr(const void *s, int c, size_t n);</b>
<br>
- The memchr() function locates the first occurrence of c 
(converted to an unsigned char)in string s.



<b>19. int		ft_memcmp(const void *s1, const void *s2, size_t n);</b>
<br>
- function compares byte string s1 against byte string s2.

<b>20. char	*ft_strnstr(const char *haystack, const char *needle, size_t len);</b>
<br>
- strnstr() function locates the first occurrence of the null-terminated string needle in the string haystack, where not more than len characters are searched. Characters that appear after a '\0' character are not searched.


<b>21. int		ft_atoi(const char *str);</b>
<br>
- The atoi() function converts the initial portion of the string pointed to
 by str to int representation.


<b>22. void	*ft_calloc(size_t count, size_t size);</b>
<br>
- calloc allocates memory and assigns bytes with value zero->returns a pointer


<b>23. char	*ft_strdup(const char *s1);</b>
<br>
- allocates sufficient memory for a copy of the string s1, does the copy, and
returns a pointer to it.

<b>24. char	*ft_substr(char const *s, unsigned int start, size_t len);</b>
<br>
- reserva con malloc, devuelve una substring de la string ’s’.
La substring empieza desde el índice ’start’ y
tiene una longitud máxima ’len’.

<b>25. char	*ft_strjoin(char const *s1, char const *s2);</b>
<br>
- Reserva malloc y devuelve una nueva
string, formada por la concatenación de ’s1’ y ’s2’.

<b>26. char	*ft_strtrim(char const *s1, char const *set);</b>
<br>
- Elimina todos los caracteres de la string ’set’
desde el principio y desde el final de ’s1’, hasta
encontrar un caracter no perteneciente a ’set devuelve resultado 
con malloc

<b>27. char** ft_split(char const *s, char c);</b>
<br>
- Reserva con malloc un array de strings
resultante de separar la string ’s’ en substrings
utilizando el caracter ’c’ como delimitador

<b>28. char	*ft_itoa(int n);</b>
<br>
- Utilizando malloc, genera una string que
represente el valor integer recibido

<b>29. char	*ft_strmapi(char const *s, char (*f)(unsigned int, char));</b>
<br>
- A cada carácter de la string ’s’, aplica la
función ’f’ dando como parámetros el índice de cada
carácter dentro de ’s’ y el propio carácter. Genera
una nueva string con el resultado del uso sucesivo
de ’f’


<b>30. void	ft_striteri(char *s, void (*f)(unsigned int, char*));</b>
<br>
- a cada caracter de string s aplica la función
’f’ dando como parámetros el índice de cada
carácter dentro de ’s’ y la dirección del propio
carácter, que podrá modificarse si es necesario.

<b>31. void	ft_putchar_fd(char c, int fd);</b>
<br>
- Envía el carácter ’c’ al file descriptor especificado.

<b>32. void	ft_putstr_fd(char *s, int fd);</b>
<br>
- Envía la string ’s’ al file descriptor especificado

<b>33. void	ft_putendl_fd(char *s, int fd);</b>
<br>
- Envía la string ’s’ al file descriptor dado, seguido de un salto de línea.

<b>34. void	ft_putnbr_fd(int n, int fd);</b>
<br>
- Envía el número ’n’ al file descriptor dado.

<b>35. t_list	*ft_lstnew(void *content);</b>
<br>
- crear nodo nuevo para la lista

<b>36. void	ft_lstadd_front(t_list** lst, t_list *new);</b>
<br>
- conectas el nodo new a la lista lst al prinicipio


<b>37. int		ft_lstsize(t_list *lst);</b>
<br>
- Cuenta el número de nodos de una lista.


<b>38. t_list	*ft_lstlast(t_list *lst);</b>
<br>
- Devuelve el último nodo de la lista.

<b>39. void	ft_lstadd_back(t_list** lst, t_list *new);</b>
<br>
- Añade el nodo ’new’ al final de la lista ’lst’

<b>40. void	ft_lstdelone(t_list *lst, void (*del)(void *));</b>
<br>
- elimina un nodo con free


<b>41. void	ft_lstclear(t_list** lst, void (*del)(void *));</b>
<br>
- elimina un la lista y todos los nodo con free

<b>42. void	ft_lstiter(t_list *lst, void (*f)(void *));</b>
<br>
- Itera la lista ’lst’ y aplica la función ’f’ en el contenido de cada nodo.

<b>43. t_list	*ft_lstmap(t_list *lst, void *(*f)(void *), void (*del)(void *));</b>
<br>
- Crea una lista resultante de la aplicación correcta y sucesiva de la 
función ’f’ sobre cada nodo.
