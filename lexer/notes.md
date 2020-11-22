Source Code -> Tokens -> Abstract Syntax Tree

Transformation of source code into tokens is called “lexical analysis” or “lexing” and it is done by lexer. These tokens are then fed into parser which then does second transformation into an “Abstract Syntax Tree”.

Example of lexing process,
`let x = 5 + 5;`

And what comes out of the lexer looks kinda like this:
`[
    LET,
    IDENTIFIER("x"),
    EQUAL_SIGN,
    INTEGER(5),
    PLUS_SIGN,
    INTEGER(5),
    SEMICOLON
]`

All these token outputs are defined in the token/token.go file. Lexer takes the source code as the input and 
returns the tokens as its output. It has only one function called `NextToken()` which calls itself iteratively and returns the next token. Example can be found inside lexer/lexer_test.go file.



