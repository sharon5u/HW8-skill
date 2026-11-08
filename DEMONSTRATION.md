# Demonstration

## Run 1 (level 1)
I started by testing the skill using easier code, such as "nth prime" from 15-112.
- After sending the request, CodeX returns: I’ll use the plain-English explanation skill. 
- Using the skill, CodeX returned a one sentence explanation of nth prime: nth_prime(n) finds and returns the nth prime number. A prime is a whole number greater than 1 divisible only by 1 and itself, such as 2, 3, 5, or 7.
- CodeX then gave a more detailed line by line explanation of the function. 

## Run 2 (level 2)
Then, I asked AI to retrive a more complex code project I wrote for 15-110 to test the MCP server. 
- After the request, CodeX returns: I’ll use the plain-English explanation skill again and look for hw6_protein_py in your workspace.
- CodeX then requested to use the MCP server tool to access my local files: "Allow the local-code-files MCP server to run tool "lookup_code"?"
- "Allow the local-code-files MCP server to run tool "lookup_code"?"
- Similar output was generated for this test with a one sentence explanation of code and then detailed high level description. 
- Checker caught many classified as "UNCLEAR". Such as : "dnaToRna has no docstring explaining that it returns three-character chunks starting at startIndex, includes the first stop chunk, and discards any incomplete trailing chunk." "synthesizeProteins combines sequence processing with console reporting at lines 128–130; callers requesting the returned proteins also receive printed output, blurring the boundary between computation and presentation." etc. 

I mostly agreed with what the checker reported interms of code functions but for some conceptual aspected specialized for the assignment, the checker was not able to grasp. 