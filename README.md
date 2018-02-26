#include <stdio.h>
#include<stdlib.h>
  
int main(){
   
	int numero;  
	int numero2; 
	int numero3; 
	int numero4;    
	int fact=2;      
	int i=0;   
	int x;
	int factorprimo[1000];
	int cociente[1001];
	   
    int est1=1;
    
     puts("			EL PROGRAMA DE LOS FACTORES PRIMOS\n\n");
     	printf("Ingrese un numero entero: "); 
	 		scanf("%d", &numero);
     
  	 if(numero<1)
          printf("\nDato no valido.");
     else if (numero==1)
          printf("\n     ADVERTENCIA! \n\t No tiene factores primos.");
     else {
          numero4=numero;
          while(numero>1){
                 if(numero%fact==0){
                        numero2=numero; numero/=fact; numero3=numero2/fact;
                        	if(est1){
                             	factorprimo[0]=fact; 
								 	cociente[0]=numero3; 
								 		est1=0;
                        	}
                        	else {
                            	i++; factorprimo[i]=fact;
								 	 cociente[i]=numero3;
                        	}
                  }
        	else
        		fact++;
           }
           
		   printf("\nNumero ingresado: %d\n",numero4);
           printf("\nFactores primos: %d\n",factorprimo[0]);
           
		   for(x=1;x<=i;x++)
                  printf("\t%d",factorprimo[x]);
           printf("\nCocientes de factorizacion: %d\n",cociente[0]);
            for(x=1;x<=i;x++)
                  printf("\t%d",cociente[x]);
       }
       return 0;;


}
