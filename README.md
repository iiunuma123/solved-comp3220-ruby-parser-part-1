Download Link: https://assignmentchef.com/product/solved-comp3220-ruby-parser-part-1
<br>
For this assignment, we will be writing a parser that is able to parse an input file written in our “<strong>Tiny</strong>” grammar. You should finish writing the “<strong>Parser</strong>” class that I’ve provided. Your Parser class should print:

<ul>

 <li>Each time it enters or leaves a rule and what the rule is</li>

 <li>Each time it recognizes a token and what the token was</li>

 <li>Something, everytime it catches an error</li>

 <li>Whether or not the parse completed successfully (no errors) and how many errors were found</li>

</ul>

<strong>Parser.rb</strong> extends <strong>Scanner.rb </strong>(The lexer that you wrote for your last assignment) and provides a framework for a top-down, recursive-descent parser of the <strong>TINY</strong> language. The parser stays one token ahead in the Token stream <strong>(@lookahead</strong>) and uses the Token to predict how to continue parsing the current instruction and which method to call next.

The <strong>consume()</strong> method calls <strong>nextToken()</strong> in the scanner. The current <strong>@lookahead</strong> Token is discarded, and the next Token in the stream is retrieved. Whitespace Tokens are discarded.

The <strong>match(dtype)</strong> method tries to match the <strong>@lookahead</strong> Token with the provided type (<strong>dtype</strong>). If a match is found, <strong>consume()</strong> is called to retrieve the next Token. Otherwise an error is raised.

The <strong>program()</strong> method is first called to parse a <strong>TINY</strong> program. Since a <strong>TINY</strong> program consists of a sequence of statements, <strong>program()</strong> calls <strong>statement()</strong> repeatedly until it encounters the <strong>EOF</strong> token.

Complete the parser by providing methods for the appropriate BNF rules in <strong>TINY</strong>.

I have given you my <strong>lexer</strong> and <strong>token</strong> ruby classes. I have also partially written the <strong>parser</strong> for you and have written a <strong>main.rb</strong> file that can run your ruby parser.

I have also included 5 sample input files that you can use to test your program once you’ve finished writing it.

<strong>input[1-3].txt</strong> should complete with no parse errors.

<strong>input[4-5].txt</strong> should have parse errors.

Below are screenshots of what your output should look like, based on the input files I’ve provided.

<h2>Deliverables</h2>

Submit ONLY your <strong>Parser.rb</strong> file.







input3.txt







<strong>input4.txt</strong>

<strong>input5.txt</strong>


