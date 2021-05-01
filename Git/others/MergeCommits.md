##
1. Откроется текстовый редактор, в котором первые две строки соответствуют последним двум коммитам:

    > pick ab37583 Added feature 1.
    >
    > pick 3ab2b83 Added feature 2.
    >
    > Rebase e46d230..3ab2b83 onto e46d230 (2 commands)
    >
    > Commands:
    >
    >
    > p, pick = use commit
    >
    > r, reword = use commit, but edit the commit message
    >
    > e, edit = use commit, but stop for amending
    >
    > s, squash = use commit, but meld into previous commit

2. В начале каждой строки стоит слово pick. Вам необходимо изменить слово pick на squash или просто на букву s у второй строки. Это означает, что данный коммит будет объединен с предыдущим коммитом. Итак, замените pick на s, у вас должно получиться что-то вроде:

    > pick ab37583 Added feature 1.
    > s 3ab2b83 Added feature 2.

3. Сохраните изменения и закройте редактор.
4. Снова откроется редактор, в котором вам предлагается ввести сообщение к коммиту, который и является объединением двух коммитов:

    >  This is a combination of 2 commits.
    >  This is the 1st commit message:
    > 
    > Added feature 1.
    > 
    >  This is the commit message #2:
    > 
    > Added feature 2.
    > 
    >  Please enter the commit message for your changes. Lines starting
    >  with '#' will be ignored, and an empty message aborts the commit.

5. Отредактируйте сообщение к коммиту, сохраните изменения, и закройте редактор.

6. В результате вы получите коммит, который был объединен из двух последних коммитов.