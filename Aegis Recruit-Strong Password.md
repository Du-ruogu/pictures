## C语言
![Alt text](https://github.com/Du-ruogu/pictures/blob/main/QQ%E6%88%AA%E5%9B%BE20210928181913.png)
![Alt text](https://github.com/Du-ruogu/pictures/blob/main/QQ%E6%88%AA%E5%9B%BE20210928182452.png)
![Alt text](https://github.com/Du-ruogu/pictures/blob/main/QQ%E6%88%AA%E5%9B%BE20210928182522.png)
![Alt text](https://github.com/Du-ruogu/pictures/blob/main/QQ%E6%88%AA%E5%9B%BE20210928183728.png)
![Alt text](https://github.com/Du-ruogu/pictures/blob/main/QQ%E6%88%AA%E5%9B%BE20210928182545.png)
![Alt text](https://github.com/Du-ruogu/pictures/blob/main/QQ%E6%88%AA%E5%9B%BE20210928182617.png)
![Alt text](https://github.com/Du-ruogu/pictures/blob/main/QQ%E6%88%AA%E5%9B%BE20210928182645.png)

```c
#include <stdio.h>
#include <ctype.h>

int main(){
    int count = 0;
    char i;
    int a = 0, b = 0, c = 0, d = 0, length;
    char pw[21];
    
    while((i = getchar()) != '\n' && count != 21){
        pw[count] = i;
        count++;
    }

    //判断长度是否符合要求 
	if(count < 9){
        printf("No, too short");
        return 0;
    }
    if(count > 20){
        printf("No, too long");
        return 0;
    }
    
	//判断是否有特殊符号 
	length = count--;
	count = 0;
    while(count <= 20 && count <= length -1 && a != 1){
    	if(ispunct(pw[count]) != 0){
    		a = 1;
		}
		count++;
	}
	if(a == 0){
		printf("No, must contain symbols");
		return 0;
	}
	
	//判断是否有小写字母 
	count = 0;
    while(count <= 20 && count <= length -1 && b != 1){
    	if(islower(pw[count]) != 0){
    		b = 1;
		}
		count++;
	}
	if(b == 0){
		printf("No, must contain lowercase letters");
		return 0;
	}
	
	//判断是否有大写字母 
	count = 0;
    while(count <= 20 && count <= length -1 && c != 1){
    	if(isupper(pw[count]) != 0){
    		c = 1;
		}
		count++;
	}
	if(c == 0){
		printf("No, must contain uppercase letters");
		return 0;
	}
	
	//判断是否有数字 
	count = 0;
    while(count <= 20 && count <= length -1 && d != 1){
    	if(isdigit(pw[count]) != 0){
    		d = 1;
		}
		count++;
	}
	if(d == 0){
		printf("No, must contain numbers");
		return 0;
	}
	
	printf("That's OK!");
	return 0;
}
```
