UPUTE ZA KORIŠTENJE

PRVI ZADATAK:
Pozicionirate se u direktorij /app
Pokrenete docker sliku sa naredbom:
docker run -p 80:80 -d b4577f412105


DRUGI ZADATAK:
Pozicionirate se u direktorij /opt/run/webphp
Pokrenete ansible playbook sa naredbom:
ansible-playbook playbook4.yml

TREĆI ZADATAK:
Pokrenete tcpdump sa naredbom:
tcpdump port 80 -w capture_file
Otvorite drugu konzolu i spojite se sa ssh na stroj.
Pokrenete naredbu:
curl localhost
