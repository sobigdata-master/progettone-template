# Boilerplate del Sito Web Progettone

## Istruzioni per l'integrazione del boilerplate del sito web nella cartella del progetto

Le istruzioni seguenti guidano l'integrazione di un boilerplate per un sito web Jekyll all'interno del vostro repository del progettone. Attraverso una serie di passaggi, aggiungeremo il boilerplate dalla repository remota al nostro progetto locale. Questo ci permetterà di avviare il nostro progetto con una struttura base già predefinita, risparmiando tempo e sforzi nella configurazione iniziale.

### The Git Way (consigliata)

1. Accedi alla directory del tuo progetto chiamato "my_progettone" e assicurati che non esista già una cartella chiamata `website` nella radice del progetto. In caso contrario, rinominala prima di procedere:
   - `cd my_progettone`

2. Aggiungi il repository "progettone-template" come remoto al tuo repository "my_progettone":
   - `git remote add progettone-template https://github.com/sobigdata-master/progettone-template`

3. Recupera i file dal repository "progettone-template":
   - `git fetch progettone-template`

4. Imposta "progettone-template" come repository remoto:
   - `git remote set-url origin https://github.com/sobigdata-master/progettone-template.git`

5. Mantieni il file README.md del repository locale e ignora quello remoto (il file che stai leggendo):
   - `git checkout --ours README.md`
   - `git add README.md`
   - `git commit -m "risolto conflitto nel README"`

6. Effettua il merge dei file dal repository "progettone-template" nel tuo repository "my_progettone":
   - `git merge progettone-template/main --allow-unrelated-histories`

7. Esegui il commit dei file aggiunti:
   - `git commit -m "aggiunto boilerplate di base"`

8. Rimuovi il collegamento con il repository "progettone-template" (non più necessario):
   - `git remote remove progettone-template`


### The Manual Way (sconsigliata)

1. Accedi alla directory del tuo progetto chiamato "my_progettone" e assicurati che non esista già una cartella chiamata `website` nella radice del progetto. In caso contrario, rinominala prima di procedere:
   - `cd my_progettone`

2. Scarica da questo repository (progettone-template) la cartella `website` e aggiungila alla root del tuo progettone

3. Fai commit e push dei file appena aggiunti

## La struttura della cartella dovrà essere simile a questa:


my_progettone/

├── code/

├── deliverables/

├── figures/

├── references/

├── *website*/

└── README.md (del tuo progetto locale, non di questo repository)
