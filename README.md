# CSS Specificity Bug: Unexpected Color Override

This repository demonstrates a subtle bug related to CSS selector specificity.  The problem stems from the unexpected interaction between selectors of different specificity.  The `h1 em` selector, despite only applying a style to an `<em>` tag *inside* an `<h1>` tag, has higher specificity than `h1`, causing unexpected color behavior.  This highlights the importance of understanding CSS specificity when writing complex stylesheets.

## Bug Description
The expectation is that `<h1>` text should be red, as specified in the CSS. However, due to the higher specificity of the `h1 em` selector, the text turns blue.

## Solution
The solution involves increasing the specificity of the `h1` selector, to ensure it overrides the `h1 em` rule.  This can be done by adding an extra selector, such as a class or ID.