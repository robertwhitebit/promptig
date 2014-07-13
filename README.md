Promptig
==============

Adds current branch/hash to prompt and colors it by current status like untracked files, behind or ahead, merge conflicts, and many more.

### Install

- Clone repository from https://github.com/robertwhitebit/promptig, add  
`source ~/<your_path>/promptig/promptig` to the end of ~/.bashrc (Linux) or ~/.bash_profile (Mac) and adapt the path. (prefered)

or

- Just download promptig and copy the content to the end of ~/.bashrc (Linux) or ~/.bash_profile (Mac).

### List of current features

![alt tag](https://raw.githubusercontent.com/robertwhitebit/promptig/master/readme-preview.png)

### Things you need to know when modifying the code

- Update both, `PS1` in the promptig file and `printPrompt()` in test/tests/testcase.sh for reviews.

- Color codes are terminal dependent. http://www.arwin.net/tech/bash.php#s_1 `Cyan='\e[0;34m'` may not be cyan in your terminal. See color palette (Edit->Profile Preferences->Colors->Palette)

- Do not mix colors and text in functions (see: http://stackoverflow.com/a/6592102)

- Colors need to be escaped in `PS1` explicitly (`PS1=...\[${Cyan}\]...`) but not in `printPrompt()` (`echo -e "...${Cyan}...`)

### How to generate a preview output

- Run `test/test.sh` to see a preview output

### How to add a preview output

- Add a new file to test/tests with file extension `.sh` (e.g. my-ultimate-feature.sh) and make it executeable (`chmod +x my-ultimate-feature.sh`)

- Copy the code from another test file and modify it

- Run `test/test.sh` to see a preview output
