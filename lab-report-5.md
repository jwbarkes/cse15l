# Lab Report 5

## How I found my failed tests:
I found my failed tests by using vim diff on the results and manually scrolling through until I found them.

---
## Link to test 503:
[Test 503](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/503.md)

## Who's Correct:
Both implementations are incorrect for different reasons. My implementation fails due to returning multiple things when only one link is present, and the other implementation fails due to not returning anything.

## Expected Output from Commonmark:
<img width="1159" alt="Screen Shot 2022-06-03 at 6 53 37 PM" src="https://user-images.githubusercontent.com/103162560/171972093-4fbe180a-40c2-4f72-a798-8fae0a7d3d5c.png">

## Actual Outputs:
<img width="1289" alt="Screen Shot 2022-06-03 at 6 50 51 PM" src="https://user-images.githubusercontent.com/103162560/171972090-9babb56e-5033-4f98-910e-a08a4d2665a5.png">

## Whats Wrong with the Code:
The problem with my code comes from what is being added to the final arraylist that is being returned. This occurs within the getLinks method as that is where links are added to the arraylist. The problem seems to come from the quotation marks as each return statement features one less `'` then the previous.
<img width="615" alt="Screen Shot 2022-06-03 at 8 44 21 PM" src="https://user-images.githubusercontent.com/103162560/171981301-74b060a1-442b-44ab-8547-2eeac063710d.png">

---
## Link to test 486:
[Test 486](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/486.md)

## Who's Correct:
The provided implementation was correct as it did not return a link, but my implementation failed this test by returning what is in the paranthesis.

## Expected Output from Commonmark:
<img width="1163" alt="Screen Shot 2022-06-03 at 6 59 53 PM" src="https://user-images.githubusercontent.com/103162560/171972280-81a280cb-179d-4444-a91f-f52874839bce.png">

## Actual Outputs:
<img width="1308" alt="Screen Shot 2022-06-03 at 7 00 43 PM" src="https://user-images.githubusercontent.com/103162560/171972323-3189f508-991c-47e9-ad57-9d46535e2e40.png">

## Whats Wrong with the Code:
The bug results from the inclusion of `/` in the link as slashes represent file paths. Thus I believe that due to the file path not being properly set up in the link section, the entire link breaks and should result in no return. However, my markdown parser looks for `](` and returns everything up until the next closed paranthesis without caring for what is inside of those paranthesis.
<img width="448" alt="Screen Shot 2022-06-03 at 8 51 55 PM" src="https://user-images.githubusercontent.com/103162560/171981311-87b6ca0b-8775-4df5-bfcb-01cf5cee5317.png">
