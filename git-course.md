# Corso git

<!-- TOC -->
* [Corso git](#corso-git)
  * [01 git init](#01-git-init)
  * [02 git clone](#02-git-clone)
  * [03 git status](#03-git-status)
<!-- TOC -->

## 01 git init

* [Scarica il progetto da qui](01-git-init/01-git-init.zip)
* Scompatta il progetto con [windows esplora risorse](https://support.microsoft.com/it-it/windows/comprimere-e-decomprimere-file-f6dde0a7-0fec-8294-e1d3-703ed85e7ebc), [7z](https://www.7-zip.org/download.html) o [tramite terminale (unzip)](https://linux.die.net/man/1/unzip) 
* Entra nella cartella `01-git-init`, contiente lo scheletro di un progetto java
* Apri [git bash](https://gitforwindows.org/) o il tuo terminale preferito :computer: [nella cartella](https://www.toolsqa.com/git/common-directory-commands-on-git-bash/#:~:text=Open%20Git%20Bash%20directly%20in%20the%20folder&text=For%20this%2C%20go%20to%20the,%3D%3E%20Open%20Git%20Bash%20here.)
* Digita `git init`
* Hai inizializzato il tuo primo repository! :partying_face:

Digita `ls -a` o apri esplora risorse, noterai che c'è una :new: nuova cartella `.git`
![git init](images/git-init.png)   
Questa conterrà tutte le informazioni necessarie per versionare il nostro repository.


## 02 git clone

* Andiamo ad aprire [questo repository github](https://github.com/ikatyang/emoji-cheat-sheet.git) :globe_with_meridians:
* Apriamo esplora risorse in una nuova cartella
* Apriamo git bash in questa cartella :computer:
* Digitiamo `git clone https://github.com/ikatyang/emoji-cheat-sheet.git`
* Ora abbiamo scaricato lo stesso progetto che abbiamo aperto poco fa sul browser

Se entriamo nella cartella `emoji-cheat-sheet`, notiamo come prima cosa che c'è già una cartella `.git`.   
Ciò significa che questo progetto è stato precedentemente inizializzato con `git init` e poi reso disponibile online.   

Dunque non ci sarà bisogno di dover inizializzare manualmente questo progetto come nella sezione precedente.

## 03 git status

* Apriamo il progetto precedento scaricato
* Apriamo git bash :computer:
* Digitiamo `git status`
![git status](images/git-status.png)
  * Ci da subito 3 informazioni   
  :one: Il branch in cui siamo `master`    
  :two: Il nostro branch è allineato con `origin/master`    
  :three: Non abbiamo nulla da aggiungere `nothing to commit, working tree clean`    


