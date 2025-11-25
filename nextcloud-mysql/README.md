
### Note importanti

Cartelle host personalizzate

/mnt/dati/nextcloud → tutti i file di Nextcloud

/mnt/dati/mysql → database MySQL/MariaDB

Puoi cambiarle in qualsiasi percorso del tuo disco o disco esterno, tipo D:\Nextcloud su Windows.

Redis serve solo per velocizzare Nextcloud e gestione cache. Puoi anche rimuoverlo se vuoi una configurazione più semplice.

Backup semplice
Basta copiare le due cartelle host:

cp -r /mnt/dati/nextcloud /backup/nextcloud
cp -r /mnt/dati/mysql /backup/mysql


### Oppure puoi fare un .tar:

 - tar czvf nextcloud_data.tar.gz /mnt/dati/nextcloud
 - tar czvf nextcloud_db.tar.gz /mnt/dati/mysql


Avvio:
 - docker compose up -d


Poi accedi via browser a http://localhost:8080 e configuri l’utente admin.
