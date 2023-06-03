# Les robots et l'infini 

Code correspondant à l'article *Les robots et l'infini* de la revue [Pour La Science](https://www.pourlascience.fr/) (PLS 551 - aout 2023) 

Comment faire en sorte qu'un robot, doté de capacités très limitées (minimum de mémoire, voire pas de mémoire) soit capable de parcourir une surface infinie ?
Précisons qu'un simple compteur de nombre de pas necessite, à l'infini, une mémoire infinie !

Le fichier robot-spirale.nlogo contient le code correspondant écrit en [Netlogo](https://ccl.northwestern.edu/netlogo/)
1. téléchargez le fichier (bouton Code (vert) puis "download ZIP")
2. allez sur https://netlogoweb.org/
3. cliquez sur "Run in your Browser" puis en haut à droite "parcourir"
4. chargez le fichier sauvegardé (robot-spirale.nlogo) 

![robot-algo2](https://user-images.githubusercontent.com/20242612/236641530-d0d7ca14-56e3-4c5f-9920-1534e9f91509.gif)
![robot-algo4](https://github.com/cristal-smac/robot-spirale/assets/20242612/b3d72151-f025-4594-a2be-c9ed5665f93c)
![robot-algo5](https://user-images.githubusercontent.com/20242612/236641509-dec4bbdb-ac0d-43be-85cb-12806c698462.gif)
![robot-algo6](https://github.com/cristal-smac/robot-spirale/assets/20242612/0d489867-9456-48c3-88cf-379241956c2a)

Dasn ces quatre figures, les cases noires sont inconnues, les cases blanches sont les cases parcourues par le robot et les X rouges sont les marques utilisées par le robot. Seul l'algorithme 4 utilise une marque.

- fig1 : algo 2  : L'agent compte ses pas dans chaque direction et incrémente à chaque tour. C'est la technique "classique". Cela necessite une position angulaire (4 valeurs) et 3 entiers (infinité de valeurs), ce qui ne fonctionne pas à l'infini, contrairement aux trois suivants.
- fig2 : algo 4  : L'agent pose des marques et tourne autour de ses marques. Il ne compte rien. Cela necessite une position angulaire (4 valeurs) et savoir tester/placer une marque. Dans cette image, des marques on déjà été posées afin de "troubler" le robot.
- fig3 : algo 5  : L'agent pousse des balises qui lui servent de butée. Quand il en rencontre une, il la pousse et change de direction. Il ne compte rien. Cela necessite une position angulaire (4 valeurs) et 4 panneaux 
- fig4 : algo 6  : L'agent change de direction à chaque rencontre d'un des deux agents qui voyage en diagonale. Cela necessite un synchronisation parfaite des agents. Aucun d'entre eux ne compte quoi que ce soit. Cela necessite 3 agents, chacun avec une position angulaire et détecter un autre agent
