# Lab Report 2 Bugfixes!

## Bugfix 1: Image vs Link
**Code Change:**
![](https://user-images.githubusercontent.com/103162560/165028539-6f8a028b-ca7e-49e8-ac90-148a9a177e05.jpg)

**File:**
[Image vs Link File](https://github.com/jwbarkes/markdown-parser/blob/main/test-file3.md)

**Symptom Output:**
![](https://user-images.githubusercontent.com/103162560/165030440-3aabe5bc-2ca9-4b5d-a138-32c32a1e3fcf.jpg)


In markdown, the difference between a link and a photo is a simple "!" at before the brackets. The bug would overlook the "!" and the code would see an image and link as the same. The symptom would be that the link for the image would also be returned.
___
## Bugfix 2: Infinite Loop
**Code Change:**
![](https://user-images.githubusercontent.com/103162560/165028582-56d59168-f6d7-4671-ba6d-41d10f3ca5f6.jpg)

**File:**
[Infinite Loop File](https://github.com/jwbarkes/markdown-parser/blob/main/test-file2.md)

**Symptom Output:**
![](https://user-images.githubusercontent.com/103162560/165030476-2cdc1909-8b35-432d-a7be-2ac33595b568.jpg)

When the code begins to look for the paranthesis and brackets to find the link, if there was no open bracket the code would be stuck in an infinite loop. Test 6 which featured simply a `)[` would cause this bug to occur. The symptom would be the infinite loop occuring.
___
## Bugfix 3: Multiple Paranthesis
**Code Change:**
![](https://user-images.githubusercontent.com/103162560/165028608-a1239f7b-b3ae-42d9-bfb5-e7b003d3914c.jpg)

**File:**
[Multiple Paranthesis File](https://github.com/jwbarkes/markdown-parser/blob/main/test-file6.md)

**Symptom Output:**
![Multiple ) outputJPG](https://user-images.githubusercontent.com/103162560/165030523-bb67204b-3470-4253-92df-68c7e54744bb.jpg)

The original code would just find the first instance of each of the paranthesis and brackets. A bug occurred in test file 2 which featured a link in a link: 
`[a test] mean ([link1](https://something.com))`
The symptom would then be the entirety of "link 1", including the brackets, paranthesis, and link title, being returned rather than just the link itself.
___
