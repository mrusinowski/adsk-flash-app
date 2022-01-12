# Zadanie 2  
## Kroki instalacji  
  
1. Stworzenie dwóch maszyn wirtualnych na AWS  
2. Połączenie na sokrates.edu.jkan.pl  
3. Stworzenie pliku hosts.ini z zadeklarowaniem dwóch ip wcześniej stworzonych maszyn wirtualnych (jedna maszyna będzie proxy)
4. Stworzenie folderu 'files' zawierającego potrzebne pliki konfiguracyjne (*app.service, proxy.conf*)
5. Stworzenie pliku *setup.yml*
  
```  
Plik setup.yml zawiera: 
 
Dla aplikacji:
- zadeklarowanie repozytorium aplikacji
- instalację gita
- synchronizacje repozytorium
- nadanie permisji dostępu
- stworzenie wirtualnego srodowiska python
- rejestrację jako serwis
- uruchomienie serwisu aplikacji

Dla proxy:
- instalację EPEL
- instalację nginx
- konfigurację nginx
```

## Egzekucja setup.yml oraz rezultat
```
ansible-playbook setup.yml -i hosts.ini
```
![](zad2ss.png)
## Diagram
![](diagram.png)