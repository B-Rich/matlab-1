Empty arrays
============

Empty arrays in MATLAB come in different sized and number of dimensions. Even though the commonly known notation for empty arrays are        

 * ``[]`` for matrices
 * ``{}`` for cell arrays
 * ``struct([])`` for structure arrays 

these arrays are all 2-dimensional of size 0-by-0::

    >> size([])
    ans =
         0     0
    >> size({})
    ans =
         0     0
    >> size(struct([]))
    ans =
         0     0
 
`being edited here <http://rst.ninjs.org/?n=632484fa4ac30e5a92faf5350a49abbe&theme=nature>`_
