::

     >> a=[]
     a =
          []
     >> c = (a==[])
     c =
          []
     >> class(a==[])
     ans =
     logical
     >> class(1==[])
     ans =
     logical
     >> (1==[])
     ans =
          []
     >> (ones(10)==[])
     Error using  == 
     Matrix dimensions must agree. 
     >> size(1)
     ans =
          1     1
     >> (ones(1,1)==[])
     ans =
          []
     >> (ones(1,0)==[])
     Error using  == 
     Matrix dimensions must agree. 
     >> (ones(0,1)==[])
     Error using  == 
     Matrix dimensions must agree. 
     >> (ones(0,0)==[])
     ans =
          []
     >> (ones(0,1)==[])
     Error using  == 
     Matrix dimensions must agree. 
     >> (ones(1,0)==[])
     Error using  == 
     Matrix dimensions must agree. 
     >> (ones(1,1)==[])
     ans =
          []
     >> (ones(1,1,1)==[])
     ans =
          []
     >> (ones(1,1,0)==[])
     Error using  == 
     Number of array dimensions must match for binary array op. 
     >> (ones(1,1,1)==[])
     ans =
          []
     >> size(ones(1,1,1))
     ans =
          1     1
     >> size(ones(1,1,1,1))
     ans =
          1     1
     >> if (a==[]), disp(1); else disp(0); end
          0
     >> isequal([], [])
     ans =
          1
     >> isequal(1, [])
     ans =
          0
     >> isequal(ones(0,0), [])
     ans =
          1
     >> isequal(ones(0,0,0), [])
     ans =
          0
     >> 
     >> load('284_Do_Aktiv_Driving_1_nhctFormat_001.mat')
     >> any([])
     ans =
          0
     >> all([])
     ans =
          1
     >> all([1 0])
     ans =
          0
     >> all([1 1])
     ans =
          1
     >> if [1 1], disp(1), else disp(0), end
          1
     >> if [1 0], disp(1), else disp(0), end
          0
     >> if [0 0], disp(1), else disp(0), end
          0
     >> if [], disp(1), else disp(0), end
          0
     >> doc if
     >> if [2.1 3], disp(1), else disp(0), end
          1
     >> if {2.1 3}, disp(1), else disp(0), end
     Conversion to logical from cell is not possible.
      
     >> if logical([]), disp(1), else disp(0), end
          0
     >> if logical([0 1]), disp(1), else disp(0), end
          0
     >> if ones(2), disp(1), else disp(0), end
          1
     >> if [1 0; 1 1], disp(1), else disp(0), end
          0
     >> if ones(2,2,2), disp(1), else disp(0), end
          1
     >> if ones(2,2,0), disp(1), else disp(0), end
          0
     >> a(2,2) = containers.map
     Undefined variable "containers" or function "containers.map".
      
     >> a(2,2) = containers.Map
     Error using containers.Map/subsasgn
     Parameter must be a scalar.
      
     >> a(2,2) = containers.Map('a','a')
     The following error occurred converting from containers.Map to double:
     Error using double
     Conversion to double from containers.Map is not possible.
      
     >> a
     a =
          []
     >> clear a
     >> a(2,2) = containers.Map('a','a')
     Error using containers.Map/subsasgn
     Parameter must be a scalar.
      
     >> doc  containers.Map
     >> a(2,2) = containers.Map({'a'},{'a'})
     The following error occurred converting from containers.Map to double:
     Error using double
     Conversion to double from containers.Map is not possible.
      
     >> clear a
     >> a = containers.Map({'a'},{'a'})
     a = 
       containers.Map handle
       Package: containers
     
       Properties:
             Count: 1
           KeyType: 'char'
         ValueType: 'char'
       Methods, Events, Superclasses
     >> a(2) = containers.Map({'a'},{'a'})
     Error using containers.Map/subsasgn
     Specified key type does not match the type expected for this container.
      
     >> handle
     Error using handle
     Not enough input arguments.
      
     >> class(a)
     ans =
     containers.Map
     >> doc  containers.Map
     >> a = []
     a =
          []
     >> a(:)
     ans =
        Empty matrix: 0-by-1
     >> a=ones(2,2,0)
     a =
        Empty array: 2-by-2-by-0
     >> a(:)
     ans =
        Empty matrix: 0-by-1
     >> a=ones(2,0,5,6)
     a =
        Empty array: 2-by-0-by-5-by-6
     >> a(:)
     ans =
        Empty matrix: 0-by-1
     >> all(a(:))
     ans =
          1
     >> if a(:), disp(1), else disp(0), end
          0
     >> edit if
     >> a=[]
     a =
          []
     >> for k=a(:), disp(a), end
     >> size(a(:))
     ans =
          0     1
     >> for k=a(:), disp(1), end
          1
     >> for k=a(:)', disp(1), end
     >> doc colon
     Warning: MATLAB was unable to launch your System web browser:
     
     'cmd.exe' is not recognized as an internal or external command,
     operable program or batch file.
      
     > In web>displayWarningMessage at 430
       In web>handleWarning at 421
       In web>openWindowsBrowser at 410
       In web at 132 
     >> size(1:-1:10)
     ans =
          1     0
     >> size(100:1:10)
     ans =
          1     0
     >> size(1:0:10)
     ans =
          1     0
     >> size(100:0:10)
     ans =
          1     0
     >> doc column
     >> doc colon
     >> reshape([], [], 1)
     ans =
        Empty matrix: 0-by-1
     >> reshape([], 1, [])
     ans =
        Empty matrix: 1-by-0
     >> all(a(:))
     ans =
          1
     >> all(a(:)')
     ans =
          1
     >> doc all
     >> a=[]
     a =
          []
     >> a(end)
     Subscript indices must either be real positive integers or logicals.
      
     >> reshape([], 1, 2, 3, [])
     ans =
        Empty array: 1-by-2-by-3-by-0
     >> reshape([], 1, 2, 3, 0)
     ans =
        Empty array: 1-by-2-by-3-by-0
     >> reshape([], 1, 2, 3, 1)
     Error using reshape
     To RESHAPE the number of elements must not change.
      
     >> reshape([], 1, 2, 0, 10)
     ans =
        Empty array: 1-by-2-by-0-by-10
     >> [ones(0,10), ones(0,12)]
     ans =
        Empty matrix: 0-by-22
     >> [ones(0,10); ones(0,12)]
     Warning: Concatenation involves an empty array with an incorrect number of columns.
     This may not be allowed in a future release. 
     ans =
        Empty matrix: 0-by-12
     >> [ones(0,10); ones(0,10)]
     ans =
        Empty matrix: 0-by-10
     >> a=ones(0,10)
     a =
        Empty matrix: 0-by-10
     >> 
     >> 1+[]
     
Operators::

     ans =
          []
     >> 1*[]
     ans =
          []
     >> 1-[]
     ans =
          []
     >> []-1
     ans =
          []
     >> []/2
     ans =
          []
     >> 2/[]
     Error using  / 
     Matrix dimensions must agree.
      
     >> 1.*[]
     ans =
          []
     >> 1./[]
     ans =
          []
     >> [].ones(2)
      [].ones(2)
       |
     Error: Unexpected MATLAB operator.
      
     >> []./ones(2)
     Error using  ./ 
     Matrix dimensions must agree.
      
     >> ones(2)./1
     ans =
          1     1
          1     1
     >> ones(2)./[]
     Error using  ./ 
     Matrix dimensions must agree.
      
     >> 1^[]
     ans =
          []
     >> 1.^[]
     ans =
          []
     >> ones(2).^[]
     Error using  .^ 
     Matrix dimensions must agree.
      
     >> ones(2)^[]
     Error using  ^ 
     Inputs must be a scalar and a square matrix.
     To compute elementwise POWER, use POWER (.^) instead.
      
     >> []^2
     ans =
          []
     >> [].^2
     ans =
          []
     >> [].^ones(2)
     Error using  .^ 
     Matrix dimensions must agree.
      
     >> []^ones(2)
     Error using  ^ 
     Inputs must be a scalar and a square matrix.
     To compute elementwise POWER, use POWER (.^) instead.
      
     >> sin([])
     ans =
          []
     >> log([])
     ans =
          []
     >> isequal(log([]), [])
     ans =
          1
     >> sin(ones(0,0))
     ans =
          []
     >> size(sin(ones(0,0)))
     ans =
          0     0
     >> size(sin(ones(0,1)))
     ans =
          0     1
     >> size(sin(ones(1,0)))
     ans =
          1     0
     >> size(sin(ones(1,0,2,3,4)))
     ans =
          1     0     2     3     4
     >> size(ones(0))
     ans =
          0     0
     >> size(ones(-1))
     ans =
          0     0
     >> size(ones(-100))
     ans =
          0     0
     >> size(ones(-100,0))
     ans =
          0     0
     >> size(ones(-100,-10))
     ans =
          0     0
     >> rand(0)
     ans =
          []
     >> []+[]
     ans =
          []
     >> []*[]
     ans =
          []
     >> []/[]
     ans =
          []
     >> []\[]
     ans =
          []
     >> \
      \
     |
     Error: Unexpected MATLAB operator.
      
     >> []^[]
     Error using  ^ 
     Inputs must be a scalar and a square matrix.
     To compute elementwise POWER, use POWER (.^) instead.
      
     >> [].^[]
     ans =
          []
     >> ones(0,10)+ ones(0,20)
     Error using  + 
     Matrix dimensions must agree.
      
     >> ones(0,10)* ones(0,20)
     Error using  * 
     Inner matrix dimensions must agree.
      
     >> ones(0,10)* ones(10,0)
     ans =
          []
     >> ones(10,0)* ones(0,10)
     ans =
          0     0     0     0     0     0     0     0     0     0
          0     0     0     0     0     0     0     0     0     0
          0     0     0     0     0     0     0     0     0     0
          0     0     0     0     0     0     0     0     0     0
          0     0     0     0     0     0     0     0     0     0
          0     0     0     0     0     0     0     0     0     0
          0     0     0     0     0     0     0     0     0     0
          0     0     0     0     0     0     0     0     0     0
          0     0     0     0     0     0     0     0     0     0
          0     0     0     0     0     0     0     0     0     0
     >> 
