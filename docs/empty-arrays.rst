Empty arrays
============

Empty arrays in MATLAB come in different sized and number of dimensions. Even though the commonly known notation for empty arrays are        

 * ``[]`` for matrices
 * ``{}`` for cell arrays
 * ``struct([])`` for structure arrays 

these arrays are all 2-dimensional of size 0-by-0:

.. code:: matlab

    >> size([])
    ans =
         0     0
    >> size({})
    ans =
         0     0
    >> size(struct([]))
    ans =
         0     0

Empty arrays can come in as many number of dimensions or dimensions as long as at least one dimension is zero. Any of MATLAB function that create a special array by taking the dimensions of it as input arguments can be used to create such an empty array:

.. code:: matlab

    >> ones(1,2,0)
    ans =
       Empty array: 1-by-2-by-0
    >> zeros(5,0,2,4)
    ans =
       Empty array: 5-by-0-by-2-by-4
    >> cell(3,5,8,13,0)
    ans = 
       Empty cell array: 3-by-5-by-8-by-13-by-0
    >> struct(rand(1,2,0))
    ans = 
       1x2x0 struct array with no fields.

Comparision
-----------

`being edited here <http://rst.ninjs.org/?n=965979ed973e11139752e05048605007&theme=nature>`_
