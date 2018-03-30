---
layout: post
title: "[HL-22] Three ways to mock methods and objects with unittest.mock.patch"
categories:
    - testing
tags:
    - Python
    - unittest
    - patch
    - mock
published: true
---

I recently write some unit tests by using `unittest.mock` module to mock objects/methods. `patch` is a very handy tool to use. However, it is not so obvious to use at the beginning.

# Mock a method

<script src="https://gist.github.com/HengfengLi/69594dfb91db4a1d793a299e2f659818.js"></script>

Solution 1 is easy to understand, which uses a method to replace `requests.get`.

Solution 2 generates an instance of MagicMock (default), which has an attribute `return_value` as the return value of its function call.

# Mock the attribute of an instance

However, when the return value is an instance of a class, which has some attributes. How should we mock it?

<script src="https://gist.github.com/HengfengLi/b2590d1c9754361ce438e20322b2de18.js"></script>

In doing so, we can mock the attribute of an instance.

# Mock instances generated by nested factory methods

A more complex case would be as follows:

<script src="https://gist.github.com/HengfengLi/38f2d41c82d9cb03e3b772032463fa78.js"></script>

As you can see, `resource()` generates a `Resource` instance and `Resource.Table()` creates a `Table` instance. So if we would like
to mock the `Table` instance, we need to mock the `return_value` twice.

The `unittest.mock` has more features to explore, but so far the above three patching solutions can make my writing of a unit test much easier.