Overview
========

function declarations
---------------------

template: [1]_

.. code-block:: go

   func nameOfFunc(arguments) (returnTypes) {
       // body
   }

examples: [1]_

.. code-block:: go

   func multiply(x, y int) int {
       return x*y
   }

   func showAge(name string, age int) {
       fmt.Printf("%s is %d years old.\n", name, age)
   }

   func addSub(x, y int) (int, int) {
       return x+y, x-y
   }


data types
----------

boolean: [2]_

- ``bool``

integers: [3]_

- ``int`` (platform dependent)
- ``int8``  -128 to 127
- ``int16`` -32768 to 32767
- ``int32`` -2147483648 to 2147483647
- ``int64``
- ``uint``
- ``uint8``
- ``uint16``
- ``uint32``
- ``uint64``

floats: [4]_

- ``float32``
- ``float64``

string: [5]_

- ``string``


structs
-------

template: [6]_

.. code-block:: go

   type struct_name struct {
       member1 datatype
       member2 datatype
       member3 datatype
   }

example: [6]_

.. code-block:: go

   type Person struct {
       name string
       age int
       job string
       salary int
   }


arrays
------

template: [7]_

.. code-block:: go

   var array_name = [length]datatype{values}
   var array_name = [...]datatype{values}

example: [7]_

.. code-block:: go

   var arr1 = [3]int{1,2,3}
   arr2 := [5]int{4,5,6,7,8}


array initialization
~~~~~~~~~~~~~~~~~~~~

If not initialized, elements receive default values.

.. code-block:: go

   arr1 := [5]int{}
   arr2 := [5]int{1,2}
   arr3 := [5]int{1,2,3,4,5}


sources
-------

.. [1] https://golangdocs.com/functions-in-golang
.. [2] https://www.w3schools.com/go/go_boolean_data_type.php
.. [3] https://www.w3schools.com/go/go_integer_data_type.php
.. [4] https://www.w3schools.com/go/go_float_data_type.php
.. [5] https://www.w3schools.com/go/go_string_data_type.php
.. [6] https://www.w3schools.com/go/go_struct.php
.. [7] https://www.w3schools.com/go/go_arrays.php
