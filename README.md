The ’futile.options’ subsystem provides an easy user-defined options management
system that is properly scoped. This means that options created via 
’futile.options’ are fully self-contained and will not collide with options 
defined in other packages. This package is a self-contained package within the 
futile suite of libraries.

Details
=======
While R provides a useful mechanism for storing and retrieving options, there is
a danger that variable names collide with names defined by a package that a 
user’s code depends. These types of errors are difficult to detect and should
be avoided. Using ’futile.options’ addresses this problem by properly scoping 
variables within its own custom ’namespace’. This is handled by the 
’OptionsManager’, which acts as a generator for functions that manage user-
defined options.

An added benefit to the package is that default values are automatically 
supported in the creation of the bespoke options manager.

Example
=======

 my.options <- OptionsManager('my.options', default=list(a=2,b=3))
 my.options(c=4,d='hello')
 my.options(c('b','d'))
 reset.options(my.options)
 my.options('c')


Author
======
Brian Lee Yung Rowe
