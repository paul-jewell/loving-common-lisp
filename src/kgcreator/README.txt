# Top level package for CL version of KGcreator

try:

(ql:quickload "kgcreator")
(in-package #:kgcreator)
        
## Making a standalone executable command line file (just one file):

````
$ sbcl
(ql:quickload "kgcreator")
(in-package #:kgcreator)
(sb-ext:save-lisp-and-die "KGcreator" :toplevel #'kgcreator :executable t)

````

Then, run using:

./KGcreator -i test_data -r out.rdf -c out.cyper

##  Web demo

(ql:quickload "kgcreator")
(in-package #:kgcreator)
(kgcweb)

http://localhost:3000

