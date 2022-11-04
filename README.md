# Useful Commands

## Docker

docker ps -a --format "table \{{.ID\}}\t\{{.Image\}}\t\{{.Command\}}\t\{{.CreatedAt\}}\t\{{.Status\}}\t\{{.Names\}}"

## Iptables

sudo iptables -nvL | cut -f -9 | column -t | sed 's/^Chain/\n&/g' | sed '/^Chain/ s/\[ \t]{1,}/ /g' | sed '/^\[0-9]/ s/\[ \t]{1,}/ /10g'

## Homebrew

brew leaves | xargs brew deps --installed --for-each | sed "s/^.\*:/$(tput setaf 4)&$(tput sgr0)/"
