# bash-oneliners
Μy one-liner bash commands

# Print your aliases
cat ~/.bash_aliases | sort -d | cut -d'=' -f1 | cut -c7- | column

# Free up memory
sudo sync && sudo echo 3 | sudo tee /proc/sys/vm/drop_caches

# Easy update (debian)
sudo apt-get update && sudo apt-get upgrade -y && sudo apt-get dist-upgrade -y && sudo apt-get autoremove -y && sudo apt-get clean -y && sudo apt-get autoclean -y && sudo apt-get purge -y

# Greek nameday (Ποιός γιορτάζει σήμερα)
curl -s -m 10 "http://www.greeknamedays.gr/tools/eortologiorssfeed/index.php?langid=gr" | sed -n 23p | sed -e 's/<[a-zA-Z\/][^>]*>//g' | sed -e 's/^[ \t]*//'
