# Test Creazione applicazione con Symfony

## Requisiti - tecnici
Prima di creare la prima applicazione Symfony accertiamoci che:

*   Sia installa una versione PHP 7.2.5 o versioni successive. 
*   Estensioni PHP (installate e abilitate per impostazione predefinita nella maggior parte delle installazioni PHP 7
    - **Ctype**, **iconv**, **JSON**, **PCRE**, **Session**, **SimpleXML** e **Tokenizer**;
*   Sia installato **Composer**, che viene utilizzato per installare i pacchetti PHP.

*   Opzionalmente, installare **Symfony CLI**. Questo crea un binario chiamato ***symfony*** che fornisce tutti gli strumenti necessari per sviluppare ed eseguire localmente l' applicazione Symfony.

Essa fornisce anche uno strumento per verificare se vengono soddisfa tutti i requisiti. 

Della console eseguire il comando:

    symfony check:requirements

## Step 1

Dopo aver verificato che i prerequisiti per la creazione di un nuovo progetto symfony
 possiamo creare una nuova applicazione Symfony.

Possiamo usare sia la ***Symfony CLI***
        
        # Avvia un'installazione tradizionale 
        symfony new my_project_name --full

        symfony new my_project_name

La differenza tra questi due comandi è il numero di pacchetti installati per impostazione predefinita. L' opzione`--full` installa tutti i pacchetti che di solito servono per creare applicazioni web, quindi la dimensione dell' installazione sarà maggiore.

Se non abbiamo installato la ***Symfony CLI**, possiamo usare direttamente ***Composer***


    composer create-project symfony/website-skeleton my_project_name
        
    composer create-project symfony/skeleton my_project_name

Anche in questo caso possiamo scegliere se installare la versione `website` oppure solo lo `skeleton`.

A questo punto, indifferentemente dall' istruzione impiegata, sarà stata creata la directory `my_project_name`, al cui interno saranno scaricate alcune dipendenze
 e file di base.

Ora possiamo eseguire l' applicazione.

Nel caso si usi un server esterno come Apache o Nginx, essi andranno [configurati per poter eseguire Symfony](https://symfony.com/doc/current/setup/web_server_configuration.html),
 mentre se si è optato per l' installazione della ***Symfony CLI*** possiamo utilizzare il ***web server*** fornito da quest' ultima.

    $ cd my_project_name
    $ symfony server:start
