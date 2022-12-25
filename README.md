# projet-SM
#include <stdio.h>  //tali mohamed redouane  Groupe 10  matricule:222231362601
#include <stdlib.h>

int main()
{ int poid,somme1,somme2,nombre,nombre_affichage,base_initial,base_finale;

    //la declaration de nombre et des bases:
    printf("donner le nombre :");
    scanf("%d",&nombre);
    nombre_affichage=nombre; // nombre_affichage c'est pour affichier le nombre a la fin
    printf("donner la base initial du nombre:");
    scanf("%d",&base_initial);
    printf("doner la base finale:");
    scanf("%d",&base_finale);
    //parte 1:
    //la  parte 1 aide quand tu vuex transformer un nombrer de base 10 a une autre base
    // DE BASE 10 ==> A LA BASE FINALE:
    if(base_initial==10)
    {  poid=1; somme1=0;

        while(nombre!=0){
            somme1=somme1+(nombre%base_finale)*poid;
            poid=poid*10;
            nombre=nombre/base_finale;
        }
        printf("(%d)%d=(%d)%d",nombre_affichage,base_initial,somme1,base_finale);
    // parte 2:
    // la parite 2 aide si tu vuex transformer un nombre d'une base initiale a la base 10
    // DE BASE INETILAE ==> A LA BASE 10 :

    }else if(base_finale==10)
           { poid=1; somme2=0;

          while(nombre!=0){
                somme2=(nombre%10)*poid+somme2;
                poid=poid*base_initial;
                nombre=nombre/10;
              }

        printf("(%d)%d=(%d)%d",nombre_affichage,base_initial,somme2,base_finale);
     // parte 3:
     // la parte 3 aide si tu vuex transformer un nombre d'une base initiale a la base finale
     // DE BASE INETIALE ==> A LA BASE FINALE:
     // DABORD ON TRANSFORME LE NOMBRE DE BASE INITIALE==> A LA BASE 10
     // APRES DE BASE 10 ==> A LA BASE FINALE

      }else{poid=1; somme2=0;

          while(nombre!=0){
                somme2=(nombre%10)*poid+somme2;
                poid=poid*base_initial;
                nombre=nombre/10;

                }
             poid=1; somme1=0;
          while(somme2!=0){
               somme1=somme1+(somme2%base_finale)*poid;
               poid=poid*10;
               somme2=somme2/base_finale;



              }
          //affichage des resultas
          printf("(%d)%d=(%d)%d",nombre_affichage,base_initial,somme1,base_finale);


           //donc avec ce projet on peutx transformer les nombres:
           // 1:de base 10 a la base finale (parte 1)
           // 2:de base initiale a la base 10(parte 2)
           // 3:de base initiale a la base finale(parte 3)
             }





return 0;
}
