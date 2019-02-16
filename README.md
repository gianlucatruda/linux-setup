# Linux Setup Files

Some quick setup files for basic Linux sessions (e.g. AWS instances / virtual machines / Raspberry Pis)

## Add this to .bash_profile

```bash
# Load aliases
if [ -f ~/.bash_aliases ]; then
    . ~/.bash_aliases
fi

if [ -f ~/.bash_prompt ]; then
    . ~/.bash_prompt
fi

# Enable tab completion for `g` by marking it as an alias for `git`
if type _git &> /dev/null && [ -f ~/.git-completion.bash ]; then
    complete -o default -o nospace -F _git g;
fi;

```
