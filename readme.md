# TP Redis

Ce TP Redis avec Docker.

## Étapes à suivre

### 1. Installation de Redis avec Docker
- **Installation de Redis avec Docker** : Lancez la commande suivante :
    ```bash
    docker pull redis
    ```
- **Démarrage du conteneur** : Utilisez la commande suivante pour démarrer le conteneur :
    ```bash
    docker run --name redis-tp -d redis
    ```
- **Connexion au conteneur redis-tp** : Pour pouvoir intéragir avec mon conteneur et faire des opérations
    ```bash
    docker exec -it redis-tp redis-cli
    ```
![Capture de l'exécution de mon code](basicCommand.png)
- **Basic Create & Read String** : Pour pouvoir intéragir avec mon conteneur et faire des opérations
    ```bash
    Set user
    Set mail
    Set age
    Mget user mail age
    HMSET user:1 name "Alice" age 30 email "alice@example.com"
    ```
![Capture de l'exécution de mon code](createRead.png)

- **Basic Create, Read, Delete List** : Pour pouvoir intéragir avec mon conteneur et faire des opérations
    ```bash
    LPUSH fruits "Pomme" "Raisin"
    RPUSH fruits "Framboise" "Orange"
    LPOP fruits    
    RPOP fruits
    LREM fruits 1 "Raisin"    
    ```
![Capture de l'exécution de mon code](List.png)
- **Basic Create, Read, Delete Sets** : Pour pouvoir intéragir avec mon conteneur et faire des opérations
    ```bash
    ZADD scores 10 "player1" 20 "player2" 30 "player3"
    ZINCRBY scores 5 "player1"
    ZRANGE scores 0 -1   
    ZRANGEBYSCORE scores 10 20 
    ZREM scores "player1"   
    ZREMRANGEBYRANK scores 0 1
    ZREMRANGEBYSCORE scores 10 20 
    ```
![Capture de l'exécution de mon code](players.png)
