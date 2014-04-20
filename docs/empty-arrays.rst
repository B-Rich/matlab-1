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

.. warning::

    These functions silently ignore negative arguments and replace them with zero. That means ``ones(-10,2)`` is exactly the same as ``ones(0,2)``. This can be an issue if the arguments are calculated using other variables, e.g., before using  ``ones(m, n-m)`` one needs to explicitly check if ``n>=m``.

A common way of encountering empty arrays is by all-false logical indexing in a non-empty array. However note that using a full-size logical matrix for indexing always leads to a 0-by-1 empty array.


.. code:: matlab

    >> A=rand(2,4)
    A =
        0.0759    0.5308    0.9340    0.5688
        0.0540    0.7792    0.1299    0.4694
    >> A(A(:,1)>1, :)
    ans =
       Empty matrix: 0-by-4
    >> A(A>1)
    ans =
       Empty matrix: 0-by-1

Comparision
-----------

For statement
---------------
MATLAB for statement for I=M iterates over columns of M however it doesn't check if M is an empty array or not, therefor, following code

.. code:: matlab

    F = rand(4);
    M = F(F(:,1)>1,:);
    for I=M,
        disp('no way!')
    end

will execute the inner loop 4 times, which in most cases is not a desirable outcome.


`being edited here <http://rst.ninjs.org/?n=805e588098773e041e94e8d0f9c769db&theme=nature>`_
