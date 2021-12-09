# The Art of the Code Review

## Things to look for

When reviewing code, some aspects worth considering and commenting-on.

### Functionality

Does the code provide the required functionality? Is it sufficiently
robust, with appropriate error-handling?

### Style

Does the code style meet your workplace's _published_ code style guide?
Does the code meet the expected style for the programming language?
In existing codebases, does the style broadly follow the rest of the codebase
without being too jarring? Excessively repetitive code also falls under
this heading.

### Security

Does the new code introduce or exacerbate security holes?

### Performance

Most code is not performance-critical (CPU, memory, IO and so-forth).
If it is, are the aspects of the code that are sub-optimal?
If not, are there any really inefficient things which could be fixed
without harming readability?

### Readability

Will the next developer, who might be junior, be able to understand
what's going on? If not, would some comments help, or could the code
be structured differently? Sometimes even better-chosen function or
variable names can make all the difference.

## Ask questions

If you're tempted to ask why the author didn't do something the
obvious way, stop and find out why.

Perhaps they didn't know about the obvious way and need you to
show them? Or (more common), they tried the obvious way and found that
in this scenario it just didn't work.

Asking _why_ provides a way for the author to explain their
approach without the defensiveness that a negative comment creates.

## I'm unhappy with something else!

You're probably being unfair on the author.

If it's something that is clear-cut wrong that everyone in your workplace
will agree with, then get it added to your style guide - then everyone
will know for future.

Otherwise, there's a likelihood you're really expressing
"that's now how _I_ would have done it". That's because you're not the author
and if you feel so strongly and are unable to let go, perhaps you should
_be_ the author? Every author is different and it's only fair to allow
them the same freedom and creativity that you would expect.
