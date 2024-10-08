# quick

Quickly load a note you have written.

    quick [note | l | list | V | version]

At least one option must be passed.

    note        : The first unique part or the full name of the note to be loaded.
    l | list    : List all the stored notes and their location.
    V | version : Show the version of the script and some other information.
 
The preset search directories for notes are:

    ${HOME}/.quick
    ${HOME}/bin/.quick
    /usr/local/share/quick

The profile varaible `${PAGER}` (if set) will be used to view the notes. If not
set or invalid, then `less` (if found) or `more` will be used.

Limitations and rules.

If there are two notes with the same name in different search directories, the
note in the first directory will be shown. This is helpful if you have a system
wide note but would like to have your own extended or modified version, or just
a completly different one with the same name.
 
Rules for the notes:
 
    Must end in ".q"
    Must be a plain text file
    Must be saved in a search directory
 
For example: you could keep track of birthdays in a file called "bdays.q", saved
to one of the search directories. To view the note you would type:
 
    quick bdays

In the example above, if "bdays.q" did not exist you will be asked if you
would like to create a new note. The file will be saved to first directory in
your search lists.

The following run command file can be edited to set a few options.
 
    ${HOME}/.quick/.quickrc

The options that can be set in the run command file are:

    Q_EDITOR  : Set an editor for new notes. Defaults to `vim` then `vi`.
    Q_PAGER   : Use a different text viewer. For example: `vim`.
    Q_PATH    : Set your own search directories.

The following note names will clash with the command line options. For this
reason you can not have a note with these names and filenames:

    l         : l.q
    list      : list.q
    V         : V.q
    version   : version.q


