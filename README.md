# Unexpected Behavior When Modifying Instance Variables Through Getter Methods

This repository demonstrates a subtle but common error in Ruby related to how instance variables are accessed and modified.

## The Problem

In Ruby, it's tempting to modify an instance variable by assigning a value to its getter method. However, this does not work as expected. The assignment creates a new local variable, leaving the instance variable unchanged.  The example in `bug.rb` illustrates this issue.

## The Solution

The correct way to modify an instance variable is to use methods that explicitly update it, such as `instance_variable_set` or define a setter method.  `bugSolution.rb` demonstrates the proper way to achieve this.

## How to Reproduce

1. Clone this repository.
2. Navigate to the directory containing `bug.rb`.
3. Run `ruby bug.rb`. Observe the output and note the unexpected results.
4. Run `ruby bugSolution.rb`. Observe the corrected output.
