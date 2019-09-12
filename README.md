# Aspell Personal Dictionaries

[![](https://img.shields.io/github/license/cn-writing/aspell-personal-dictionaries)](https://github.com/cn-writing/aspell-personal-dictionaries)
[![](https://img.shields.io/github/issues/cn-writing/aspell-personal-dictionaries)](https://github.com/cn-writing/aspell-personal-dictionaries)
[![](https://img.shields.io/github/issues-closed/cn-writing/aspell-personal-dictionaries)](https://github.com/cn-writing/aspell-personal-dictionaries)
[![](https://img.shields.io/github/languages/code-size/cn-writing/aspell-personal-dictionaries)](https://github.com/cn-writing/aspell-personal-dictionaries)
[![](https://img.shields.io/github/repo-size/cn-writing/aspell-personal-dictionaries)](https://github.com/cn-writing/aspell-personal-dictionaries)

## Usage for Spanish analysis

1. Download the word_list file.

        wget -O spanish_word_list https://raw.githubusercontent.com/cn-writing/aspell-personal-dictionaries/master/spanish_word_list
    
2. Generate the Aspell dictionary for Spanish adding the word list.

        aspell --lang=es create master ./list.pws < spanish_word_list
    
3. Move the recently created dictionary to the Aspell folder.

        mv list.pws /usr/lib/aspell/
    
4. Add the dictionary to the spanish checks

        echo "add list.pws" >> /usr/lib/aspell/es.multi

5. Use the Aspell command as usual

        aspell --lang=es
