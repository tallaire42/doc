# ERRNO

extern	`___errno_location`

retourn un pointeur en rax. Il dereferencer rax comme ceci [rax]
pour y mettre le bon code d'erreur.

`syscall
mov	rcx, rax
___errno_location
neg	rcx
mov	[rax], rcx`
