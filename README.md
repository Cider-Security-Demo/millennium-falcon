## Introduction

This package extends Flask-RESTful by implementing datacentric Resources using **dbbase** for enabling the use of SQLAlchemy.

Creating a website can result in a fair amount of boilerplate code as the same characteristics for table models are recreated at each layer. Then, the boilerplate code must be tested as well, resulting in boilerplate testcode.

Using this package, the database models are introspected and applied to the API, resulting in less code over all.

This package should be thought of as a tool rather than a framework. It can coexist with other Flask packages. A framework can get awkward on edge cases as a seemingly straight-forward idea turns out to be very difficult due to trying to fit it into the framework design.

Inherent in the design is an understanding that the simplest cases can be done simply, but that there are additional ways to open up the functionality to accommodate more difficult issues.

And, if the issue encountered does not fit this package's approach, the original resource classes used with no loss of functionality.

The design of Flask-RESTful-DBBase creates Flask-RESTful style Resources, but are derived directly from the SQLAlchemy model classes.