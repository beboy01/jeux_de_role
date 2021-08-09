# jeux_de_role
```python

import random
point_joueur=50
point_ennemi =50
jouer=False
potion=3
while True:
     if jouer:
          print("Vous passez votre tour ...")
          jouer= False
     else:
          votre_choix=""
          while votre_choix not in ["1","2"]:
               votre_choix= input("Souhaitez vous attaquez (1) ou utiliser une potion (2): ")
          if votre_choix=="1":
               attack_joueur= random.randint(5,10)
               point_ennemi -=attack_joueur
               print(f"Vous avez infliger {attack_joueur} attack à énnemi !")
          elif votre_choix=="2" and potion >0:
               votre_potion= random.randint(5, 50)
               point_joueur  +=votre_potion
               potion -=1
               jouer=True
               print(f"Vous avez eu {votre_potion} point de vie !")
          else :
               print("Vous n'avez plus de potions ! ")
               continue
     if point_ennemi <=0:
          print("Vous avez gagné !")
          break
     attack_ennemi= random.randint(5, 15)
     point_joueur -=attack_ennemi
     print(f"L'ennemi vous à infliger {attack_ennemi} points de Dégâts ! ")
     if point_joueur <=0:
          print("Vous avez perdu !")
          break
     print(f"Il vous reste {point_joueur} points de vie")
     print(f"Il reste {point_ennemi}point de vie à l'ennemi ! ")
     print("-"* 50)
     print("Fin du jeu !")
```
