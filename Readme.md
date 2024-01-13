projekt obejmuje dwa reozytoria:

 - source-repo https://github.com/AdamPiechowiak/zad2-source-repo
 - config-repo https://github.com/AdamPiechowiak/zad2-config-repo

## krok 1  

 w repozytorium source-repo znajduje się plik dockerfile oraz index.html na podstawie których budowany jest obraz z aplikacją
 w repozytorium config-repo znajdują się pliki manifestów kubernetesa:
 
  - my-app-deploy.yaml
  - my-app-ingress.yaml
  - my-app-svc.yaml
  
## krok 2 

do repozytorium source-repo został dodany plik zad2lab10.yml opisujący workflow w ramach którego jest budowany obraz z nową wersją aplikacji oraz aktualizowane jest repozytorium config-repo tak aby kożystało z nowego obrazu 

## krok 3

budowany jest obraz na podstawie pliku Dockerfile znajdującego się w tym repozytorium

![alt text](https://github.com/AdamPiechowiak/fullstack-zad2/blob/main/img/1.png)

uruchamiany jest cronejob o nazwie StepCD

![alt text](https://github.com/AdamPiechowiak/fullstack-zad2/blob/main/img/2.png)
![alt text](https://github.com/AdamPiechowiak/fullstack-zad2/blob/main/img/3.png)

## krok 4

sprawdzenie czy aplikacja działa

![alt text](https://github.com/AdamPiechowiak/fullstack-zad2/blob/main/img/4.png)

sprawdzenie czy aplikacja działa po zmianie wersji

![alt text](https://github.com/AdamPiechowiak/fullstack-zad2/blob/main/img/5.png)
![alt text](https://github.com/AdamPiechowiak/fullstack-zad2/blob/main/img/6.png)
![alt text](https://github.com/AdamPiechowiak/fullstack-zad2/blob/main/img/7.png)
![alt text](https://github.com/AdamPiechowiak/fullstack-zad2/blob/main/img/8.png)
