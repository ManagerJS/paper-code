# Fibonacci

A fascinating number sequence that finds applications in biology and art.

The challenges below use JavaScript, HTML, and CSS.

- You will solve a problem in JavaScript.
- You will use your JavaScript on a HTML page.
- You will apply very basic styling to the HTML page.

## JavaScript Problem Statement

There are exactly two rules for the fibonacci sequence:

1. The first two numbers are 1. That is: f1 = f2 = 1.

2. Aside from that, every subsequent number in the sequence is the sum of the previous 2. That is: for n > 2, f\_n = f\_(n-1) + f\_(n-2).

For example, the first few numbers of the sequence are 1, 1, 2, 3, 5, 8, 13. You can see that the first two numbers come from rule 1. All the other numbers come from rule 2.

Before going on, check your understanding of the problem by determining the next number in the sequence.

### Your Assignment

Write a function named `fib` that takes a number, `n`, and returns the nth number in the sequence. For example, if I called `fib` with the number `6` it should return the number `8`.

That is, fill in the missing code:

    function fib(n) {

      // MISSING CODE

    }

    fib(6); // returns 8

### Some Tips

- Use as many sheets of paper as you need to think clearly and keep your work readable.
- Put your name at the top of every sheet.
- Treat your interviewer as a team mate. Include them in thinking through the problem.

## Expanding Beyond JS: HTML and CSS

### Problem Statement:

Take the function `fib` you just wrote.

- Put it in its own file.
- Name the file and all files you create.

Complete the following HTML challenges:

- Include the file you just created with your function in it. Use it externally. That is, don't just paste it into the HTML.
- Write the markup for an HTML page that when viewed in the browser simply says, "The sixth fibonacci number is 8." 
- The page should load your reusable function and call it with the number 6 and put the result into the DOM in the proper place. That is, the "8" in the web page must be dynamically computed and added to the page.
- Keep your original JavaScript function (and the file that contains it) reusable. If you need to write "glue code" to get a value into the page then place it elsewhere.

Complete the following CSS challenge:

- Create a CSS file and link it to your page.
- Causes the "8" in the rendered sentence to be red. NOTE: It should _only_ style the "8" and not any other part of the sentence.

### Some Possibly Useful API Notes

You _may_ be able to use some of these APIs in the challenge.

    console.log('msg') // prints msg to the browser debug console

    domElement.innerHTML = 'msg' // Replaces the content of the tag
                                 // referred to by domElement with msg

    document.getElementById('x') // Returns the domElement for the tag
                                 // with the id 'x'

    Math.random() // Returns a floating point number on the half-open
                  // interval [0, 1)


