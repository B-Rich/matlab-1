Empty arrays
------------

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
 
`being edited here <http://rst.ninjs.org/?n=23d9ede1c097c55b468b85b4333aeca8&theme=nature>`_
