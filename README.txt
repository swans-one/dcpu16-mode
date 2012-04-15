DCPU-16 MODE README

This emacs mode adds basic syntax highlighting and indentation support
for DCPU-16 assembly.

########################
# INSTALLATION AND USE #
########################

To use dcpu16-mode place the file dcpu16-mode.el in your load-path and
add the line

        (require 'dcpu16-mode) 

to your .emacs file. If you don't have a load path set up, you can
create a directory:

        mkdir ~/.emacs.d

And add the line 

        (add-to-list 'load-path "~/.emacs.d/")

to your emacs file, above the require line.

To use the mode, open a DCPU-16 assembly file and invoke 
     
         M-x dcpu16-mode

############
# FEATURES #
############

This major mode includes two things:

1) Syntax Highlighting
2) Indentation Rules

Syntax Highlighting:

Syntax highlighting rules exist for lables, comments, instructions and 
register names.

Indentation Rules:

The indentation rules are fairly simple. Any comment, label or blank
line is not indented. Every instruction is indented 16 spaces.

###############
# LIMITATIONS #
###############

This is a first attempt at creating a major mode, so there might be
some issues. Know issues include:

- Indentation after a label
  
  Currently, if an instruction is on the same line as a label,
  indentation must be done manually by adding spaces.

- Comment highlighting.

  Adding a ';' character at the start of line with existing
  instructions may not change the highlight to be a comment
