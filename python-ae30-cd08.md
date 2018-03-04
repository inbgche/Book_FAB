-- 파일 읽기 문법

filereader를 쓰지 말고 아래 방식을 쓰자. 닫기를 명시하지 않아도 자동으로 파일이 닫기어져서 안전하다. 

```python
#!/usr/bin/env pytho3

from math import exp, log, sqrt
import re
from datetime import date, time, datetime, timedelta
from operator import itemgetter
import sys


input_file = sys.argv[1]
print("Output file:")

with open(input_file,'r', newline='') as filereader:
    for row in filereader:
        print("{}".format(row.strip())


```



-- **glob.glob**은 특정 폴더에서 패턴과 일치하는 모든 파일을 찾는다. 

```python
#!/usr/bin/env pytho3

from math import exp, log, sqrt
import re
from datetime import date, time, datetime, timedelta
from operator import itemgetter
import sys
import glob
import os 

print("Output 폴더의 조건에 맞는 파일 읽기 예제")
inputPath = sys.argv[1]
for input_file in glob.glob(os.path.join(inputPath, '*.txt')):
    with open(input_file, 'r', newline = '') as filereader:
        for row in filereader:
            print("{}".format(row.strip()))
            
```





