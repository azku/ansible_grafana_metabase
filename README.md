# Grafana eta Metabase zerbitzarien instalazioa Ansible erabiliz
## Sarea (Netplan)
Jarduera hau, IsardVDI bezalako ingurune batean prestatzeko pentsatua izan da. Makina birtualera sarbidea lortu eta pasahitz gabeko ssh gako bidezko sarbidea prestatu ondoren exekutatu beharko da.

Prozesuak lehenengo sare lokala prestatuko du. Ideia nagusia, beste makina batetako Prometheus bezalako zerbitzuak erabiltzea izango denez, sare lokal bat konfiguratu beharko da. Prometheus zerbitzariaren konfigurazioa beste proiektu batean eskainiko da.

Sare lokaleko IP helbidea DHCP bitartez jasotzea esperoko da.

## Grafana
Ubuntu/Debian systemare apt pakete kudeatzailea erabilita eta systema eguneratu ondoren, Grafana instalatu eta zerbitzua martxan jartzen da.

## Docker
Ubuntu/Debian systeman Docker instalatzeko biltegi (repository) berria gehitu behar da lehenengo. Ondoren instalazioa burutu, erabiltzaile eta taldea sortu eta zerbitzua martxan jartzen da.

## Metabase (Docker barruan)
Docker instalatuta dagoela baliatuz, metabase eta postgres kontenedore bana abiatzen dira. Metabase 3001 atakan ezartzen da, 3000 atakan Grafana egotea espero delako.

## Exekuzioa
`` ansible-playbook -i inventory.ini main.yml --ask-become-pass``
