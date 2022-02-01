---
title: "Custom Dropper"
date: 2022-01-12T13:20:47-05:00
draft: false
---
## Writing Custom Malware For Red Teams

Why should you write your own custom malware? Threat Hunters and AV engines are becoming more advanced and proficient at identifying and removing malware. Additionally, using malware templates written by some unkonwn person can __actually__ compromise your client.

## PE Format

Portable Executable Format is simply a way that an executable's code is organized on the disk so that the Windows OS Loader can read it,load it into memory as a process, and execute it.

![PE Format](https://upload.wikimedia.org/wikipedia/commons/thumb/1/1b/Portable_Executable_32_bit_Structure_in_SVG_fixed.svg/1024px-Portable_Executable_32_bit_Structure_in_SVG_fixed.svg.png)

## What Does a Basic PE Look Like?

Well, if you've ever written in C, it's just a basic program!

```C
#include <windows.h>
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main(void) {
	printf("I am a basic PE!\n");
	
	getchar();

	return 0;
}
```
## Function Call Obfuscation

Suspicious shopping list analogy
