# quick

Quickly load a note you have written.

    quick [note | list V | version]

At least one option must be passed.

    note        : The first unique part or the full name of the note to be loaded.
    list        : List all the stored notes and their location. Obviously you can
                  not have a note called "list".
    V | version : Show the version of the script and some other information.

Default settings and values.

The preset search directories for notes are:

    ${HOME}/.quick
    ${HOME}/bin/.quick
    /usr/local/share/quick

The profile varible `${PAGER}` (if set) will be used to view the notes. If not set
or invalid, then "less" (if found) or "more" will be used.

Limitations and rules.

If there are two notes with the same name in different search directories, the
note in the first directory will be shown. This is helpful if you have a system
wide note but would like to have your own extended or modified version, or just
a completly different one with the same name.

Rules for the notes:

- Must end in ".q"
- Must be a plain text file
- Must be save in a search directory

For example: you could keep track of birthdays in a file called "bdays.q",
saved to one of the search directories. To view the note you would type:

    quick bdays

The following run command file can be used to set a few options.

    ${HOME}/.quick/.quickrc

    Q_PATH      : Set your own search directories.
    Q_PAGER     : Use a different text viewer (for example: vim)


