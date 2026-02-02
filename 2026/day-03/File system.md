- Directory Navigation 😊

pwd              # Show current directory

ls               # List files

ls -l            # Long listing

ls -a            # Show hidden files

ls -al           # formatted listing with hidden files

cd foldername    # Move into directory

cd ..            # Go up one level

cd ~             # Home directory

- File & Directory Management 😊😊

touch file.txt          # Create empty file

mkdir folder            # Create directory

mkdir -p a/b/c          # Create nested directories

rm file.txt             # Delete file ( Please remeber file extension )

rm -r folder's Name     # Delete directory

cp file1 file2          # Copy file

cp -r dir1 dir2         # Copy directory

mv old new              # Move or rename

rm -f file name         # force remove file

rm -rf directory name   # force remove directory 

cp -r dir1 dir 2        # copy dir1 to dir2 , create dir2 if it does not exit

mv file1 file2          # rename or move file1 to file2 , if file2 is an exsiting directory , move file1 into directory file2

- Viewing File Content 😊😊😊

cat file.txt            # View entire file

less file.txt           # Scrollable view

more file.txt           # Page-by-page view

head file.txt           # First 10 lines

tail file.txt           # Last 10 lines

tail -f file.log        # Live log view


- Permissions & Ownership 😊😊😊😊

ls -l                   # View permissions

chmod 755 file.sh       # Change permissions

chmod +x file.sh        # Make executable

chown user file.txt     # Change owner

chgrp group file.txt    # Change group

( Permission format: r = read, w = write, x = execute ) 


Search & Find 🔍 

find /path -name file.txt      # Find file

locate filename                # Fast search (needs updatedb)

grep "text" file.txt           # Search inside file

grep -r "text" folder/         # Search recursively

- Disk Usage & Space

  df -h                   # Disk space usage
  
du -h                   # Directory size

du -sh folder            # Folder total size

- 🧾 File Info

stat file.txt            # Detailed file info

file file.txt            # File type

- 🔗 Links

ln file linkname         # Hard link

ln -s file symlink       # Soft link


- 🗜️ Compression & Archives

tar -cvf file.tar folder/       # Create tar

tar -xvf file.tar               # Extract tar

tar -czvf file.tar.gz folder/   # Create tar.gz

tar -xzvf file.tar.gz            # Extract tar.gz







