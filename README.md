# libft
Personal C Library

### Functions:

| Function Name | Prototype     | Utility  |
| ------------- |---------------| -------- |
| ft_memset     | void \*ft_memset(void \*b, int c, size_t len)| man memset. |
| ft_bzero      | void ft_bzero(void \*s, size_t n)| man bzero |
| ft_memcpy     | void \*ft_memcpy(void \*dst, const void \*src, size_t n) | man memcpy|
| ft_memccpy    | void \*ft_memccpy(void \*dst, const void \*src, int c, size_t n)| man memccpy |
| ft_memmove    | void \*ft_memmove(void \*dst, const void \*src, size_t len)| man memmove |
| ft_memchr     | void \*ft_memchr(const void \*s, int c, size_t n)| man memchr |
| ft_memcmp     | int ft_memcmp(const void \*s1, const void \*s2, size_t n) | man memcmp |
| ft_strlen     | size_t ft_strlen(const char \*s) | man strlen |
| ft_strdup     | char \*ft_strdup(const char \*s1) | man strdup |
| ft_strcpy     | char \*ft_strcpy(char \*dst, const char \*src) | man strcpy |
| ft_strncpy    | char \*ft_strncpy(char \*dst, const char \*src, size_t len) | man strncpy |
| ft_strcat     | char \*ft_strcat(char \*s1, const char \*s2) | man strcat |
| ft_strncat    | char \*ft_strncat(char \*s1, const char \*s2, size_t n) | man strncat |
| ft_strlcat    | size_t ft_strlcat(char \*dst, const char \*src, size_t size)| man strlcat |
| ft_strchr     | char \*ft_strchr(const char \*s, int c) | man strchr |
| ft_strrchr    | char \*ft_strrchr(const char \*s, int c) | man strrchar |
| ft_strstr     | char \*ft_strstr(const char \*big, const char \*little) | man strstr |
| ft_strnstr    | char \*ft_strnstr(const char \*big, const char \*little, size_t len) | man strnstr |
| ft_strcmp     | int ft_strcmp(const char \*s1, const char \*s2) | man strcmp |
| ft_strncmp    | int ft_strncmp(const char \*s1, const char \*s2, size_t n) | man strncmp |
| ft_atoi       | int ft_atoi(const char \*str) | man atoi |
| ft_isalpha    | int ft_isalpha(int c) | man isalpha |
| ft_isdigit    | int ft_isdigit(int c) | man isdigit |
| ft_isalnum    | int ft_isalnum(int c) | man isalnum |
| ft_isascii    | int ft_isascii(int c) | man isascii |
| ft_isprint    | int ft_isprint(int c) | man isprint |
| ft_toupper    | int ft_toupper(int c) | man toupper |
| ft_tolower    | int ft_tolower(int c) | man tolower |

### Additional Functions

| Function Name | Prototype     | Utility  |
| ------------- |---------------| ---------|
| ft_memalloc   | void \*ft_memalloc(size_t size) | Replicates malloc + bzero |
| ft_memdel     | void ft_memdel(void \*\*ap)     | Frees memory and puts the pointer to NULL |
| ft_strnew     | char \*ft_strnew(size_t size)   | Returns a 'fresh' null-terminated string with zeroed characters|
| ft_strdel     | void ft_strdel(char \*\*as)     | ft_memdel() variant for strings|
| ft_strclr     | void ft_strclr(char \*s)        | Sets every character of the string to the value ’\0’|
| ft_striter    | void ft_striter(char \*s, void (\*f)(char \*)) | Applies f() to each character in as string|
| ft_striteri   | void ft_striteri(char \*s, void (\*f)(unsigned int, char \*)) |ft_striter() variant|
| ft_strmap     | char \*ft_strmap(char const \*s, char (\*f)(char)) |Applies f() to each character of a new string|
| ft_strmapi    | char \*ft_strmapi(char const \*s, char (\*f)(unsigned int, char)) |ft_strmap() variant|
| ft_strequ     | int ft_strequ(char const \*s1, char const \*s2) |Lexicographical comparison between 2 strings|
| ft_strnequ    | int ft_strnequ(char const \*s1, char const \*s2, size_t n) |ft_strequ() up to 'n' characters|
| ft_strsub     | char \*ft_strsub(char const \*s, unsigned int start, size_t len) |Returns a 'fresh' sub-string|
| ft_strjoin    | char \*ft_strjoin(char const \*s1, char const \*s2) |Returns a 'fresh' concatenated string|
| ft_strtrim    | char \*ft_strtrim(char const \*s) |Returns a 'fresh' string without whitespaces at the beginning and at the end|
| ft_strsplit   | char \*\*ft_strsplit(char const \*s, char c) |Returns a 'fresh' array of strings, made from the split of a string|
| ft_itoa       | char \*ft_itoa(int n) |Returns a 'fresh' string that represents an int value|
| ft_putchar    | void ft_putchar(char c) |Writes a character to stdout| 
| ft_putstr     | void ft_putstr(char const \*s) |Writes a string to stdout|
| ft_putendl    | void ft_putendl(char const \*s) |Writes a string followed by a newline to stdout|
| ft_putnbr     | void ft_putnbr(int n) |Writes an int to the stdout|
| ft_putchar_fd | void ft_putchar_fd(char c, int fd) |Writes an int to the file descriptor|
| ft_putstr_fd  | void ft_putstr_fd(char const \*s, int fd) |Writes a string to the file descriptor |
| ft_putendl_fd | void ft_putendl_fd(char const \*s, int fd) |Writes a string followed by a newline to the file descriptor|
| ft_putnbr_fd  | void ft_putnbr_fd(int n, int fd) |Writes a character to the file descriptor|


### Bonus Functions

The following functions are for list manipulation. To use them properly, you must use the following structure to represent linked lists:

```C
typedef struct  s_list
{
  void          *content;           /* Data contained in the link (of any type) */
  size_t        content_size;       /* The size of the data stored */
  struct s_list *next;              /* Next link address or NULL */
}               t_list;
```

| Function Name | Prototype     | Utility  |
| ------------- |---------------| ---------|
| ft_lstnew     | t_list \*ft_lstnew(void const \*content, size_t content_size) |Returns a 'fresh' link|
| ft_lstdelone  | void ft_lstdelone(t_list \*\*alst, void (\*del)(void \*, size_t)) |Frees 1 link and sets its pointer to NULL|
| ft_lstdel     | void ft_lstdel(t_list \*\*alst, void (\*del)(void \*, size_t)) |Frees 1 link and every successor of it|
| ft_lstadd     | void ft_lstadd(t_list \*\*alst, t_list \*new) |Adds the element 'new' to the beginning of the list|
| ft_lstiter    | void ft_lstiter(t_list \*lst, void (\*f)(t_list \*elem)) |Iterates a list and applies f() to each node|
| ft_lstmap     | t_list \*ft_lstmap(t_list \*lst, t_list \*(\*f)(t_list \*elem)) |Iterates a list and applies f() to each node to create a new list|

### Extra functions
The structure for the Binary Search Trees is shown below. 

```C
typedef struct      s_btree
{
  int               item;        /* Key/Value */
  struct s_btree    *left;       /* Left Child */
  struct s_btree    *right;      /* Right Child */
}                   t_btree;
```
| Function Name | Prototype     | Utility  |
| ------------- |---------------| ---------|
| ft_strsplitlist | t_list  \*ft_strsplitlist(char \*str, char delim) | Split strings and returns as a linkedlist|
| ft_lstappend | void	  ft_lstappend(t_list \*\*alst, t_list \*nw) | appends a new linked list node to the last node |
| btree_create_node | t_btree		\*btree_create_node(int item) | Creates a BST node
| btree_add_node | void   btree_add_node(t_btree \*\*root, t_btree \*node) | Create a BST node by node |
| btree_apply_inorder | btree_apply_inorder(t_btree \*root, void (\*applyf)(int)) | Inorder traversal of BST|
| btree_apply_postorder | btree_apply_postorder(t_btree \*root, void (\*applyf)(int)) | Postorder traversal of BST|
| btree_apply_preorder | tree_apply_preorder(t_btree \*root, void (\*applyf)(int)) | Preorder traversal of BST |

### MD Credit: Matt Hurd
