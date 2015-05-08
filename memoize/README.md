# Memoization

**JavaScript and Algorithms**

Part 1 is a discussion. Part 2 gets to the code. You can skip straight to 2 when time is short. This problem is particularly useful for gauging JavaScript familiarity since it takes advantage of functions as objects and closures.

## Part 1 -- Analysis

**Note:** There's a lot of jargon in the question, but that's not the point of this challenge.  Make sure they understand the question. You might gauge how willing they are to ask questions, but only gently. Don't put them on the defensive just by the wording of the question.

**Question:** You have a number of expensive pure functions. During the course of any given hour these functions are each called with a small number of inputs.  Hour over hour the inputs vary dramatically. Describe how you could improve the performance of the system.

**Candidate behaviors to look for:** Caches the results and bypasses the expensive function calls when the answer is cached. Memoization.

### WEAK
- Ignores cache hit/miss analysis.
- Ignores the changing inputs.
- Attempts a static solution.
- Ignores memory leaks.
- Caches forever.

### STRONG
- Knows a pure function has no side-effects so the results can be cached.
- Plans to cache the results of the call.
- Empties or expires the cache reasonably to avoid memory issues.
- Addresses/bounds cache size.
- Multiple approaches and reasons for picking them.

### NOTES:

```


```

## Part 2 -- Implementation

**Notes:** Again, gauge the candidate as you read the question and be sure that they understand. You aren't testing their knowledge of jargon.

**Question:** Write a higher order function (a function that takes a function and returns a function) that accepts a function of arity 1 and returns an identical, memoized function.

Write up this template and have them fill it in.  Helps to use different colors between interviewer and candidate. If they struggle you might add elements to the solution and guide them to a solution.

```javascript
var expensive = function (x) { /* expensive code. e.g. translate id to static value from a database. */ };

function memoize(orig) {
  // --A-- Your code here






}

expensive = memoize(expensive);
expensive(1); // slow --B--
expensive(2); // slow
expensive(1); // fast
```

**Note:** You will find that some candidates will solve the problem handily, refactor, then easily run through the examples at **--B--**. Other candidates might have to be coached more through the implementation, but should at least be able to step through the execution at **--B--**.

**Candidate behaviors to look for:** readable code. Accounting for errors and initial condition. Careful programming.

### WEAK
- Ignores cache miss.
- Ignores error cases.

### STRONG
- Initial condition
- Code is readable
- Variable names are descriptive.
- Addresses “this” of the resulting function.

### Variations

If a candidate solves the problem handily you should probe into variations of the problem:

- How would you make memoize work for functions of arity greater than one?
- How would you allow users to modify the cache hit strategy? For example, perhaps only a subset of inputs can be memoized and the user of the library knows how to express that rule.
- How would you control cache size?
- How would you modify the solution to scale multiple nodes?

### Notes:
Possible basic solution:
```javascript
function memoize(orig) {
  var memo = {};
  return function (input) {
    if (memo.hasOwnProperty(input)) {
      return memo[input]; // cache hit
    } else {
      return memo[input] = orig(input); // cache miss
    }
  }
}
```
