# Part 1: Description of Overall Test Plan



# Part 2: Test Case Descriptions
## Web Scraper Tests (WS):
- WS1
    - Test that the web scraper is picking up all desired text from a webpage
    - Test web scraper on a sample webpage and compare with predetermined results
    - Input: pre-made sample webpage
    - Output: array containing all text from heading and paragraph HTML tags
    - Normal
    - Whitebox
    - Functional 
    - Unit test

## Statement Finder Tests (SF):
- SF1
    - Test that the statement finder tool is finding all desired statements from some text
    - Test statement finder by giving it an array of text and checking against an expected array of outputs
    - Input: array of text gathered from a webpage
    - Output: Array of all statements gathered from the text
    - Normal
    - Whitebox
    - Functional
    - Unit test
- SF2
    - Test that the statement finder tool is not finding opinions
    - Test that the statement finder tool is not including opinions in the output
    - Input: text array with opinion statements
    - Output: array of statements that doesn't include opinions
    - Boundary
    - Whitebox
    - Functional
    - Unit
- SF3
    - Test that the statement finder tool is not finding questions
    - Test that the statement finder tool is not including questions in the output
    - Input: text array with questions
    - Output: array of statements that doesn't include questions
    - Boundary
    - Whitebox
    - Functional
    - Unit


# Part 3: Test Case Matrix
| Name | Normal/Abnormal | Blackbox/Whitebox | Functional/Performance | Unit/Integration |
| --- | ---| --- | --- | --- |
| WS1 | Normal | Whitebox | Functional | Unit |
| SF1 | Normal | Whitebox | Functional | Unit |
| SF2 | Boundary | Whitebox | Functional | Unit |
| SF3 | Boundary | Whitebox | Functional | Unit |