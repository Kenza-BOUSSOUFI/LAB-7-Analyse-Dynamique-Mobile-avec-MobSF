# LAB-7-Analyse-Dynamique-Mobile-avec-MobSF

# Étape 1 : Création de l’émulateur AVD sans Play Store

Pour ce lab je vais utiliser un emulateur pixel 5 System Image: Google APIs (API 30)

<img width="1108" height="811" alt="image" src="https://github.com/user-attachments/assets/2675fd6f-979d-4c0b-aac5-14041e86a739" />

# Étape 2 : Cloner MobSF pour utiliser les scripts AVD officiels

Dans un Terminal:

<img width="792" height="90" alt="image" src="https://github.com/user-attachments/assets/2df6a4f8-ba46-4ea8-ae95-05ba8d01627c" />

<img width="476" height="876" alt="image" src="https://github.com/user-attachments/assets/a7a12579-a9d9-4466-a5e0-36c84a436df9" />

# Étape 3 : Lancement de l’émulateur avec le script MobSF (rooté & prêt pour l’analyse)
1. On va lancer l’émulateur 'MobSF_DIVA' avec le script MobSF: 

<img width="1770" height="940" alt="image" src="https://github.com/user-attachments/assets/7f145f1f-7644-4097-bca9-292c7d83b002" />

2. Après, on va noter l'identifiant de notre emulateur:

<img width="791" height="73" alt="image" src="https://github.com/user-attachments/assets/ba3c8a65-f397-4abf-b197-3c86876b18c1" />


Donc L’émulateur est maintenant rooté et configuré pour MobSF.

# Étape 4 : Installation et lancement de MobSF via Docker 

1. Téléchargement de l'image MobSF:

Dans un nouveau terminal (émulateur toujours en marche) :

<img width="962" height="367" alt="image" src="https://github.com/user-attachments/assets/16f0793c-8df0-48a4-bec0-4c20777d31e3" />

Image MobSF téléchargée avec succès.

2. Lancement de MobSF en utilisant l'identifiant de notre émulateur ( emulator-5554 ):

<img width="1372" height="1022" alt="image" src="https://github.com/user-attachments/assets/c5affa1c-185e-4772-8252-acc256342562" />

3. Dans notre navigateur, on va ouvrir  : http://127.0.0.1:8000  (émulateur toujours en marche AVANT MobSF, sinon l’analyse dynamique échoue).

Login / Mot de passe par défaut : mobsf / mobsf

<img width="1917" height="866" alt="image" src="https://github.com/user-attachments/assets/fb3243e8-61d9-4708-b360-b3b25e3328c5" />

<img width="1913" height="973" alt="image" src="https://github.com/user-attachments/assets/15345227-d11b-4d7b-8ce7-9f0d65df9d21" />

# Étape 5 : Téléchargement de l’APK DIVA (Damn Insecure and Vulnerable App)

<img width="911" height="247" alt="image" src="https://github.com/user-attachments/assets/dfd3c744-fecc-4c76-9b53-fcd7f5f4f1b4" />

# Étape 6 : Analyse Statique + Dynamique de DIVA

1. Dans MobSF → Upload & Analyze → choisissez votre diva.apk (pour notre cas DivaApplication.apk).
2. Aprés, on va attendre la fin de l’analyse statique:

<img width="1546" height="855" alt="image" src="https://github.com/user-attachments/assets/939ceecf-d1a0-40ce-9547-a867f8f98a9a" />

<img width="1896" height="886" alt="image" src="https://github.com/user-attachments/assets/11b76708-f37b-4b7d-93a9-1eac7cac1d79" />

3. Dans le rapport de scan → on va cliquer sur le gros bouton « Start Dynamic Analyzer ».


<img width="1907" height="882" alt="image" src="https://github.com/user-attachments/assets/f037932b-19e9-4c09-9ae0-8109fbc69189" />

MobSF va :

Installer automatiquement DIVA sur l’émulateur.

Lancer Frida Server

Configurer le proxy HTTPS global.

Ouvrir l’interface Dynamic Analyzer.

1. Avec un Clique sur "Show Screen" dans MobSF pour voir l'émulateur, puis on va ouvrir l'app DIVA

<img width="1901" height="880" alt="image" src="https://github.com/user-attachments/assets/0895dda1-30ce-47cb-96ac-783816a1895c" />

2. Ensuite pour afficher les 13 challenges (Insecure Logging, Hardcoded, Insecure Storage, etc.), on va choisir MainAvtivity

puis on va cliquer sur start activity.

 <img width="636" height="658" alt="image" src="https://github.com/user-attachments/assets/2e741ed5-ce9e-4e7e-a998-1d3665e9372f" />

<img width="1831" height="883" alt="image" src="https://github.com/user-attachments/assets/b2bc3bfc-0408-44d1-a5dc-4db036268e83" />

1️⃣ Runtime Logs (Logcat Stream)
Clique sur Logcat Stream en haut dans MobSF, puis dans DIVA :

<img width="1920" height="972" alt="image" src="https://github.com/user-attachments/assets/2d406948-cdc5-4499-afc7-3d600da13df2" />























