#rust-gedit

Instructions for syntax highlighting for Rust in gedit (GtkSourceView 3).

1. Run the following command:

  > git clone https://github.com/rust-lang/gedit-config

2. Close all instances of gedit

3. Obtain super-user access

4. Copy the rust.lang file and place it in /usr/share/gtksourceview-3.0/language-specs/

Example (after extracting the gedit-config-master.zip to the ~/Downloads directory):

  > sudo mv /Downloads/gedit-config/share/gtksourceview-3.0/language-specs/rust.lang /usr/share/gtksourceview-3.0/language-specs/
