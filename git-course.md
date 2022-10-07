# Corso git

## Indice

<!-- TOC -->

* [Corso git](#corso-git)
    * [Indice](#indice)
    * [01 git init](#01-git-init)
    * [02 git clone](#02-git-clone)
    * [03 git status](#03-git-status)
        * [Stati possibili](#stati-possibili)
            * [Unmodified](#unmodified)
            * [Modified](#modified)
            * [Untracked](#untracked)
    * [04 git add](#04-git-add)
    * [05 git commit](#05-git-commit)

<!-- TOC -->

## 01 git init

* [Scarica il progetto da qui](01-git-init/01-git-init.zip)
* Scompatta il progetto
  con [windows esplora risorse](https://support.microsoft.com/it-it/windows/comprimere-e-decomprimere-file-f6dde0a7-0fec-8294-e1d3-703ed85e7ebc)
  , [7z](https://www.7-zip.org/download.html) o [tramite terminale (unzip)](https://linux.die.net/man/1/unzip)
* Entra nella cartella `01-git-init`, contiente lo scheletro di un progetto java
* Apri [git bash](https://gitforwindows.org/) o il tuo terminale preferito :
  computer: [nella cartella](https://www.toolsqa.com/git/common-directory-commands-on-git-bash/#:~:text=Open%20Git%20Bash%20directly%20in%20the%20folder&text=For%20this%2C%20go%20to%20the,%3D%3E%20Open%20Git%20Bash%20here.)
* Digita `git init`
* Hai inizializzato il tuo primo repository! :partying_face:

Digita `ls -a` o apri esplora risorse, noterai che c'è una :new: nuova cartella `.git`    
![git init](images/git-init.png)   
Questa conterrà tutte le informazioni necessarie per versionare il nostro repository.

[:arrow_up: indice](#indice) - [prossima sezione :arrow_heading_down:](#02-git-clone)

## 02 git clone

* Andiamo ad aprire [questo repository GitHub](https://github.com/dc-zerob/01-git-init) :globe_with_meridians:
* Apriamo esplora risorse in una nuova cartella
* Apriamo git bash in questa cartella :computer:
* Digitiamo `git clone https://github.com/ikatyang/emoji-cheat-sheet.git`
* Ora abbiamo scaricato lo stesso progetto che abbiamo aperto poco fa sul browser

Se entriamo nella cartella `emoji-cheat-sheet`, notiamo come prima cosa che c'è già una cartella `.git`.   
Ciò significa che questo progetto è stato precedentemente inizializzato con `git init` e poi reso disponibile online.

Dunque non ci sarà bisogno di dover inizializzare manualmente questo progetto come
spiegato [nella sezione precedente](#01-git-init)).

[:arrow_up: indice](#indice) - [prossima sezione :arrow_heading_down:](#03-git-status)

## 03 git status

* Apriamo il progetto [precedentemente scaricato](#02-git-clone)
* Apriamo git bash :computer:
* Digitiamo `git status`
  ![git status](images/git-status.png)

Ci da subito 3 informazioni   
:one: Il branch in cui siamo `master`    
:two: Il nostro branch è allineato con `origin/master`    
:three: Non abbiamo nulla da aggiungere `nothing to commit, working tree clean`

### Stati possibili

![git-status-lifecycle.png](images/git-status-lifecycle.png)

#### Unmodified

Al momento siamo nello stato `Unmodified`, non abbiamo modificato e non abbiamo aggiunto file.

#### Modified

* Apriamo il file :pencil: `README.MD` e modifichiamo il titolo
* Salviamo il file :floppy_disk:
* Digitiamo `git status`, ora siamo nello stato `Modified`
  ![git-status-modified.png](images/git-status-modified.png)

#### Untracked

* Aggiungiamo un nuovo file digitando `touch test.txt` nel terminale
* Verifichiamo con `git status`
  ![git-status-untracked.png](images/git-status-untracked.png)    
  Come notiamo dall'immagine, abbiamo il file precedente `README.MD` in stato _Modified_ e il nostro nuovo
  file `test.txt` in stato _Untracked_.     
  Dunque, git ci sta dicendo che il file `test.txt` non è versionato nel repository e non terrà traccia delle modifiche.

[:arrow_up: indice](#indice) - [prossima sezione :arrow_heading_down:](#04-git-add)

## 04 git add

Andiamo ad aggiungere il file `test.txt` in stato _Untracked_ al repository git.

* Digitiamo `git add test.txt`
* Controlliamo con `git status`
  ![git-add.png](images/git-add.png)

Leggendo la console, git ci comunica che il file è pronto per essere committato (nella sezione _Changes to be
committed_) e viene dichiarato da git come nuovo (_new file_).    
Questo perchè stiamo aggiungendo un file che non era presente nel repository.

Proviamo a modificare il file:

* Apriamo il file :pencil: `test.txt` e scriviamo `test`
* Salviamo il file :floppy_disk:
* Facciamo una verifica con :computer: `git status`
  ![git-add-file-modified.png](images/git-add-file-modified.png)

Troviamo il nostro file in due punti:

1. _Changes to be committed_
2. _Changes not staged for commit_

Questo perchè git traccia la versione del file precedente alla nostra modifica.   
Se vogliamo aggiungere le modifiche appena salvate, bisognerà digitare nuovamente `git add test.txt`

![git-add-modified-add.png](images/git-add-modified-add.png)

Ora abbiamo un solo file sotto la voce _Changes to be committed_, che include le nostre modifiche.

[:arrow_up: indice](#indice) - [prossima sezione :arrow_heading_down:](#05-git-commit)

## 05 git commit

Siamo pronti per versionare le nostre modifiche e dunque fare il nostro primo commit.

* Digitiamo  :computer: `git commit -m "aggiunto file di test"`
    * Tramite il flag `-m` andiamo a scrivere il messaggio per il nostro commit
* Verifichiamo con git status
  ![git-commit.png](images/git-commit.png)

Ora siamo
