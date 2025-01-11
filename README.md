# Tailwind CSS @apply Directive Conflict

This repository demonstrates a bug encountered when using Tailwind CSS's `@apply` directive with conflicting class styles. The problem arises from applying multiple classes using `@apply` where the classes define the same CSS property.  The last class applied overrides previous ones, potentially leading to unexpected visual outcomes and making debugging tricky.

## Bug Description
When using `@apply` to apply multiple classes, if those classes define the same style property (like `background-color` in this example), the order of application matters. The last applied class overrides the previous one, potentially leading to subtle bugs that are hard to track down.

## How to Reproduce
1. Clone this repository.
2. Open `bug.html` in your browser.  You will observe that the div's background is blue, not red, demonstrating the override.
3. Examine `bug.html` and `bugSolution.html` to understand the issue and solution.

## Solution
The solution involves being more mindful of potential class conflicts when using `@apply`.  Use more descriptive class names and verify your class application logic to avoid accidentally overriding desired styles.  In some cases refactoring your CSS or using a more direct CSS approach might be needed.

## Note
This bug is not a flaw in Tailwind itself, but a consequence of using `@apply` with conflicting styles. Careful coding practices are essential to prevent this issue.