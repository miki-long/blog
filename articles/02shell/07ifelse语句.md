1. 一般 if 语句
```
    #!/bin/bash
    echo -n "Please input a score:"
    read SCORE
    if [ "$SCORE" -lt 60 ]; then
       echo "C"
    fi
    if [ "$SCORE" -lt 80 -a "$SCORE" -ge 60 ]; then
       echo "B"
    fi
    if [ "$SCORE" -ge 80 ]; then
       echo "A"
    fi
```    
2. if else 语句

3. if elseif else 语句

4. switch case 语句