#!/bin/bash
clear
VERT="\\033[1;32m" 
NORMAL="\\033[0;39m" 
ROUGE="\\033[1;31m" 
ROSE="\\033[1;35m" 
BLEU="\\033[1;34m" 
BLANC="\\033[0;02m" 
BLANCLAIR="\\033[1;08m" 
JAUNE="\\033[1;33m" 
CYAN="\\033[1;36m"
VERT="\\033[1;32m"
NORMAL="\\033[0;39m"
ROUGE="\\033[1;31m"
ROSE="\\033[1;35m"
BLEU="\\033[1;34m"
BLANC="\\033[0;02m"
BLANCLAIR="\\033[1;08m"
JAUNE="\\033[1;33m"
CYAN="\\033[1;36m"
echo -e "$ROUGE""Utilisateur FTP ?" "$BLANC"
read nariex
echo -e "$BLEU""Dossier a assigner a l'utilisateur ? /home/" "$BLANC"
read dossier
chown -R nariex:ftpgroup $dossier
pure-pw nariex $nariex -u nariex -g ftpgroup -d $dossier
pure-pw mkdb
exit 0
