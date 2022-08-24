---
title: "Hello World 부트로더"
excerpt: "Hello World를 출력하는 인텔 CPU 부트로더"
categories:
    - kernel
tags:
    - kernel
---

# 'A'를 출력하는 부트로더

```assembly
ORG 0x7c00
BITS 16

start:
	mov ah, 0eh
	mov al, 'A'
	mov bx, 0
	int 0x10

	jmp $

times 510-($ - $$) db 0
dw 0xAA55
```
