# XINT

This is a text based game. Everything is in some text format, including json.

Everything can be viewed and solved using a bash terminal. But feel free to do however you like.

Read this document carefully. Statements here might be assumptions elsewhere.

## Todos

Tasks to be solved can be found in

    todo.txt

The solutions are most of the time passwords, tokens or flags.

Flags looks like this:

    xint{some_relevant_content}

## Wiki

The wiki might contain techniques, examples and other relevant information. So if you get stuck, look in the wiki.

If you are still stuck or have questions or feedback feel free to write to me on salza@salza.dk.

## Terminal

In all documentation I will assume `XINT_HOME` points to the root of the XINT project (The folder containing this document). This is not a requirement. You still do however you like. It is just a convience allowing for documenting specific file location.

In my own case I would write:

    XINT=~/proj/xint

Adjust to your needs. If done right this command will now work for anyone:

    alias encrypt=$XINT/scripts/encrypt
    alias decrypt=$XINT/scripts/decrypt

Allowing easy commands like

    echo "Some important secret" | encrypt 1234
    echo "Jgf8 9eiiil3hk k76i6m" | decrypt 1234

## Language agnostic

Except for a few bash scripts, everything in this "game" is language agnostic. You can use whatever scripting/programming language you want. Or no language at all.

The few bash scripts are located in scripts. They are documented in `$XINT_HOME/wiki`. Using just the scripts or scripts and documentation, some AI will have no problem creating Python, Nodejs, Java, Clojure variants of the scripts.

In the samples, other bash tools might also be used, like `jq` to extract information from JSON. I recommend installing it or use similar libraries for Python, NodeJS, etc.


