# Lab Report 4
## Links to Repositories:
[My Repository](https://github.com/Barakar13/markdown-parser)

[Other Group's Repository](https://github.com/gabrielseventhucsd25/markdown-parser)

## Test 1:
### Intended Outcome
1. `google.com
2. google.com
3. ucsd.edu

### MarkdownParseTest Code:
<img width="466" alt="Test 1 Code" src="https://user-images.githubusercontent.com/103162560/171090981-a0bc674e-730c-485e-9515-0712b57a7be4.png">


### My Results:
<img width="838" alt="My Test 1" src="https://user-images.githubusercontent.com/103162560/171091099-ae925223-6c7e-40da-b6af-8aad0229e0c0.png">


### Their Results:
<img width="616" alt="Their Test 1" src="https://user-images.githubusercontent.com/103162560/171091170-b0e74afe-232a-4282-8cf2-2c882a2e31d3.png">


### Potential Fixes:
> For my Markdown parser there does seem to be a simple fix. My code looks for the `](` combination but with if statements checking the line that this combo is on, my code can avoid the mistake of catching url.com. That fix will also hopefully catch the ucsd.edu if implemented correctly.
---
## Test 2:
### Intended Outcome
1. a.com
2. a.com(())
3. example.com

### MarkdownParseTest Code:
<img width="465" alt="Test 2 Code" src="https://user-images.githubusercontent.com/103162560/171091008-25ed09cc-e9d7-45ef-a421-434018b858b0.png">


### My Results:
<img width="681" alt="My Test 2" src="https://user-images.githubusercontent.com/103162560/171091118-b77e25d1-4c47-4b58-9853-4d2f8c101b60.png">


### Their Results:
<img width="598" alt="Their Test 2" src="https://user-images.githubusercontent.com/103162560/171091191-295c8a89-e580-4660-8471-c053548f54b1.png">


### Potential Fixes:
> While there does not seem to be a simple fix for catching example.com, the error with the return of a.com(()) can be fixed. This is fixed by editing the return by creating a counter of how many open paranthesis the program finds before finding the first closed paranthesis, and will skip over as many closed paranthesis as bonus open paranthesis are found.
---
## Test 3:
### Intended Outcome
1. https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule

### MarkdownParseTest Code:
<img width="615" alt="Test 3 Code" src="https://user-images.githubusercontent.com/103162560/171091028-bf3ab43b-9729-4d64-af25-42b2d6a567e6.png">


### My Results:


### Their Results:
<img width="846" alt="Their Test 3" src="https://user-images.githubusercontent.com/103162560/171091201-b5bebbf7-ef0a-43cf-b5c4-0b66bbe7648e.png">


### Potential Fixes:
> 
