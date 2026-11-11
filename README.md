# J2-jenkins-script-not-label

The command must come from `script:`, never from `label:`. Regression for commit ce17fa9.

## How to test

1. Octiq QA -> Import -> GitHub -> this repo
2. In chat: `add a comment at the top of the README`
3. Read the two lines in the reply.

**Line 1 (the CI verdict - THIS IS THE TEST):**

    Tests required - CI runs `cargo test`   (NOT 'Run tests')

**Line 2 (the build/test outcome):**

    Tests passed - 4 passed        (or a real failure, never "no recipe")
