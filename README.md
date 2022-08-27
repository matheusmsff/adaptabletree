# Adaptable tree using C

#include <stdio.h>

int main (){

  int lines, columns, size=0;

  printf("Input a size for the tree: ");
  scanf("%d", &size);

  columns = size * 13;
  lines = size * 11;
  
  for(int i=0; i<(lines/2)+2; i++){
    for (int j=0; j<columns; j++){
      if(j==((lines/2)+1) || j==((lines/2)+1)+i || j==((lines/2)+1)-i || ((lines/2)+1)-i<j && j<((lines/2)+1) || j>((lines/2)+1) && j<((lines/2)+1)+i){
        printf(" * ");
      }
      else{
        printf("   ");
      }
    }
    printf("\n");
  }

  for(int i=0; i<(lines/2)-1; i++){
    for (int j=0; j<columns; j++){
      if(j==((lines/2)+1) || j==((lines/2)+1)+1 || j==((lines/2)+1)-1){
        printf(" * ");
      }
      else {
        printf("   ");
      }
    }
    printf("\n");
  }

  return 0;
}
