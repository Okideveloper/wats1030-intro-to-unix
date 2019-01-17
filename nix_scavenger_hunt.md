# *nix Scavenger Hunt

Complete the following challenges using the command-line interface on your favorite
Unix or Linux operating system. You are welcome and encouraged to consult any
additional documentation online or in books.

Please add your answers/responses/text pastes to the document after each prompt.

Note: For some of the challenges you will need to reference files included with
this repository, so you will need to fork the repo into your own Github account
and then clone it to your development environment.

## The Challenges

### Navigating the Filesystem

* Get an idea of where you are in the operating system. Use the `pwd` command to find your "path to working directory"--your current location in the filesystem of your devbox. *Paste the output of the `pwd` command here:*

/Users/amanda/wats3020/wats3030/wats1030-intro-to-unix

* Discover more about this filesystem. Use `ls` (the "list" command)to see what is in this directory. *What directories and files do you see when you run `ls`?*

Applications                    Downloads                       Pictures                        WATS3030-Servers and Hosting
Creative Cloud Files            Library                         Public                          wats3020
Desktop                         Movies                          WATS3020-JS
Documents                       Music                           WATS3030

* You can use *options* to modify how a command runs. Try using `ls -alh` to see the contents of your current directory. *How are the results different when you use the `-alh` options?*
it provides motifies dates and times withthe number of files in each folder.

total 80
drwxr-xr-x+  26 amanda  staff   832B Jan 15 13:59 .
drwxr-xr-x    7 root    admin   224B Nov  4 11:07 ..
-r--------    1 amanda  staff     7B Jun 24  2017 .CFUserTextEncoding
-rw-r--r--@   1 amanda  staff    16K Jan 15 13:53 .DS_Store
drwx------  154 amanda  staff   4.8K Jan 15 13:55 .Trash
-rw-------    1 amanda  staff   4.2K Jan 15 13:13 .bash_history
drwx------   29 amanda  staff   928B Jan 13 12:26 .bash_sessions
-rw-r--r--    1 amanda  staff   173B Nov 20 19:48 .gitconfig
drwxr-xr-x    3 amanda  staff    96B Feb 19  2018 .kodi
drwx------    5 amanda  staff   160B Jan  8 09:52 .ssh
-rw-------    1 amanda  staff   3.9K Jan 11 16:05 .viminfo
drwxr-xr-x    3 amanda  staff    96B Nov 20 19:50 .vscode
drwx------@   3 amanda  staff    96B Jul 10  2017 Applications
drwxrwxr-x@   3 amanda  staff    96B Dec 19 18:52 Creative Cloud Files
drwx------@  28 amanda  staff   896B Jan 15 13:56 Desktop
drwx------@   4 amanda  staff   128B Jan 14 06:22 Documents
drwx------+  67 amanda  staff   2.1K Jan 10 18:39 Downloads
drwx------@  75 amanda  staff   2.3K Jan  4 17:41 Library
drwx------+   4 amanda  staff   128B Oct 30 16:01 Movies
drwx------+   4 amanda  staff   128B Jun 29  2017 Music
drwx------+   3 amanda  staff    96B Jun 24  2017 Pictures
drwxr-xr-x+   5 amanda  staff   160B Jun 24  2017 Public
drwxr-xr-x    5 amanda  staff   160B Jan 15 13:07 WATS3020-JS
drwxr-xr-x    4 amanda  staff   128B Jan 15 13:55 WATS3030
drwxr-xr-x    3 amanda  staff    96B Jan 15 13:59 WATS3030-Servers and Hosting
drwxr-xr-x    3 amanda  staff    96B Jan 15 13:11 wats3020

* The `man` ("manual") command tells you more about how any given command works. (*WARNING:* CodeAnywhere does not support the man command. You can click the following link to complete this task: http://man.he.net/). Run `man` to see instructions about how to use `man`. Then use `man` to learn what the `a`, `l`, and `h` options mean when used with the `ls` command. *Write down what those options do?*

ls -a

.                               .gitconfig                      Desktop                         Public
..                              .kodi                           Documents                       WATS3020-JS
.CFUserTextEncoding             .ssh                            Downloads                       WATS3030
.DS_Store                       .viminfo                        Library                         WATS3030-Servers and Hosting
.Trash                          .vscode                         Movies                          wats3020
.bash_history                   Applications                    Music
.bash_sessions                  Creative Cloud Files            Pictures

ls -l

total 0
drwx------@  3 amanda  staff    96 Jul 10  2017 Applications
drwxrwxr-x@  3 amanda  staff    96 Dec 19 18:52 Creative Cloud Files
drwx------@ 28 amanda  staff   896 Jan 15 13:56 Desktop
drwx------@  4 amanda  staff   128 Jan 14 06:22 Documents
drwx------+ 67 amanda  staff  2144 Jan 10 18:39 Downloads
drwx------@ 75 amanda  staff  2400 Jan  4 17:41 Library
drwx------+  4 amanda  staff   128 Oct 30 16:01 Movies
drwx------+  4 amanda  staff   128 Jun 29  2017 Music
drwx------+  3 amanda  staff    96 Jun 24  2017 Pictures
drwxr-xr-x+  5 amanda  staff   160 Jun 24  2017 Public
drwxr-xr-x   5 amanda  staff   160 Jan 15 13:07 WATS3020-JS
drwxr-xr-x   4 amanda  staff   128 Jan 15 13:55 WATS3030
drwxr-xr-x   3 amanda  staff    96 Jan 15 13:59 WATS3030-Servers and Hosting
drwxr-xr-x   3 amanda  staff    96 Jan 15 13:11 wats3020

ls -h

Applications                    Downloads                       Pictures                        WATS3030-Servers and Hosting
Creative Cloud Files            Library                         Public                          wats3020
Desktop                         Movies                          WATS3020-JS
Documents                       Music                           WATS3030

* Commands can also take *arguments*, which are usually the names of files or locations that you want the command to work with. Try running `ls /` to see what files are in the *root* directory of the filesystem. *What files and directories do you see listed?*

Applications                    Volumes                         home                            tmp
Library                         bin                             installer.failurerequests       usr
Network                         cores                           net                             var
System                          dev                             private
Users                           etc                             sbin

* A Unix filesystem has a few special shortcuts to refer to specific locations. `/` indicates the *root* of the filesystem, meaning the top-most directory in the filesystem hierarchy. Use the `cd` ("change directory") command to move to the root directory. (Hint: Use `man` to look up the `cd` command if you have any issues) *Then run `pwd` and paste the output here:*

Amandas-MacBook-Pro:~ amanda$ pwd
/Users/amanda

* Another special shortcut in Unix is the `~` location. This indicates the *user root* directory, meaning the top-most directory in the hierarchy that comes below your user account. Use `cd` to move to `~`. *Run `pwd` and paste the response here:*
Amandas-MacBook-Pro:~ amanda$ cd ~
Amandas-MacBook-Pro:~ amanda$ cd /users/amanda
Amandas-MacBook-Pro:amanda amanda$ pwd
/users/amanda


* Change directory into the `challenge_files` directory. Use `ls` to find only the files with a `.demo` pattern. *How many files do you find?*
2

* Use the `cd` command to move "up" one directory. *Where are you in the filesystem now?*
From challenge_files to my assignment folder. I went back a one.

* Press the up arrow on your keyboard. *What just happened?*
cd ~
* Press the up arrow a few more times. *What do you see?*
It's changing commands such as ls -alh, ls, pwd, etc

* Run the `history` command. *What do you see?*
It gives the history of all my past commands. It is ALOT
!!!

### Observing the System

* Discover what account you are logged into using the `whoami` command. *What username are you currently using?*
amanda

* Discover who else is on your system with the `who` command. *Are any other users using your system? If so, list them here:*
No other users. Here is the list
amanda   console  Dec 19 18:51
amanda   ttys003  Jan 13 12:26

* How long has your system been running? Use `uptime` to see, and *paste the result here:*
15:29  up 27 days, 18:27, 2 users, load averages: 1.47 1.45 1.33

* Run `ps aux` and review the results. (Hint: Use `man` to learn more about the `ps` command and options.) *How do you interpret what you see here?*
It gives detailed times and dates when users have portals open. 

* Run `top` and review the results. (Hint: You may need to use `ctrl-c` to get out of this app.) *How do you interpret what you see here?*
It shows what my processor is doing in current time. Also shows the memory. I see the time going in google chrome, which is my current browser. ctrl-c did work!

### Finding and Viewing Files

* Make sure you are in the `challenge_files` directory. Use the `*` wildcard to find all the files that have the word "credit" in the filename. *How many files did you find?*
./credit_cards2.txt
./credit_cards.txt

* Use the `more` command to view one of the `credit_cards` files you just discovered. (Hint: Type `q` to quit viewing the file. Press the `spacebar` to page down. Use your keyboard arrows to move up/down.) *What is the date in the file you have viewed?*
01-15-2015

* Use the `find` command to search for files more effectively. Search the sub-directories under `challenge_files` to find the location of the file named `modi_laboriosam.txt`. *Where is that file located?*
./tmp/modi_laboriosam.txt

* Use the `grep` command to search for text within a file. Use `grep` on all the `.user` files in `challenge_files` to find which files contain "WA" (the abbreviation for Washington state). *How many files did you find?*
1

* Use the `-r` option of `grep` to *recursively* find the text "Waldo" hidden in a file somewhere under the `challenge_files` directory. *Paste the result showing the file and line where the word "Waldo" shows up.*
./serial-numbers/eaque_molestiae.txt:Ut est maiores quia autem. Nisi modi Waldo sed corporis sit explicabo ut est. Et est placeat ea sunt sunt consectetur sunt incidunt. Explicabo vel esse blanditiis dolorem culpa non quia.

### Pipes and Connecting Commands

* Sometimes it's useful to output the results of a command to a text file for further analysis, reference, or processing. Try running `ls > files.txt`. Notice that the file `files.txt` was created. View that file using `more`. *What do you see in the `files.txt` file?*

01
2015_special_stuff.demo
Afton-Jast.user
Aimee-Maggio.user
Alfonso-Gottlieb.user
Allen-Kemmer.user
Almina-Cormier.user
Alta-Lemke.user
Amina-McGlynn.user
Anabel-Hammes.user
Ancel-Conn.user
Anjali-Halvorson.user
Ardath-Kuvalis.user
Avah-Dickinson.user
Ayaan-Stiedemann.user
Aylin-Grant.user
Bedford-Sipes.user
Benita-King.user
Benito-Stoltenberg.user
Beverlee-Moen.user
Brad-Thiel.user
Brayan-Douglas.user
Bria-Satterfield.user
Bridgette-Reichel.user
Britt-Erdman.user
Britta-Hammes.user
Bryant-Kuhic.user
Bryton-Aufderhar.user
Caitlin-Grady.user
Carroll-Hartmann.user
Claudie-McClure.user
Clemente-Haley.user
Cleo-VonRueden.user
Codie-Romaguera.user
Cooper-Reynolds.user
Corrie-Bogisich.user
Dannielle-Green.user
Deedee-Jacobson.user
Desiree-Marks.user
Deven-Rutherford.user
Doyle-Jones.user
Dustyn-O'Connell.user
Elza-Mraz.user
Emory-Crona.user
Erin-Walker.user
Estela-Schultz.user
Fernanda-Tromp.user
Fletcher-Rice.user
Fred-Ryan.user
Genie-Abshire.user
Grace-Tromp.user
Grant-Cronin.user
Hali-Roob.user
Harland-Schoen.user
Harrell-Quitzon.user
Hillard-Ziemann.user
Isadora-Leffler.user
Jaxen-Gleichner.user
Jayme-Rodriguez.user
Jenni-O'Connell.user
Johny-Borer.user
Kassandra-Barrows.user
Keely-Hilpert.user
Kenyatta-Hickle.user
Kiana-Kulas.user
Kirstin-Hoppe.user
Kwame-Schmitt.user
Ladonna-Lueilwitz.user
Lala-Will.user
Leia-Hudson.user
Leia-Ziemann.user
Lillard-Purdy.user
Lilly-Kohler.user
Lissie-Strosin.user
Mannie-Ritchie.user
Masako-Lind.user
Melisa-Yundt.user
Michelina-Kuphal.user
Minnie-Jacobi.user
Murdock-Leffler.user
Mychal-Corkery.user
Nakita-Nader.user
Nayely-Dare.user
Nicholas-Strosin.user
Niles-Runte.user
Nina-Sporer.user
Noreta-Steuber.user
Ovid-Bogan.user
Randell-Sauer.user
Remy-Renner.user
Ronna-Hermann.user
Rosalind-Wisozk.user
Rosena-Simonis.user
Sandie-Balistreri.user
Sharen-Hansen.user
Sherrill-Russel.user
Sherwin-Kovacek.user
Sherwood-Rath.user
Shyheim-Murazik.user
Siobhan-Kirlin.user
Tomas-Kutch.user
cloaked-wookie.demo
credit_cards.txt
credit_cards2.txt
files.txt
scooter-double-mamba.demo
serial-numbers
test2
tmp
wow



* Notice that if you run `ls -alh` in the `challenge_files` directory, the files scroll by very quickly. Sometimes it would be better to get the results in a paginated format. Try running `ls -alh | more`. *Describe what you see when you run `ls -alh | more`.*

It provides information with my user name amanda of a long list of files with the dates and dates I have visited the challange folder. 

* Earlier, when you viewed the list of active processes on your devbox using `ps aux`, the list was probably really long. You can make this list more manageable by using the pipe (`|`) to filter the results of `ps` using `grep`. Run `ps aux | grep <your_username>` to see what processes are running for your specific user. *Paste the list of processes that reference your username here:* 

This is a LONG LIST!!!

amanda           22407   6.3  1.2  5009592 200012   ??  S     1:41PM   0:27.15 /Applications/Google Chrome.app/Contents/Versions/71.0.3578.98/Google Chrome Helper.app/Contents/MacOS/Google Chrome Helper --type=renderer --field-trial-handle=18050009161147368515,12073003594094258993,131072 --service-pipe-token=14628171943056833893 --lang=en-US --metrics-client-id=c4c85bd6-057c-4022-b575-d3dbada7fab5 --enable-offline-auto-reload --enable-offline-auto-reload-visible-only --num-raster-threads=4 --enable-zero-copy --enable-gpu-memory-buffer-compositor-resources --enable-main-frame-before-activation --service-request-channel-token=14628171943056833893 --renderer-client-id=3210 --no-v8-untrusted-code-mitigations --seatbelt-client=265
amanda           22406   4.7  1.2  5092480 195332   ??  S     1:41PM   0:25.16 /Applications/Google Chrome.app/Contents/Versions/71.0.3578.98/Google Chrome Helper.app/Contents/MacOS/Google Chrome Helper --type=renderer --field-trial-handle=18050009161147368515,12073003594094258993,131072 --service-pipe-token=6550724132501203213 --lang=en-US --metrics-client-id=c4c85bd6-057c-4022-b575-d3dbada7fab5 --enable-offline-auto-reload --enable-offline-auto-reload-visible-only --num-raster-threads=4 --enable-zero-copy --enable-gpu-memory-buffer-compositor-resources --enable-main-frame-before-activation --service-request-channel-token=6550724132501203213 --renderer-client-id=3209 --no-v8-untrusted-code-mitigations --seatbelt-client=234
amanda           22232   3.2  1.5  6194076 254100   ??  R     1:16PM   1:12.81 /private/var/folders/99/pccf2f9x1gz2y99n3m6hbdg40000gn/T/AppTranslocation/76BB7FC3-740A-4B11-BA03-58E8DE438C57/d/Visual Studio Code.app/Contents/Frameworks/Code Helper.app/Contents/MacOS/Code Helper --type=renderer --js-flags=--nolazy --disable-mojo-local-storage --no-sandbox --disable-features=ColorCorrectRendering --service-pipe-token=649D0746971214957BCBB55C3E0EDD87 --lang=en-US --app-path=/private/var/folders/99/pccf2f9x1gz2y99n3m6hbdg40000gn/T/AppTranslocation/76BB7FC3-740A-4B11-BA03-58E8DE438C57/d/Visual Studio Code.app/Contents/Resources/app --node-integration=true --webview-tag=true --no-sandbox --background-color=#171717 --context-id=1 --enable-pinch --num-raster-threads=4 --enable-zero-copy --enable-gpu-memory-buffer-compositor-resources --enable-main-frame-before-activation --content-image-texture-target=0,0,3553;0,1,3553;0,2,3553;0,3,3553;0,4,3553;0,5,3553;0,6,3553;0,7,3553;0,8,3553;0,9,3553;0,10,3553;0,11,34037;0,12,34037;0,13,34037;0,14,3553;0,15,3553;0,16,3553;0,17,3553;1,0,3553;1,1,3553;1,2,3553;1,3,3553;1,4,3553;1,5,3553;1,6,3553;1,7,3553;1,8,3553;1,9,3553;1,10,3553;1,11,34037;1,12,34037;1,13,34037;1,14,3553;1,15,3553;1,16,3553;1,17,3553;2,0,3553;2,1,3553;2,2,3553;2,3,3553;2,4,3553;2,5,3553;2,6,3553;2,7,3553;2,8,3553;2,9,3553;2,10,3553;2,11,34037;2,12,34037;2,13,34037;2,14,3553;2,15,3553;2,16,3553;2,17,3553;3,0,3553;3,1,3553;3,2,3553;3,3,3553;3,4,3553;3,5,34037;3,6,3553;3,7,3553;3,8,3553;3,9,3553;3,10,3553;3,11,3553;3,12,3553;3,13,34037;3,14,34037;3,15,3553;3,16,34037;3,17,34037;4,0,3553;4,1,3553;4,2,3553;4,3,3553;4,4,3553;4,5,34037;4,6,3553;4,7,3553;4,8,3553;4,9,3553;4,10,3553;4,11,3553;4,12,3553;4,13,34037;4,14,34037;4,15,3553;4,16,34037;4,17,34037 --enable-gpu-async-worker-context --service-request-channel-token=649D0746971214957BCBB55C3E0EDD87 --renderer-client-id=57
amanda             812   1.9  2.4  5720500 402372   ??  S    19Dec18 286:13.52 /Applications/Google Chrome.app/Contents/MacOS/Google Chrome -psn_0_237626
amanda             939   1.2  0.8  5379520 139132   ??  S    19Dec18  69:45.44 /Library/Application Support/Adobe/Adobe Desktop Common/HEX/Adobe CEF Helper.app/Contents/MacOS/Adobe CEF Helper --type=renderer --disable-features=AsyncWheelEvents,TouchpadAndWheelScrollLatching --service-pipe-token=74376DD9A9533D49A41C80D7463FC95A --lang=en-US --log-file=/Users/amanda/Library/Logs/CreativeCloud/ACC/CEF.log --log-severity=warning --user-agent=Mozilla/5.0 (Macintosh) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/57.0.2987.98 Safari/537.36 CreativeCloud/4.7.0.400 --num-raster-threads=4 --enable-zero-copy --enable-gpu-memory-buffer-compositor-resources --enable-main-frame-before-activation --service-request-channel-token=74376DD9A9533D49A41C80D7463FC95A --renderer-client-id=3
amanda             908   0.8  0.4  4864384  65076   ??  S    19Dec18  42:19.54 /Applications/Utilities/Adobe Creative Cloud/ACC/Creative Cloud.app/Contents/MacOS/Creative Cloud --showwindow=false --onOSstartup=true
amanda           14101   0.7  0.7  6014552 113492   ??  S    Thu05PM  20:35.85 /private/var/folders/99/pccf2f9x1gz2y99n3m6hbdg40000gn/T/AppTranslocation/76BB7FC3-740A-4B11-BA03-58E8DE438C57/d/Visual Studio Code.app/Contents/MacOS/Electron
amanda           22409   0.6  0.5  4872232  89828   ??  S     1:41PM   0:06.15 /Applications/Google Chrome.app/Contents/Versions/71.0.3578.98/Google Chrome Helper.app/Contents/MacOS/Google Chrome Helper --type=renderer --field-trial-handle=18050009161147368515,12073003594094258993,131072 --service-pipe-token=11963457778838214393 --lang=en-US --metrics-client-id=c4c85bd6-057c-4022-b575-d3dbada7fab5 --enable-offline-auto-reload --enable-offline-auto-reload-visible-only --num-raster-threads=4 --enable-zero-copy --enable-gpu-memory-buffer-compositor-resources --enable-main-frame-before-activation --service-request-channel-token=11963457778838214393 --renderer-client-id=3212 --no-v8-untrusted-code-mitigations --seatbelt-client=267
amanda             936   0.5  0.1  4665948  18364   ??  S    19Dec18  30:20.06 /Library/Application Support/Adobe/Adobe Desktop Common/HEX/Adobe CEF Helper.app/Contents/MacOS/Adobe CEF Helper --type=gpu-process --disable-features=AsyncWheelEvents,TouchpadAndWheelScrollLatching --log-file=/Users/amanda/Library/Logs/CreativeCloud/ACC/CEF.log --log-severity=warning --user-agent=Mozilla/5.0 (Macintosh) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/57.0.2987.98 Safari/537.36 CreativeCloud/4.7.0.400 --lang=en-US --gpu-preferences=KAAAAAAAAAAAAQAAAQAAAAAAAAAAAGAAAAAAAAAAAAAIAAAAAAAAAOAAAAAbAAAA2AAAAAAAAADgAAAAAAAAAOgAAAAAAAAA8AAAAAAAAAD4AAAAAAAAAAABAAAAAAAACAEAAAAAAAAQAQAAAAAAABgBAAAAAAAAIAEAAAAAAAAoAQAAAAAAADABAAAAAAAAOAEAAAAAAABAAQAAAAAAAEgBAAAAAAAAUAEAAAAAAABYAQAAAAAAAGABAAAAAAAAaAEAAAAAAABwAQAAAAAAAHgBAAAAAAAAgAEAAAAAAACIAQAAAAAAAJABAAAAAAAAmAEAAAAAAACgAQAAAAAAAKgBAAAAAAAAEAAAAAAAAAAAAAAABQAAABAAAAAAAAAAAAAAAAsAAAAQAAAAAAAAAAAAAAAMAAAAEAAAAAAAAAAAAAAADgAAABAAAAAAAAAAAAAAAA8AAAAQAAAAAAAAAAAAAAARAAAAEAAAAAAAAAAAAAAAEgAAABAAAAAAAAAAAQAAAAUAAAAQAAAAAAAAAAEAAAALAAAAEAAAAAAAAAABAAAADAAAABAAAAAAAAAAAQAAAA4AAAAQAAAAAAAAAAEAAAAPAAAAEAAAAAAAAAABAAAAEQAAABAAAAAAAAAAAQAAABIAAAAQAAAAAAAAAAMAAAALAAAAEAAAAAAAAAADAAAADAAAABAAAAAAAAAAAwAAAA4AAAAQAAAAAAAAAAUAAAAFAAAAEAAAAAAAAAAFAAAADgAAABAAAAAAAAAABQAAAA8AAAAQAAAAAAAAAAUAAAARAAAAEAAAAAAAAAAFAAAAEgAAABAAAAAAAAAABgAAAAUAAAAQAAAAAAAAAAYAAAAOAAAAEAAAAAAAAAAGAAAADwAAABAAAAAAAAAABgAAABEAAAAQAAAAAAAAAAYAAAASAAAA --gpu-vendor-id=0x1002 --gpu-device-id=0x67ef --gpu-driver-vendor --gpu-driver-version --gpu-driver-date --gpu-secondary-vendor-ids=0x8086 --gpu-secondary-device-ids=0x191b --gpu-active-vendor-id=0x1002 --gpu-active-device-id=0x67ef --amd-switchable --log-file=/Users/amanda/Library/Logs/CreativeCloud/ACC/CEF.log --log-severity=warning --user-agent=Mozilla/5.0 (Macintosh) AppleWebKit/537.36 (KHTML,like Gecko) Chrome/57.0.2987.98 Safari/537.36 CreativeCloud/4.7.0.400 --lang=en-US --service-request-channel-token=D6BAB66AB05FEC2815A04BF399862996
amanda            4259   0.5  0.0  4494288   6596   ??  S    26Dec18  59:21.39 /usr/libexec/avconferenced
amanda            9315   0.3  0.6  4787624  95048   ??  S     7Jan19   7:14.75 /Applications/Slack.app/Contents/Frameworks/Slack Helper.app/Contents/MacOS/Slack Helper --type=gpu-process --no-sandbox --supports-dual-gpus=true --gpu-driver-bug-workarounds=1,12,27,30,56,70,73,75,76,84,86,94,95,100,103 --disable-gl-extensions=GL_KHR_blend_equation_advanced GL_KHR_blend_equation_advanced_coherent --gpu-vendor-id=0x1002 --gpu-device-id=0x67ef --gpu-driver-vendor --gpu-driver-version --gpu-driver-date --gpu-secondary-vendor-ids=0x8086 --gpu-secondary-device-ids=0x191b --gpu-active-vendor-id=0x1002 --gpu-active-device-id=0x67ef --service-request-channel-token=3639B7C38F378F09F2D4FF282024A058
amanda           22412   0.3  0.7  4884984 109568   ??  S     1:41PM   0:08.20 /Applications/Google Chrome.app/Contents/Versions/71.0.3578.98/Google Chrome Helper.app/Contents/MacOS/Google Chrome Helper --type=renderer --field-trial-handle=18050009161147368515,12073003594094258993,131072 --service-pipe-token=1454831158334513806 --lang=en-US --metrics-client-id=c4c85bd6-057c-4022-b575-d3dbada7fab5 --enable-offline-auto-reload --enable-offline-auto-reload-visible-only --num-raster-threads=4 --enable-zero-copy --enable-gpu-memory-buffer-compositor-resources --enable-main-frame-before-activation --service-request-channel-token=1454831158334513806 --renderer-client-id=3215 --no-v8-untrusted-code-mitigations --seatbelt-client=276
amanda           22233   0.2  0.0  4300620   1532 s002  Ss    1:16PM   0:00.03 /bin/bash -l
amanda           22411   0.2  0.5  4849392  87284   ??  S     1:41PM   0:03.50 /Applications/Google Chrome.app/Contents/Versions/71.0.3578.98/Google Chrome Helper.app/Contents/MacOS/Google Chrome Helper --type=renderer --field-trial-handle=18050009161147368515,12073003594094258993,131072 --service-pipe-token=2792898493418399626 --lang=en-US --metrics-client-id=c4c85bd6-057c-4022-b575-d3dbada7fab5 --enable-offline-auto-reload --enable-offline-auto-reload-visible-only --num-raster-threads=4 --enable-zero-copy --enable-gpu-memory-buffer-compositor-resources --enable-main-frame-before-activation --service-request-channel-token=2792898493418399626 --renderer-client-id=3214 --no-v8-untrusted-code-mitigations --seatbelt-client=187
amanda           14102   0.1  0.4  4871916  67000   ??  S    Thu05PM   7:51.16 /private/var/folders/99/pccf2f9x1gz2y99n3m6hbdg40000gn/T/AppTranslocation/76BB7FC3-740A-4B11-BA03-58E8DE438C57/d/Visual Studio Code.app/Contents/Frameworks/Code Helper.app/Contents/MacOS/Code Helper --type=gpu-process --disable-features=ColorCorrectRendering --no-sandbox --supports-dual-gpus=true --gpu-driver-bug-workarounds=1,12,27,30,56,70,73,75,76,84,86,94,95,100,103 --disable-gl-extensions=GL_KHR_blend_equation_advanced GL_KHR_blend_equation_advanced_coherent --gpu-vendor-id=0x1002 --gpu-device-id=0x67ef --gpu-driver-vendor --gpu-driver-version --gpu-driver-date --gpu-secondary-vendor-ids=0x8086 --gpu-secondary-device-ids=0x191b --gpu-active-vendor-id=0x1002 --gpu-active-device-id=0x67ef --service-request-channel-token=03CD9F11344B0A5BEE45840E9D16049F
amanda           22178   0.0  1.0  6174628 172612   ??  S    12:11PM   0:15.78 /Applications/Safari.app/Contents/MacOS/Safari
amanda           22171   0.0  0.1  4381284  19356   ??  S    12:08PM   0:00.10 /System/Library/Frameworks/CoreServices.framework/Frameworks/Metadata.framework/Versions/A/Support/mdworker_shared -s mdworker -c MDSImporterWorker -m com.apple.mdworker.shared
amanda           22154   0.0  0.1  4412980  17820   ??  S    11:35AM   0:00.45 /System/Library/CoreServices/CoreServicesUIAgent.app/Contents/MacOS/CoreServicesUIAgent
amanda           22110   0.0  0.4  4379684  59364   ??  S     6:50AM   0:01.63 /System/Library/Frameworks/CoreServices.framework/Frameworks/Metadata.framework/Versions/A/Support/mdworker_shared -s mdworker -c MDSImporterWorker -m com.apple.mdworker.shared
amanda           22109   0.0  0.4  4387280  64232   ??  S     6:50AM   0:02.20 /System/Library/Frameworks/CoreServices.framework/Frameworks/Metadata.framework/Versions/A/Support/mdworker_shared -s mdworker -c MDSImporterWorker -m com.apple.mdworker.shared
amanda           21746   0.0  1.4  5036700 243224   ??  S    10:09PM   5:18.79 /Applications/Google Chrome.app/Contents/Versions/71.0.3578.98/Google Chrome Helper.app/Contents/MacOS/Google Chrome Helper --type=renderer --field-trial-handle=18050009161147368515,12073003594094258993,131072 --service-pipe-token=4809356707569035968 --lang=en-US --metrics-client-id=c4c85bd6-057c-4022-b575-d3dbada7fab5 --enable-offline-auto-reload --enable-offline-auto-reload-visible-only --num-raster-threads=4 --enable-zero-copy --enable-gpu-memory-buffer-compositor-resources --enable-main-frame-before-activation --service-request-channel-token=4809356707569035968 --renderer-client-id=3100 --no-v8-untrusted-code-mitigations --seatbelt-client=250
amanda           21486   0.0  0.4  4382348  70132   ??  S     7:25PM   0:08.00 /System/Library/Frameworks/CoreServices.framework/Frameworks/Metadata.framework/Versions/A/Support/mdworker_shared -s mdworker -c MDSImporterWorker -m com.apple.mdworker.shared
amanda           21315   0.0  0.1  4382636  11880   ??  S     5:18PM   0:00.05 open -W http://127.0.0.1:5500/
amanda           21113   0.0  0.4  4384768  73500   ??  S     4:21PM   0:11.27 /System/Library/Frameworks/CoreServices.framework/Frameworks/Metadata.framework/Versions/A/Support/mdworker_shared -s mdworker -c MDSImporterWorker -m com.apple.mdworker.shared
amanda           21029   0.0  1.0  4933596 168812   ??  S     3:19PM   0:05.53 /Applications/Google Chrome.app/Contents/Versions/71.0.3578.98/Google Chrome Helper.app/Contents/MacOS/Google Chrome Helper --type=renderer --field-trial-handle=18050009161147368515,12073003594094258993,131072 --service-pipe-token=14458767925505929557 --lang=en-US --metrics-client-id=c4c85bd6-057c-4022-b575-d3dbada7fab5 --enable-offline-auto-reload --enable-offline-auto-reload-visible-only --num-raster-threads=4 --enable-zero-copy --enable-gpu-memory-buffer-compositor-resources --enable-main-frame-before-activation --service-request-channel-token=14458767925505929557 --renderer-client-id=2984 --no-v8-untrusted-code-mitigations --seatbelt-client=185
amanda           20912   0.0  0.1  4860892  20116   ??  Ss    2:33PM   0:00.11 /System/Library/Frameworks/Metal.framework/Versions/A/XPCServices/MTLCompilerService.xpc/Contents/MacOS/MTLCompilerService
amanda           20775   0.0  0.2  4357508  26160   ??  Ss   Tue01PM   0:00.06 /System/Library/Frameworks/SafariServices.framework/Versions/A/XPCServices/com.apple.SafariServices.xpc/Contents/MacOS/com.apple.SafariServices
amanda           20738   0.0  0.2  4439988  41796   ??  Ss   Tue01PM   0:04.10 /Applications/Utilities/Adobe Sync/CoreSync/Core Sync.app/Contents/PlugIns/ACCFinderSync.appex/Contents/MacOS/ACCFinderSync
amanda           20693   0.0  0.1  4380184  24752   ??  S    Tue12PM   0:00.39 /Applications/Sublime Text.app/Contents/MacOS/plugin_host 20690 --auto-shell-env
amanda           20692   0.0  0.1  4879324  22320   ??  Ss   Tue12PM   0:00.19 /System/Library/Frameworks/Metal.framework/Versions/A/XPCServices/MTLCompilerService.xpc/Contents/MacOS/MTLCompilerService
amanda           20690   0.0  1.2  5101476 202908   ??  S    Tue12PM   0:26.40 /Applications/Sublime Text.app/Contents/MacOS/Sublime Text
amanda           19373   0.0  0.0  4860892      8   ??  Ss   Mon03PM   0:00.30 /System/Library/Frameworks/Metal.framework/Versions/A/XPCServices/MTLCompilerService.xpc/Contents/MacOS/MTLCompilerService
amanda           19372   0.0  0.0  4429508   7756   ??  Ss   Mon03PM   0:04.40 /System/Library/Frameworks/AppKit.framework/Versions/C/XPCServices/SandboxedServiceRunner.xpc/Contents/MacOS/SandboxedServiceRunner
amanda           19285   0.0  0.6  5074528  97620   ??  S    Mon03PM   0:15.16 /Applications/Google Chrome.app/Contents/Versions/71.0.3578.98/Google Chrome Helper.app/Contents/MacOS/Google Chrome Helper --type=renderer --field-trial-handle=18050009161147368515,12073003594094258993,131072 --service-pipe-token=6459708796670617364 --lang=en-US --metrics-client-id=c4c85bd6-057c-4022-b575-d3dbada7fab5 --enable-offline-auto-reload --enable-offline-auto-reload-visible-only --num-raster-threads=4 --enable-zero-copy --enable-gpu-memory-buffer-compositor-resources --enable-main-frame-before-activation --service-request-channel-token=6459708796670617364 --renderer-client-id=2788 --no-v8-untrusted-code-mitigations --seatbelt-client=214
amanda           18909   0.0  0.0  4383624    956   ??  Ss   Mon06AM   0:00.10 /System/Library/Frameworks/VideoToolbox.framework/Versions/A/XPCServices/VTDecoderXPCService.xpc/Contents/MacOS/VTDecoderXPCService
amanda           18776   0.0  0.2  4836964  35104   ??  S    Sun07PM   1:13.11 /Applications/Google Chrome.app/Contents/Versions/71.0.3578.98/Google Chrome Helper.app/Contents/MacOS/Google Chrome Helper --type=renderer --field-trial-handle=18050009161147368515,12073003594094258993,131072 --service-pipe-token=1920718223923839446 --lang=en-US --metrics-client-id=c4c85bd6-057c-4022-b575-d3dbada7fab5 --enable-offline-auto-reload --enable-offline-auto-reload-visible-only --num-raster-threads=4 --enable-zero-copy --enable-gpu-memory-buffer-compositor-resources --enable-main-frame-before-activation --service-request-channel-token=1920718223923839446 --renderer-client-id=2702 --no-v8-untrusted-code-mitigations --seatbelt-client=305
amanda           18592   0.0  0.0  4374188    488   ??  S    Sun02PM   0:00.07 open -W http://127.0.0.1:5500/index.html
amanda           18307   0.0  0.0  4382380    452   ??  S    Sun01PM   0:00.07 open -W http://127.0.0.1:5500/index.html
amanda           18272   0.0  0.0  4374188    452   ??  S    Sun01PM   0:00.07 open -W http://127.0.0.1:5500/index.html
amanda           18157   0.0  0.0  4382380    488   ??  S    Sun01PM   0:00.07 open -W http://127.0.0.1:5500/index.html
amanda           18099   0.0  0.0  4374188    496   ??  S    Sun01PM   0:00.07 open -W http://127.0.0.1:5500/index.html
amanda           18051   0.0  0.0  4382380    488   ??  S    Sun01PM   0:00.07 open -W http://127.0.0.1:5500/index.html
amanda           17886   0.0  0.0  4382380    488   ??  S    Sun01PM   0:00.07 open -W http://127.0.0.1:5500/
amanda           17792   0.0  0.0  4374188    476   ??  S    Sun01PM   0:00.07 open -W http://127.0.0.1:5500/index.html
amanda           17697   0.0  0.0  4374188    488   ??  S    Sun12PM   0:00.07 open -W http://127.0.0.1:5500/index.html
amanda           17666   0.0  0.0  4374188    496   ??  S    Sun12PM   0:00.07 open -W http://127.0.0.1:5500/index.html
amanda           17651   0.0  0.0  4382380    476   ??  S    Sun12PM   0:00.07 open -W http://127.0.0.1:5500/index.html
amanda           17629   0.0  0.0  4382380    472   ??  S    Sun12PM   0:00.07 open -W http://127.0.0.1:5500/index.html
amanda           17546   0.0  0.0  4382380    480   ??  S    Sun12PM   0:00.07 open -W http://127.0.0.1:5500/index.html
amanda           17464   0.0  0.0  4305740      8 s003  S+   Sun12PM   0:00.04 -bash
root             17463   0.0  0.0  4333332      8 s003  Ss   Sun12PM   0:00.03 login -pf amanda
amanda           17455   0.0  0.0  4382380    492   ??  S    Sun12PM   0:00.07 open -W http://127.0.0.1:5500/index.html
amanda           17436   0.0  0.0  4365996    484   ??  S    Sun12PM   0:00.07 open -W http://127.0.0.1:5500/index.html
amanda           17415   0.0  0.0  4382380    496   ??  S    Sun12PM   0:00.07 open -W http://127.0.0.1:5500/index.html
amanda           17293   0.0  0.0  4374188    476   ??  S    Sun12PM   0:00.07 open -W http://127.0.0.1:5500/index.html
amanda           17237   0.0  0.0  4382380    484   ??  S    Sun12PM   0:00.07 open -W http://127.0.0.1:5500/
amanda           17210   0.0  0.0  4382380    480   ??  S    Sun11AM   0:00.07 open -W http://127.0.0.1:5500/index.html
amanda           17175   0.0  0.0  4382380    476   ??  S    Sun11AM   0:00.07 open -W http://127.0.0.1:5500/index.html
amanda           17164   0.0  0.0  4382380    484   ??  S    Sun11AM   0:00.07 open -W http://127.0.0.1:5500/
amanda           17144   0.0  0.0  4365996    476   ??  S    Sun11AM   0:00.07 open -W http://127.0.0.1:5500/index.html
amanda           16877   0.0  0.0  4382380    492   ??  S    Sun11AM   0:00.07 open -W http://127.0.0.1:5500/index.html
amanda           16787   0.0  0.0  4374188    448   ??  S    Sun11AM   0:00.07 open -W http://127.0.0.1:5500/
amanda           16783   0.0  0.0  4382380    512   ??  S    Sun11AM   0:00.07 open -W http://127.0.0.1:5500/index.html
amanda           16756   0.0  0.0  4374188    460   ??  S    Sun11AM   0:00.07 open -W http://127.0.0.1:5500/
amanda           15090   0.0  0.0  4382380    488   ??  S    Fri04PM   0:00.08 open -W http://127.0.0.1:5500/index.html
amanda           15088   0.0  1.8  5947088 296600   ??  S    Fri04PM   9:18.34 /Applications/Slack.app/Contents/Frameworks/Slack Helper.app/Contents/MacOS/Slack Helper --type=renderer --disable-pinch --force-color-profile=srgb --no-sandbox --service-pipe-token=F60A50E440E10CA05EA34195FF212EAE --lang=en-US --standard-schemes=slack-resources,slack-sounds,slack-webapp-dev--secure-schemes=slack-resources,slack-sounds,slack-webapp-dev --app-path=/Applications/Slack.app/Contents/Resources/app.asar --enable-experimental-web-platform-features --node-integration=false --webview-tag=false --no-sandbox --preload=/Applications/Slack.app/Contents/Resources/app.asar/src/static/ssb-interop.js --context-id=1 --num-raster-threads=4 --enable-zero-copy --enable-gpu-memory-buffer-compositor-resources --enable-main-frame-before-activation --content-image-texture-target=0,0,3553;0,1,3553;0,2,3553;0,3,3553;0,4,3553;0,5,3553;0,6,3553;0,7,3553;0,8,3553;0,9,3553;0,10,3553;0,11,34037;0,12,34037;0,13,34037;0,14,3553;0,15,3553;0,16,3553;0,17,3553;1,0,3553;1,1,3553;1,2,3553;1,3,3553;1,4,3553;1,5,3553;1,6,3553;1,7,3553;1,8,3553;1,9,3553;1,10,3553;1,11,34037;1,12,34037;1,13,34037;1,14,3553;1,15,3553;1,16,3553;1,17,3553;2,0,3553;2,1,3553;2,2,3553;2,3,3553;2,4,3553;2,5,3553;2,6,3553;2,7,3553;2,8,3553;2,9,3553;2,10,3553;2,11,34037;2,12,34037;2,13,34037;2,14,3553;2,15,3553;2,16,3553;2,17,3553;3,0,3553;3,1,3553;3,2,3553;3,3,3553;3,4,3553;3,5,34037;3,6,3553;3,7,3553;3,8,3553;3,9,3553;3,10,3553;3,11,3553;3,12,3553;3,13,34037;3,14,34037;3,15,3553;3,16,34037;3,17,34037;4,0,3553;4,1,3553;4,2,3553;4,3,3553;4,4,3553;4,5,34037;4,6,3553;4,7,3553;4,8,3553;4,9,3553;4,10,3553;4,11,3553;4,12,3553;4,13,34037;4,14,34037;4,15,3553;4,16,34037;4,17,34037 --enable-gpu-async-worker-context --service-request-channel-token=F60A50E440E10CA05EA34195FF212EAE --renderer-client-id=9 {"loadSettings":{"resourcePath":"/Applications/Slack.app/Contents/Resources/app.asar","version":"3.3.3","devMode":false,"logFile":null,"invokedOnStartup":false,"chromeDriver":false,"webappSrcPath":null,"devEnv":null,"rxLogging":false,"sessionId":"MTEzNThiMGQtM2IzOS01MzM0LWIwZGYtNzQ5ZTljMmRlNjA5XzE1NDY5MDA1MzQ4MDM=","releaseChannel":"prod","platformVersion":{"major":18,"minor":2,"build":0},"isTitleBarHidden":false,"isDevMode":false,"appVersion":"3.3.3","versionName":"Dirty Computer","webappParams":null,"launchOnStartup":false,"openDevToolsOnStart":false,"pretendNotReallyWindows10":false,"isAeroGlassEnabled":false,"isGpuCompositionAvailable":true,"windowType":"webapp","subType":"T03ANFNQR-preload"},"perfTimer":{"mainPid":819,"BOOT":[237534,465761946],"numTeamsAtLaunch":1,"SHELL":[237534,646866890],"APP_READY":[237535,859700632],"MAIN_WINDOW_CREATING":[237536,309119730]},"identifier":"slack_preload_metadata_arguments","teamId":"T03ANFNQR"}
amanda           14590   0.0  0.0  4350376    664   ??  S    Thu06PM   0:00.10 /System/Library/Frameworks/ApplicationServices.framework/Frameworks/PrintCore.framework/Versions/A/printtool agent
amanda           14223   0.0  0.0  4439732   6944   ??  Ss   Thu06PM   0:08.75 /Applications/Utilities/Adobe Sync/CoreSync/Core Sync.app/Contents/PlugIns/ACCFinderSync.appex/Contents/MacOS/ACCFinderSync
amanda           14131   0.0  0.0  4382380    484   ??  S    Thu05PM   0:00.09 open -W http://127.0.0.1:5500/index.html
amanda           14127   0.0  0.4  5259848  58792   ??  S    Thu05PM   0:23.73 /private/var/folders/99/pccf2f9x1gz2y99n3m6hbdg40000gn/T/AppTranslocation/76BB7FC3-740A-4B11-BA03-58E8DE438C57/d/Visual Studio Code.app/Contents/Frameworks/Code Helper.app/Contents/MacOS/Code Helper --type=renderer --js-flags=--nolazy --disable-mojo-local-storage --no-sandbox --disable-features=ColorCorrectRendering --service-pipe-token=C3F03E369044A868BFD07B2A79F59832 --lang=en-US --app-path=/private/var/folders/99/pccf2f9x1gz2y99n3m6hbdg40000gn/T/AppTranslocation/76BB7FC3-740A-4B11-BA03-58E8DE438C57/d/Visual Studio Code.app/Contents/Resources/app --node-integration=true --webview-tag=true --no-sandbox --background-color=#171717 --disable-blink-features=Auxclick --context-id=2 --enable-pinch --num-raster-threads=4 --enable-zero-copy --enable-gpu-memory-buffer-compositor-resources --enable-main-frame-before-activation --content-image-texture-target=0,0,3553;0,1,3553;0,2,3553;0,3,3553;0,4,3553;0,5,3553;0,6,3553;0,7,3553;0,8,3553;0,9,3553;0,10,3553;0,11,34037;0,12,34037;0,13,34037;0,14,3553;0,15,3553;0,16,3553;0,17,3553;1,0,3553;1,1,3553;1,2,3553;1,3,3553;1,4,3553;1,5,3553;1,6,3553;1,7,3553;1,8,3553;1,9,3553;1,10,3553;1,11,34037;1,12,34037;1,13,34037;1,14,3553;1,15,3553;1,16,3553;1,17,3553;2,0,3553;2,1,3553;2,2,3553;2,3,3553;2,4,3553;2,5,3553;2,6,3553;2,7,3553;2,8,3553;2,9,3553;2,10,3553;2,11,34037;2,12,34037;2,13,34037;2,14,3553;2,15,3553;2,16,3553;2,17,3553;3,0,3553;3,1,3553;3,2,3553;3,3,3553;3,4,3553;3,5,34037;3,6,3553;3,7,3553;3,8,3553;3,9,3553;3,10,3553;3,11,3553;3,12,3553;3,13,34037;3,14,34037;3,15,3553;3,16,34037;3,17,34037;4,0,3553;4,1,3553;4,2,3553;4,3,3553;4,4,3553;4,5,34037;4,6,3553;4,7,3553;4,8,3553;4,9,3553;4,10,3553;4,11,3553;4,12,3553;4,13,34037;4,14,34037;4,15,3553;4,16,34037;4,17,34037 --enable-gpu-async-worker-context --service-request-channel-token=C3F03E369044A868BFD07B2A79F59832 --renderer-client-id=6
amanda           14108   0.0  0.0  4338364    712   ??  S    Thu05PM   0:00.09 /var/folders/99/pccf2f9x1gz2y99n3m6hbdg40000gn/T/AppTranslocation/76BB7FC3-740A-4B11-BA03-58E8DE438C57/d/Visual Studio Code.app/Contents/Frameworks/Electron Framework.framework/Resources/crashpad_handler --no-rate-limit --no-upload-gzip --database=/var/folders/99/pccf2f9x1gz2y99n3m6hbdg40000gn/T/VSCode Crashes --metrics-dir=/var/folders/99/pccf2f9x1gz2y99n3m6hbdg40000gn/T/VSCode Crashes --url=https://rink.hockeyapp.net/api/2/apps/21a48a66799e47fea4f52c0ff81e803d/crashes/upload --handshake-fd=57
amanda           14092   0.0  0.0  4382380    496   ??  S    Thu05PM   0:00.09 open -W http://127.0.0.1:5500/
amanda           14058   0.0  0.0  4382380    500   ??  S    Thu05PM   0:00.09 open -W http://127.0.0.1:5500/
amanda           13962   0.0  0.0  4382380    488   ??  S    Thu05PM   0:00.08 open -W http://127.0.0.1:5500/
amanda           13876   0.0  0.0  4382380    476   ??  S    Thu05PM   0:00.08 open -W http://127.0.0.1:5500/
amanda           13813   0.0  0.0  4382380    480   ??  S    Thu05PM   0:00.08 open -W http://127.0.0.1:5500/
amanda           13769   0.0  0.0  4382380    464   ??  S    Thu05PM   0:00.08 open -W http://127.0.0.1:5500/index.html
amanda           13767   0.0  0.0  4382380    508   ??  S    Thu05PM   0:00.09 open -W http://127.0.0.1:5500/index.html
amanda           13754   0.0  0.0  4382380    460   ??  S    Thu05PM   0:00.08 open -W http://127.0.0.1:5500/index.html
amanda           13733   0.0  0.0  4382380    488   ??  S    Thu05PM   0:00.08 open -W http://127.0.0.1:5500/index.html
amanda           13649   0.0  0.0  4382380    476   ??  S    Thu05PM   0:00.09 open -W http://127.0.0.1:5500/
amanda           13623   0.0  0.0  4382380    484   ??  S    Thu05PM   0:00.09 open -W http://127.0.0.1:5500/index.html
amanda           13296   0.0  0.0  4382380    464   ??  S    Thu04PM   0:00.08 open -W http://127.0.0.1:5500/index.html
amanda           13052   0.0  0.0  4382380    472   ??  S    Thu03PM   0:00.09 open -W http://127.0.0.1:5500/index.html
amanda           13023   0.0  0.0  4382380    496   ??  S    Thu03PM   0:00.09 open -W http://127.0.0.1:5500/
amanda           12412   0.0  0.0  4381700    904   ??  Ss   Wed04PM   0:00.19 /System/Library/PrivateFrameworks/IMTranscoding.framework/XPCServices/IMTranscoderAgent.xpc/Contents/MacOS/IMTranscoderAgent
amanda           12395   0.0  0.0  4844508      8   ??  Ss   Wed04PM   0:00.14 /System/Library/Frameworks/Metal.framework/Versions/A/XPCServices/MTLCompilerService.xpc/Contents/MacOS/MTLCompilerService
amanda           11861   0.0  0.0  4379564    492   ??  S     9Jan19   0:00.10 open -W http://127.0.0.1:5500/index.html
amanda           11778   0.0  0.0  4379564    484   ??  S     9Jan19   0:00.10 open -W http://127.0.0.1:5500/index.html
amanda           11491   0.0  0.0  4927468   4080   ??  Ss    8Jan19   0:07.06 /System/Library/Frameworks/Quartz.framework/Versions/A/Frameworks/QuickLookUI.framework/Versions/A/XPCServices/QuickLookUIService.xpc/Contents/MacOS/QuickLookUIService
amanda           11284   0.0  0.0  4383588   1936   ??  S     8Jan19   0:02.84 /var/folders/99/pccf2f9x1gz2y99n3m6hbdg40000gn/T/AppTranslocation/76BB7FC3-740A-4B11-BA03-58E8DE438C57/d/Visual Studio Code.app/Contents/Frameworks/Electron Framework.framework/Resources/crashpad_handler --no-rate-limit --no-upload-gzip --database=/var/folders/99/pccf2f9x1gz2y99n3m6hbdg40000gn/T/VSCode Crashes --metrics-dir=/var/folders/99/pccf2f9x1gz2y99n3m6hbdg40000gn/T/VSCode Crashes --url=https://rink.hockeyapp.net/api/2/apps/21a48a66799e47fea4f52c0ff81e803d/crashes/upload --handshake-fd=59
amanda           10970   0.0  0.0  4315584      8   ??  S     8Jan19   0:00.04 /System/Library/Frameworks/CoreSpotlight.framework/CoreSpotlightService
amanda           10782   0.0  0.0  4351636    676   ??  S     8Jan19   0:00.16 /usr/libexec/SafariPlugInUpdateNotifier
amanda           10627   0.0  0.2  5055520  33056   ??  Ss    8Jan19   0:11.38 /System/Library/PrivateFrameworks/Lookup.framework/Versions/A/XPCServices/LookupViewService.xpc/Contents/MacOS/LookupViewService
amanda           10403   0.0  0.0  4371372    468   ??  S     8Jan19   0:00.10 open -W http://127.0.0.1:5500/wats3020-mad-libs/index.html
amanda           10304   0.0  0.1  4390304   8444   ??  Ss    8Jan19   0:03.78 /System/Library/PrivateFrameworks/CommerceKit.framework/Versions/A/XPCServices/com.apple.CommerceKit.TransactionService.xpc/Contents/MacOS/com.apple.CommerceKit.TransactionService
amanda           10282   0.0  0.0  4289460      8   ??  S     8Jan19   0:00.05 /usr/bin/ssh-agent -l
amanda           10250   0.0  0.0  4879324      8   ??  Ss    8Jan19   0:00.26 /System/Library/Frameworks/Metal.framework/Versions/A/XPCServices/MTLCompilerService.xpc/Contents/MacOS/MTLCompilerService
amanda           10249   0.0  0.2  5058452  35924   ??  S     8Jan19   0:52.82 /Applications/Utilities/Terminal.app/Contents/MacOS/Terminal
amanda            9525   0.0  0.0  4852700      8   ??  Ss    7Jan19   0:00.07 /System/Library/Frameworks/Metal.framework/Versions/A/XPCServices/MTLCompilerService.xpc/Contents/MacOS/MTLCompilerService
amanda            9433   0.0  0.1  4932788  12528   ??  Ss    7Jan19   0:09.45 /System/Library/Frameworks/Quartz.framework/Versions/A/Frameworks/QuickLookUI.framework/Versions/A/XPCServices/QuickLookUIService.xpc/Contents/MacOS/QuickLookUIService
amanda            9414   0.0  0.0  4353724    656   ??  S     7Jan19   0:00.15 /var/folders/99/pccf2f9x1gz2y99n3m6hbdg40000gn/T/AppTranslocation/76BB7FC3-740A-4B11-BA03-58E8DE438C57/d/Visual Studio Code.app/Contents/Frameworks/Electron Framework.framework/Resources/crashpad_handler --no-rate-limit --no-upload-gzip --database=/var/folders/99/pccf2f9x1gz2y99n3m6hbdg40000gn/T/VSCode Crashes --metrics-dir=/var/folders/99/pccf2f9x1gz2y99n3m6hbdg40000gn/T/VSCode Crashes --url=https://rink.hockeyapp.net/api/2/apps/21a48a66799e47fea4f52c0ff81e803d/crashes/upload --handshake-fd=51
amanda            9321   0.0  0.3  5269244  43100   ??  S     7Jan19   0:13.35 /Applications/Slack.app/Contents/Frameworks/Slack Helper.app/Contents/MacOS/Slack Helper --type=renderer --disable-pinch --force-color-profile=srgb --no-sandbox --service-pipe-token=1484C0F05BD9FD5C60F3BE04220F27CF --lang=en-US --standard-schemes=slack-resources,slack-sounds,slack-webapp-dev--secure-schemes=slack-resources,slack-sounds,slack-webapp-dev --app-path=/Applications/Slack.app/Contents/Resources/app.asar --node-integration=true --webview-tag=false --no-sandbox --preload=/Applications/Slack.app/Contents/Resources/app.asar/src/static/index.js --background-color=#FFFFFF --context-id=2 --num-raster-threads=4 --enable-zero-copy --enable-gpu-memory-buffer-compositor-resources --enable-main-frame-before-activation --content-image-texture-target=0,0,3553;0,1,3553;0,2,3553;0,3,3553;0,4,3553;0,5,3553;0,6,3553;0,7,3553;0,8,3553;0,9,3553;0,10,3553;0,11,34037;0,12,34037;0,13,34037;0,14,3553;0,15,3553;0,16,3553;0,17,3553;1,0,3553;1,1,3553;1,2,3553;1,3,3553;1,4,3553;1,5,3553;1,6,3553;1,7,3553;1,8,3553;1,9,3553;1,10,3553;1,11,34037;1,12,34037;1,13,34037;1,14,3553;1,15,3553;1,16,3553;1,17,3553;2,0,3553;2,1,3553;2,2,3553;2,3,3553;2,4,3553;2,5,3553;2,6,3553;2,7,3553;2,8,3553;2,9,3553;2,10,3553;2,11,34037;2,12,34037;2,13,34037;2,14,3553;2,15,3553;2,16,3553;2,17,3553;3,0,3553;3,1,3553;3,2,3553;3,3,3553;3,4,3553;3,5,34037;3,6,3553;3,7,3553;3,8,3553;3,9,3553;3,10,3553;3,11,3553;3,12,3553;3,13,34037;3,14,34037;3,15,3553;3,16,34037;3,17,34037;4,0,3553;4,1,3553;4,2,3553;4,3,3553;4,4,3553;4,5,34037;4,6,3553;4,7,3553;4,8,3553;4,9,3553;4,10,3553;4,11,3553;4,12,3553;4,13,34037;4,14,34037;4,15,3553;4,16,34037;4,17,34037 --enable-gpu-async-worker-context --service-request-channel-token=1484C0F05BD9FD5C60F3BE04220F27CF --renderer-client-id=8 {"loadSettings":{"resourcePath":"/Applications/Slack.app/Contents/Resources/app.asar","version":"3.3.3","devMode":false,"logFile":null,"invokedOnStartup":false,"chromeDriver":false,"webappSrcPath":null,"devEnv":null,"rxLogging":false,"sessionId":"MTEzNThiMGQtM2IzOS01MzM0LWIwZGYtNzQ5ZTljMmRlNjA5XzE1NDY5MDA1MzQ4MDM=","releaseChannel":"prod","platformVersion":{"major":18,"minor":2,"build":0},"isTitleBarHidden":false,"isDevMode":false,"appVersion":"3.3.3","versionName":"Dirty Computer","webappParams":null,"launchOnStartup":false,"openDevToolsOnStart":false,"pretendNotReallyWindows10":false,"isAeroGlassEnabled":false,"isGpuCompositionAvailable":true,"webPreferences":{"webviewTag":false,"preload":"/Applications/Slack.app/Contents/Resources/app.asar/src/static/index.js"},"title":"Slack","autoHideMenuBar":false,"show":false,"windowType":"main","bootstrapScript":"/Applications/Slack.app/Contents/Resources/app.asar/src/renderer/main.tsx","acceptFirstMouse":false,"backgroundColor":"#FFFFFF","minHeight":400,"minWidth":600},"perfTimer":{"mainPid":819,"BOOT":[237534,465761946],"numTeamsAtLaunch":1,"SHELL":[237534,646866890],"APP_READY":[237535,859700632],"MAIN_WINDOW_CREATING":[237536,309119730]},"identifier":"slack_preload_metadata_arguments"}
amanda            9319   0.0  0.0  4346516    676   ??  S     7Jan19   0:00.16 /Applications/Slack.app/Contents/Frameworks/Electron Framework.framework/Resources/crashpad_handler --no-rate-limit --no-upload-gzip --database=/var/folders/99/pccf2f9x1gz2y99n3m6hbdg40000gn/T/Slack Crashes --metrics-dir=/var/folders/99/pccf2f9x1gz2y99n3m6hbdg40000gn/T/Slack Crashes --url=https://slack.com/apps/breakpad?instanceUid=11358b0d-3b39-5334-b0df-749e9c2de609&version=3.3.3&channel=prod --handshake-fd=49
amanda            9316   0.0  0.0  4878300      8   ??  Ss    7Jan19   0:00.21 /System/Library/Frameworks/Metal.framework/Versions/A/XPCServices/MTLCompilerService.xpc/Contents/MacOS/MTLCompilerService
amanda            8728   0.0  0.6  5225992  98196   ??  S     6Jan19  36:46.79 /Applications/Google Chrome.app/Contents/Versions/71.0.3578.98/Google Chrome Helper.app/Contents/MacOS/Google Chrome Helper --type=renderer --field-trial-handle=18050009161147368515,12073003594094258993,131072 --service-pipe-token=18240148400242609507 --lang=en-US --metrics-client-id=c4c85bd6-057c-4022-b575-d3dbada7fab5 --enable-offline-auto-reload --enable-offline-auto-reload-visible-only --num-raster-threads=4 --enable-zero-copy --enable-gpu-memory-buffer-compositor-resources --enable-main-frame-before-activation --service-request-channel-token=18240148400242609507 --renderer-client-id=1403 --no-v8-untrusted-code-mitigations --seatbelt-client=215
amanda            7813   0.0  0.0  4392808   1888   ??  Ss    4Jan19   0:18.88 /System/Library/Frameworks/WebKit.framework/Versions/A/XPCServices/com.apple.WebKit.Networking.xpc/Contents/MacOS/com.apple.WebKit.Networking
amanda            7246   0.0  0.0  4379080   1312   ??  S     3Jan19   0:00.39 /System/Library/PrivateFrameworks/AccountsDaemon.framework/XPCServices/DataclassOwnersManager.xpc/Contents/MacOS/DataclassOwnersManager
amanda            4751   0.0  0.0  4379920   5060   ??  Ss   27Dec18   0:05.05 /System/Library/PrivateFrameworks/IMFoundation.framework/XPCServices/IMRemoteURLConnectionAgent.xpc/Contents/MacOS/IMRemoteURLConnectionAgent
amanda            4500   0.0  0.0  4390232    936   ??  Ss   26Dec18   0:00.53 /System/Library/Frameworks/VideoToolbox.framework/Versions/A/XPCServices/VTDecoderXPCService.xpc/Contents/MacOS/VTDecoderXPCService
amanda            4497   0.0  0.0  4373288    612   ??  Ss   26Dec18   0:00.33 /System/Library/PrivateFrameworks/AssistantServices.framework/Versions/A/XPCServices/com.apple.siri.ClientFlow.ClientScripter.xpc/Contents/MacOS/com.apple.siri.ClientFlow.ClientScripter
amanda            4496   0.0  0.0  4313384      8   ??  Ss   26Dec18   0:00.02 /System/Library/Frameworks/AudioToolbox.framework/XPCServices/com.apple.audio.SandboxHelper.xpc/Contents/MacOS/com.apple.audio.SandboxHelper
amanda            4495   0.0  0.0  4843484      8   ??  Ss   26Dec18   0:00.10 /System/Library/Frameworks/Metal.framework/Versions/A/XPCServices/MTLCompilerService.xpc/Contents/MacOS/MTLCompilerService
amanda            4494   0.0  0.0  4349804    936   ??  Ss   26Dec18   0:00.65 /System/Library/CoreServices/ControlStrip.app/Contents/XPCServices/com.apple.DFRSystemExtra.Siri.xpc/Contents/MacOS/com.apple.DFRSystemExtra.Siri
amanda            4378   0.0  0.0  4852700      8   ??  Ss   26Dec18   0:00.08 /System/Library/Frameworks/Metal.framework/Versions/A/XPCServices/MTLCompilerService.xpc/Contents/MacOS/MTLCompilerService
amanda            4273   0.0  0.0  4317220      8   ??  Ss   26Dec18   0:00.02 /System/Library/Frameworks/AudioToolbox.framework/XPCServices/com.apple.audio.SandboxHelper.xpc/Contents/MacOS/com.apple.audio.SandboxHelper
amanda            4271   0.0  0.0  4315432      8   ??  Ss   26Dec18   0:00.02 /System/Library/Frameworks/AudioToolbox.framework/XPCServices/com.apple.audio.SandboxHelper.xpc/Contents/MacOS/com.apple.audio.SandboxHelper
amanda            4265   0.0  0.0  4870108      8   ??  Ss   26Dec18   0:00.11 /System/Library/Frameworks/Metal.framework/Versions/A/XPCServices/MTLCompilerService.xpc/Contents/MacOS/MTLCompilerService
amanda            4263   0.0  0.1  4985776  12676   ??  Ss   26Dec18   0:42.06 /Applications/FaceTime.app/Contents/XPCServices/FaceTimeNotificationCenterService.xpc/Contents/MacOS/FaceTimeNotificationCenterService
amanda            4262   0.0  0.0  4333604      8   ??  Ss   26Dec18   0:00.02 /System/Library/Frameworks/AudioToolbox.framework/XPCServices/com.apple.audio.SandboxHelper.xpc/Contents/MacOS/com.apple.audio.SandboxHelper
amanda            4261   0.0  0.0  4379920   4916   ??  Ss   26Dec18   0:05.35 /System/Library/PrivateFrameworks/IMFoundation.framework/XPCServices/IMRemoteURLConnectionAgent.xpc/Contents/MacOS/IMRemoteURLConnectionAgent
amanda            4260   0.0  0.0  4879324      8   ??  Ss   26Dec18   0:00.25 /System/Library/Frameworks/Metal.framework/Versions/A/XPCServices/MTLCompilerService.xpc/Contents/MacOS/MTLCompilerService
amanda            4257   0.0  0.2  5058276  38028   ??  S    26Dec18   7:55.34 /Applications/FaceTime.app/Contents/MacOS/FaceTime
amanda            4053   0.0  0.0  4436916   7404   ??  Ss   26Dec18   0:27.18 /Applications/Utilities/Adobe Sync/CoreSync/Core Sync.app/Contents/PlugIns/ACCFinderSync.appex/Contents/MacOS/ACCFinderSync
amanda            4052   0.0  0.0  4860892      8   ??  Ss   26Dec18   0:00.24 /System/Library/Frameworks/Metal.framework/Versions/A/XPCServices/MTLCompilerService.xpc/Contents/MacOS/MTLCompilerService
amanda            4049   0.0  0.1  5046092  21616   ??  Ss   26Dec18   1:11.89 /System/Library/Frameworks/AppKit.framework/Versions/C/XPCServices/com.apple.appkit.xpc.openAndSavePanelService.xpc/Contents/MacOS/com.apple.appkit.xpc.openAndSavePanelService
amanda            4019   0.0  0.0  4897556   3568   ??  Ss   26Dec18   0:12.84 /System/Library/PrivateFrameworks/Lookup.framework/Versions/A/XPCServices/LookupViewService.xpc/Contents/MacOS/LookupViewService
amanda            4014   0.0  0.0  4884468      8   ??  Ss   26Dec18   0:00.46 /System/Library/Frameworks/Metal.framework/Versions/A/XPCServices/MTLCompilerService.xpc/Contents/MacOS/MTLCompilerService
amanda            3955   0.0  0.0  4379920   2272   ??  Ss   26Dec18   0:04.82 /System/Library/PrivateFrameworks/IMFoundation.framework/XPCServices/IMRemoteURLConnectionAgent.xpc/Contents/MacOS/IMRemoteURLConnectionAgent
amanda            3954   0.0  0.0  4306980      8   ??  Ss   26Dec18   0:00.02 /System/Library/Frameworks/AudioToolbox.framework/XPCServices/com.apple.audio.SandboxHelper.xpc/Contents/MacOS/com.apple.audio.SandboxHelper
amanda            3952   0.0  1.7  6296588 287992   ??  S    26Dec18   8:40.81 /Applications/Messages.app/Contents/MacOS/Messages
amanda            3517   0.0  0.0  4342056      8   ??  Ss   25Dec18   0:00.02 /System/Library/Frameworks/AudioToolbox.framework/XPCServices/com.apple.audio.SandboxHelper.xpc/Contents/MacOS/com.apple.audio.SandboxHelper
amanda            3401   0.0  0.0  4437568   7488   ??  Ss   24Dec18   0:28.11 /Applications/Utilities/Adobe Sync/CoreSync/Core Sync.app/Contents/PlugIns/ACCFinderSync.appex/Contents/MacOS/ACCFinderSync
amanda            3153   0.0  0.0  4893216      8   ??  Ss   24Dec18   0:22.23 /System/Library/Frameworks/Metal.framework/Versions/A/XPCServices/MTLCompilerService.xpc/Contents/MacOS/MTLCompilerService
amanda            2945   0.0  0.0  4351808   1208   ??  Ss   23Dec18   0:02.51 /System/Library/Frameworks/iTunesLibrary.framework/Versions/A/XPCServices/com.apple.iTunesLibraryService.xpc/Contents/MacOS/com.apple.iTunesLibraryService
amanda            2396   0.0  0.0  4428296    768   ??  S    22Dec18   0:06.68 /System/Library/CoreServices/ReportCrash agent
amanda            2062   0.0  0.0  4350984   4628   ??  S    21Dec18   0:01.34 /usr/libexec/silhouette
amanda            2061   0.0  0.0  4422784   1456   ??  Ss   21Dec18   0:08.37 /System/Library/Frameworks/VideoToolbox.framework/Versions/A/XPCServices/VTDecoderXPCService.xpc/Contents/MacOS/VTDecoderXPCService
amanda            2058   0.0  0.0  4379200   1052   ??  S    21Dec18   0:00.70 /System/Library/PrivateFrameworks/UsageTracking.framework/Versions/A/UsageTrackingAgent
amanda            2051   0.0  0.0  4382592   1404   ??  Ss   21Dec18   0:00.51 /System/Library/PrivateFrameworks/CommerceKit.framework/Versions/A/XPCServices/com.apple.CommerceKit.TransactionService.xpc/Contents/MacOS/com.apple.CommerceKit.TransactionService
amanda            1945   0.0  0.0  4416060   7300   ??  S    21Dec18   0:39.62 /System/Library/CoreServices/PowerChime.app/Contents/MacOS/PowerChime
amanda            1941   0.0  0.0  4379240   1536   ??  S    21Dec18   0:01.79 /usr/libexec/assertiond
amanda            1460   0.0  0.0  4433196   2612   ??  S    20Dec18   0:02.62 /System/Library/Frameworks/ApplicationServices.framework/Frameworks/SpeechSynthesis.framework/Resources/com.apple.speech.speechsynthesisd
amanda            1447   0.0  0.0  4879324      8   ??  Ss   20Dec18   0:00.08 /System/Library/Frameworks/Metal.framework/Versions/A/XPCServices/MTLCompilerService.xpc/Contents/MacOS/MTLCompilerService
amanda            1446   0.0  0.0  4925196   6920   ??  S    20Dec18   0:49.32 /System/Library/CoreServices/LocationMenu.app/Contents/MacOS/LocationMenu
amanda            1444   0.0  0.1  4431488  14204   ??  S    20Dec18   1:05.55 /System/Library/PrivateFrameworks/WeatherFoundation.framework/Versions/A/XPCServices/WeatherService.xpc/Contents/MacOS/WeatherService
amanda            1443   0.0  0.0  4384724   7748   ??  S    20Dec18   0:15.26 /System/Library/CoreServices/mapspushd
amanda            1399   0.0  0.3  4856436  45068   ??  S    20Dec18   0:23.71 /Applications/Google Chrome.app/Contents/Versions/71.0.3578.98/Google Chrome Helper.app/Contents/MacOS/Google Chrome Helper --type=renderer --field-trial-handle=18050009161147368515,12073003594094258993,131072 --service-pipe-token=9399947355678064670 --lang=en-US --metrics-client-id=c4c85bd6-057c-4022-b575-d3dbada7fab5 --extension-process --enable-offline-auto-reload --enable-offline-auto-reload-visible-only --num-raster-threads=4 --enable-zero-copy --enable-gpu-memory-buffer-compositor-resources --enable-main-frame-before-activation --service-request-channel-token=9399947355678064670 --renderer-client-id=3 --no-v8-untrusted-code-mitigations --seatbelt-client=137
amanda            1397   0.0  0.0  4860892      8   ??  Ss   20Dec18   0:00.66 /System/Library/Frameworks/Metal.framework/Versions/A/XPCServices/MTLCompilerService.xpc/Contents/MacOS/MTLCompilerService
amanda            1390   0.0  0.1  4387704   8580   ??  Ss   20Dec18   0:02.12 /System/Library/Frameworks/VideoToolbox.framework/Versions/A/XPCServices/VTDecoderXPCService.xpc/Contents/MacOS/VTDecoderXPCService
amanda            1388   0.0  0.0  4386288   6708   ??  Ss   20Dec18   0:02.36 /Applications/Google Chrome.app/Contents/Versions/71.0.3578.98/Google Chrome Framework.framework/Versions/A/XPCServices/AlertNotificationService.xpc/Contents/MacOS/AlertNotificationService
amanda            1387   0.0  1.3  5288848 215272   ??  S    20Dec18 105:31.34 /Applications/Google Chrome.app/Contents/Versions/71.0.3578.98/Google Chrome Helper.app/Contents/MacOS/Google Chrome Helper --type=gpu-process --field-trial-handle=18050009161147368515,12073003594094258993,131072 --metrics-client-id=c4c85bd6-057c-4022-b575-d3dbada7fab5 --gpu-preferences=KAAAAAAAAACAAAAAAQAAAAAAAAAAAGAAAAAAAAAAAAAIAAAAAAAAADgBAAAmAAAAMAEAAAAAAAA4AQAAAAAAAEABAAAAAAAASAEAAAAAAABQAQAAAAAAAFgBAAAAAAAAYAEAAAAAAABoAQAAAAAAAHABAAAAAAAAeAEAAAAAAACAAQAAAAAAAIgBAAAAAAAAkAEAAAAAAACYAQAAAAAAAKABAAAAAAAAqAEAAAAAAACwAQAAAAAAALgBAAAAAAAAwAEAAAAAAADIAQAAAAAAANABAAAAAAAA2AEAAAAAAADgAQAAAAAAAOgBAAAAAAAA8AEAAAAAAAD4AQAAAAAAAAACAAAAAAAACAIAAAAAAAAQAgAAAAAAABgCAAAAAAAAIAIAAAAAAAAoAgAAAAAAADACAAAAAAAAOAIAAAAAAABAAgAAAAAAAEgCAAAAAAAAUAIAAAAAAABYAgAAAAAAABAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAGAAAAEAAAAAAAAAAAAAAABwAAABAAAAAAAAAAAAAAAAgAAAAQAAAAAAAAAAAAAAAKAAAAEAAAAAAAAAAAAAAACwAAABAAAAAAAAAAAAAAAA0AAAAQAAAAAAAAAAAAAAAOAAAAEAAAAAAAAAABAAAAAAAAABAAAAAAAAAAAQAAAAYAAAAQAAAAAAAAAAEAAAAHAAAAEAAAAAAAAAABAAAACAAAABAAAAAAAAAAAQAAAAoAAAAQAAAAAAAAAAEAAAALAAAAEAAAAAAAAAABAAAADQAAABAAAAAAAAAAAQAAAA4AAAAQAAAAAAAAAAQAAAAAAAAAEAAAAAAAAAAEAAAABgAAABAAAAAAAAAABAAAAAcAAAAQAAAAAAAAAAQAAAAIAAAAEAAAAAAAAAAEAAAACgAAABAAAAAAAAAABAAAAAsAAAAQAAAAAAAAAAQAAAANAAAAEAAAAAAAAAAEAAAADgAAABAAAAAAAAAABgAAAAAAAAAQAAAAAAAAAAYAAAAGAAAAEAAAAAAAAAAGAAAACAAAABAAAAAAAAAABgAAAAoAAAAQAAAAAAAAAAYAAAALAAAAEAAAAAAAAAAGAAAADQAAABAAAAAAAAAABgAAAA4AAAAQAAAAAAAAAAcAAAAAAAAAEAAAAAAAAAAHAAAABgAAABAAAAAAAAAABwAAAAgAAAAQAAAAAAAAAAcAAAAKAAAAEAAAAAAAAAAHAAAACwAAABAAAAAAAAAABwAAAA0AAAAQAAAAAAAAAAcAAAAOAAAA --metrics-client-id=c4c85bd6-057c-4022-b575-d3dbada7fab5 --service-request-channel-token=14620977264126654853
amanda            1384   0.0  0.0  4354588    740   ??  S    20Dec18   0:00.30 /Applications/Google Chrome.app/Contents/Versions/71.0.3578.98/Google Chrome Framework.framework/Helpers/crashpad_handler --monitor-self-annotation=ptype=crashpad-handler --database=/Users/amanda/Library/Application Support/Google/Chrome/Crashpad --metrics-dir=/Users/amanda/Library/Application Support/Google/Chrome --url=https://clients2.google.com/cr/report --annotation=channel= --annotation=plat=OS X --annotation=prod=Chrome_Mac --annotation=ver=71.0.3578.98 --handshake-fd=8
amanda            1175   0.0  0.0  4379956   2344   ??  S    20Dec18   0:03.54 /System/Library/Frameworks/CoreServices.framework/Frameworks/Metadata.framework/Versions/A/Support/mdwrite
amanda            1162   0.0  0.1  4389600  13408   ??  S    20Dec18   0:25.16 /System/Library/PrivateFrameworks/CallHistory.framework/Support/CallHistorySyncHelper
amanda            1153   0.0  0.0  4860892      8   ??  Ss   20Dec18   0:00.08 /System/Library/Frameworks/Metal.framework/Versions/A/XPCServices/MTLCompilerService.xpc/Contents/MacOS/MTLCompilerService
amanda            1152   0.0  0.1  4926504   9468   ??  S    20Dec18   0:28.22 /System/Library/CoreServices/OSDUIHelper.app/Contents/MacOS/OSDUIHelper
amanda            1091   0.0  0.0  4351420    652   ??  S    19Dec18   0:00.38 /usr/libexec/USBAgent
amanda            1089   0.0  0.1  4987940   9668   ??  S    19Dec18   0:29.67 /System/Library/Frameworks/LocalAuthentication.framework/Support/coreautha.bundle/Contents/MacOS/coreautha
amanda            1076   0.0  0.1  4443432   8620   ??  S    19Dec18   0:06.54 /System/Library/PrivateFrameworks/ContextKit.framework/Versions/A/XPCServices/ContextService.xpc/Contents/MacOS/ContextService
amanda            1062   0.0  0.0  4379808   6028   ??  S    19Dec18   0:08.65 /System/Library/PrivateFrameworks/DistributedEvaluation.framework/Versions/A/XPCServices/com.apple.siri-distributed-evaluation.xpc/Contents/MacOS/com.apple.siri-distributed-evaluation
amanda            1060   0.0  0.0  4413764    948   ??  S    19Dec18   0:03.13 /System/Library/Frameworks/ApplicationServices.framework/Frameworks/ATS.framework/Support/atsd
amanda            1054   0.0  0.1  4389672   8760   ??  S    19Dec18   0:22.25 /System/Library/PrivateFrameworks/AppStoreDaemon.framework/Support/appstoreagent
amanda            1053   0.0  0.0  4351952   3328   ??  S    19Dec18   0:01.45 /System/Library/Frameworks/Security.framework/Versions/A/Resources/CloudKeychainProxy.bundle/Contents/MacOS/CloudKeychainProxy
amanda            1052   0.0  0.0  4387396   6768   ??  S    19Dec18   0:10.34 /usr/libexec/keyboardservicesd
amanda            1051   0.0  0.6  4778196  98280   ??  S    19Dec18   3:16.24 /System/Library/Services/AppleSpell.service/Contents/MacOS/AppleSpell
amanda            1043   0.0  0.0  4843484      8   ??  Ss   19Dec18   0:00.12 /System/Library/Frameworks/Metal.framework/Versions/A/XPCServices/MTLCompilerService.xpc/Contents/MacOS/MTLCompilerService
amanda            1041   0.0  0.0  4382688   3856   ??  S    19Dec18   0:02.32 /System/Library/PrivateFrameworks/IMDPersistence.framework/IMAutomaticHistoryDeletionAgent.app/Contents/MacOS/IMAutomaticHistoryDeletionAgent
amanda            1039   0.0  0.1  4991208  17428   ??  Ss   19Dec18   1:24.64 /System/Library/CoreServices/Siri.app/Contents/XPCServices/SiriNCService.xpc/Contents/MacOS/SiriNCService
amanda            1002   0.0  0.0  4349904   1028   ??  S    19Dec18   0:00.20 /usr/libexec/mobileactivationd
amanda             997   0.0  0.1  4407468   8408   ??  Ss   19Dec18   0:04.91 /System/Library/PrivateFrameworks/PhotoLibraryPrivate.framework/Versions/A/Frameworks/PhotoLibraryServices.framework/Versions/A/XPCServices/com.apple.photomodel.xpc/Contents/MacOS/com.apple.photomodel
amanda             996   0.0  0.0  4389836   3680   ??  Ss   19Dec18   0:07.66 /System/Library/PrivateFrameworks/FMClient.framework/Versions/A/XPCServices/FMIPClientXPCService.xpc/Contents/MacOS/FMIPClientXPCService
amanda             995   0.0  0.0  4377232   4080   ??  S    19Dec18   0:01.33 /usr/libexec/siriknowledged
amanda             994   0.0  0.0  4379924   3556   ??  Ss   19Dec18   0:08.15 /System/Library/Frameworks/iTunesLibrary.framework/Versions/A/XPCServices/com.apple.iTunesLibraryService.xpc/Contents/MacOS/com.apple.iTunesLibraryService
amanda             993   0.0  0.3  4456612  54084   ??  S    19Dec18   1:26.41 /System/Library/PrivateFrameworks/AssistantServices.framework/Versions/A/Support/assistant_service
amanda             991   0.0  0.0  4378900   2680   ??  Ss   19Dec18   0:03.21 /System/Library/Frameworks/iTunesLibrary.framework/Versions/A/XPCServices/com.apple.iTunesLibraryService.xpc/Contents/MacOS/com.apple.iTunesLibraryService
amanda             988   0.0  0.0  4342056      8   ??  Ss   19Dec18   0:00.02 /System/Library/Frameworks/AudioToolbox.framework/XPCServices/com.apple.audio.SandboxHelper.xpc/Contents/MacOS/com.apple.audio.SandboxHelper
amanda             984   0.0  0.0  4342140    540   ??  S    19Dec18   0:00.39 /System/Library/Frameworks/ColorSync.framework/Support/colorsync.useragent
amanda             979   0.0  0.1  5065220  11596   ??  S    19Dec18   0:35.92 /Library/Application Support/Adobe/Creative Cloud Libraries/CCLibrary.app/Contents/MacOS/../libs/node /Library/Application Support/Adobe/Creative Cloud Libraries/CCLibrary.app/Contents/MacOS/../js/server.js
amanda             978   0.0  0.1  4456632  18780   ??  Ss   19Dec18   0:15.14 /System/Library/PrivateFrameworks/AssistantServices.framework/Versions/A/XPCServices/media-indexer.xpc/Contents/MacOS/media-indexer
amanda             965   0.0  0.0  4407968   5900   ??  S    19Dec18   0:25.59 /System/Library/PrivateFrameworks/CommerceKit.framework/Resources/LaterAgent.app/Contents/MacOS/LaterAgent
amanda             964   0.0  0.1  4423608  14940   ??  S    19Dec18   0:34.64 /System/Library/PrivateFrameworks/CommerceKit.framework/Versions/A/Resources/storeassetd
amanda             962   0.0  0.1  4484124  14180   ??  S    19Dec18   0:09.99 /System/Library/PrivateFrameworks/CoreSuggestions.framework/Versions/A/Support/reversetemplated
amanda             961   0.0  0.0  4378072   1212   ??  S    19Dec18   0:00.52 /System/Library/PrivateFrameworks/CommerceKit.framework/Versions/A/Resources/storelegacy
amanda             959   0.0  0.0  4350968   2056   ??  S    19Dec18   0:00.61 /System/Library/CoreServices/Software Update.app/Contents/Resources/softwareupdate_notify_agent
amanda             949   0.0  0.0  4382008   4496   ??  S    19Dec18   6:01.17 /Applications/Utilities/Adobe Sync/CoreSync/Core Sync.app/Contents/Frameworks/AdobeCrashReporter.framework/Versions/A/AdobeCRDaemon.app/Contents/MacOS/AdobeCRDaemon 947Core Sync 4.1.0.29 /Applications/Utilities/Adobe Sync/CoreSync/Core Sync.app/Contents/Resources/CreativeCloudIcons.icns /Applications/Utilities/Adobe Sync/CoreSync/Core Sync.app/Contents/Frameworks/AdobeCrashReporter.framework/Versions/A/Adobe Crash Reporter.app/Contents/MacOS/Adobe Crash Reporter 0          Adobe Sync
amanda             948   0.0  0.1  5045968  10476   ??  S    19Dec18   0:37.02 /Applications/Utilities/Adobe Creative CloudExperience/CCXProcess/CCXProcess.app/Contents/MacOS/../libs/node /Applications/Utilities/Adobe Creative Cloud Experience/CCXProcess/CCXProcess.app/Contents/MacOS/../js/main.js
amanda             947   0.0  0.2  5004948  30304   ??  S    19Dec18  15:17.89 /Applications/Utilities/Adobe Sync/CoreSync/Core Sync.app/Contents/MacOS/Core Sync
amanda             943   0.0  0.0  4378412   4508   ??  S    19Dec18   5:37.58 /Library/Application Support/Adobe/Adobe Desktop Common/ADS/Adobe Desktop Service.app/Contents/Frameworks/AdobeCrashReporter.framework/Versions/A/AdobeCRDaemon.app/Contents/MacOS/AdobeCRDaemon 938 Adobe Desktop Service 4.7 /Library/Application Support/Adobe/Adobe Desktop Common/ADS/Adobe Desktop Service.app/Contents/Resources/AdobeDesktopService.icns /Library/Application Support/Adobe/Adobe Desktop Common/ADS/Adobe Desktop Service.app/Contents/Frameworks/AdobeCrashReporter.framework/Versions/A/Adobe Crash Reporter.app/Contents/MacOS/Adobe Crash Reporter 0          Adobe Desktop Service 1 1
amanda             941   0.0  0.0  4870108      8   ??  Ss   19Dec18   0:00.07 /System/Library/Frameworks/Metal.framework/Versions/A/XPCServices/MTLCompilerService.xpc/Contents/MacOS/MTLCompilerService
amanda             940   0.0  0.0  4350276    668   ??  S    19Dec18   0:00.39 /System/Library/PrivateFrameworks/ToneLibrary.framework/Versions/A/XPCServices/com.apple.tonelibraryd.xpc/Contents/MacOS/com.apple.tonelibraryd
amanda             938   0.0  1.6  6107428 264220   ??  S    19Dec18  30:07.29 /Library/Application Support/Adobe/Adobe Desktop Common/ADS/Adobe Desktop Service.app/Contents/MacOS/Adobe Desktop Service --onOSstartup=true --showwindow=false --waitForRegistration=true
amanda             937   0.0  0.0  4378760    900   ??  Ss   19Dec18   0:00.62 /System/Library/Frameworks/VideoToolbox.framework/Versions/A/XPCServices/VTDecoderXPCService.xpc/Contents/MacOS/VTDecoderXPCService
amanda             934   0.0  0.0  4379436   4472   ??  S    19Dec18   5:38.37 /Applications/Utilities/Adobe Creative Cloud/ACC/Creative Cloud.app/Contents/Frameworks/AdobeCrashReporter.framework/Versions/A/AdobeCRDaemon.app/Contents/MacOS/AdobeCRDaemon 908 Creative Cloud 4.7 /Applications/Utilities/Adobe Creative Cloud/ACC/Creative Cloud.app/Contents/Resources/CreativeCloud.icns /Applications/Utilities/Adobe Creative Cloud/ACC/Creative Cloud.app/Contents/Frameworks/AdobeCrashReporter.framework/Versions/A/Adobe Crash Reporter.app/Contents/MacOS/Adobe Crash Reporter 0          Creative Cloud 1 1
amanda             931   0.0  0.0  4315172      8   ??  Ss   19Dec18   0:00.01 /System/Library/Frameworks/AudioToolbox.framework/XPCServices/com.apple.audio.SandboxHelper.xpc/Contents/MacOS/com.apple.audio.SandboxHelper
amanda             926   0.0  0.1  4415316  10140   ??  S    19Dec18   3:33.39 /Applications/Utilities/Adobe Application Manager/IPC/AdobeIPCBroker.app/Contents/MacOS/AdobeIPCBroker -launchedbyvulcan /Applications/Utilities/Adobe Creative Cloud/ACC/Creative Cloud.app/Contents/MacOS/Creative Cloud
amanda             921   0.0  0.1  4419240   9332   ??  Ss   19Dec18   0:54.96 /System/Library/Frameworks/WebKit.framework/Versions/A/XPCServices/com.apple.WebKit.Networking.xpc/Contents/MacOS/com.apple.WebKit.Networking
amanda             919   0.0  0.0  4378256   7888   ??  S    19Dec18   0:06.48 /System/Library/PrivateFrameworks/CoreRecents.framework/Versions/A/Support/recentsd
amanda             918   0.0  0.1  4767572  21924   ??  S    19Dec18   1:00.42 /System/Library/Frameworks/CoreServices.framework/Frameworks/Metadata.framework/Versions/A/Support/corespotlightd
amanda             915   0.0  0.0  4351524    680   ??  S    19Dec18   0:00.39 /System/Library/Frameworks/CryptoTokenKit.framework/ctkd -tw
amanda             914   0.0  0.0  4351080   1108   ??  S    19Dec18   0:00.48 /System/Library/Frameworks/CryptoTokenKit.framework/ctkahp.bundle/Contents/MacOS/ctkahp
amanda             912   0.0  0.1  4486992  23132   ??  S    19Dec18   1:44.55 /Library/Application Support/Symantec/Silo/NFM/SymUIAgent/Norton.app/Contents/MacOS/Norton
amanda             909   0.0  0.1  4416612   9608   ??  S    19Dec18   0:38.11 /System/Library/PrivateFrameworks/Noticeboard.framework/Versions/A/Resources/nbagent.app/Contents/MacOS/nbagent
amanda             906   0.0  0.0  4378136   2848   ??  S    19Dec18   2:18.28 /System/Library/CoreServices/cloudpaird
amanda             905   0.0  0.0  4912240   5824   ??  S    19Dec18   0:27.42 /System/Library/CoreServices/AirPlayUIAgent.app/Contents/MacOS/AirPlayUIAgent --launchd
amanda             904   0.0  0.0  4382960   2044   ??  S    19Dec18   0:01.40 /Library/Application Support/Adobe/AdobeGCClient/AGMService -mode=logon
amanda             900   0.0  0.0  4377684   1580   ??  S    19Dec18   0:02.88 /System/Library/Image Capture/Support/icdd
amanda             899   0.0  0.1  4408184  12912   ??  S    19Dec18   1:07.18 /System/Library/CoreServices/Siri.app/Contents/MacOS/Siri launchd
amanda             898   0.0  0.0  4377676   2936   ??  S    19Dec18   0:01.90 /usr/libexec/dmd
amanda             896   0.0  0.1  4441312  11352   ??  S    19Dec18   2:28.54 /Library/Application Support/iGlasses3/iGlasses.app/Contents/MacOS/iGlasses
amanda             894   0.0  0.0  4376384   1448   ??  S    19Dec18   0:00.97 /System/Library/CoreServices/SocialPushAgent.app/Contents/MacOS/SocialPushAgent
amanda             892   0.0  0.0  4349828    564   ??  S    19Dec18   0:00.42 /System/Library/PrivateFrameworks/CoreSpeech.framework/corespeechd
amanda             891   0.0  0.0  4884452      8   ??  Ss   19Dec18   0:00.73 /System/Library/Frameworks/Metal.framework/Versions/A/XPCServices/MTLCompilerService.xpc/Contents/MacOS/MTLCompilerService
amanda             882   0.0  0.0  4377216   3204   ??  S    19Dec18   0:02.98 /System/Library/PrivateFrameworks/FileProvider.framework/Support/fileproviderd
amanda             881   0.0  0.0  4350288   1128   ??  S    19Dec18   0:00.73 /System/Library/Frameworks/MediaAccessibility.framework/Versions/A/XPCServices/com.apple.accessibility.mediaaccessibilityd.xpc/Contents/MacOS/com.apple.accessibility.mediaaccessibilityd
amanda             880   0.0  0.0  4350992   1792   ??  S    19Dec18   0:01.08 /usr/libexec/findmydevice-user-agent
amanda             879   0.0  0.0  4879324      8   ??  Ss   19Dec18   0:00.12 /System/Library/Frameworks/Metal.framework/Versions/A/XPCServices/MTLCompilerService.xpc/Contents/MacOS/MTLCompilerService
amanda             878   0.0  0.1  4927940   8936   ??  S    19Dec18   0:33.61 /System/Library/CoreServices/NowPlayingTouchUI.app/Contents/MacOS/NowPlayingTouchUI
amanda             876   0.0  0.0  4864708      8   ??  Ss   19Dec18   0:00.56 /System/Library/Frameworks/Metal.framework/Versions/A/XPCServices/MTLCompilerService.xpc/Contents/MacOS/MTLCompilerService
amanda             875   0.0  0.1  4394776  16948   ??  S    19Dec18   0:55.44 /usr/libexec/knowledge-agent
amanda             873   0.0  0.0  4378144    884   ??  S    19Dec18   0:00.59 /System/Library/CoreServices/Menu Extras/SafeEjectGPUExtra.menu/Contents/XPCServices/SafeEjectGPUService.xpc/Contents/MacOS/SafeEjectGPUService
amanda             872   0.0  0.0  4822332      8   ??  S    19Dec18   0:00.02 SafeEjectGPUAgent
amanda             871   0.0  0.0  4401344   2500   ??  Ss   19Dec18   0:33.29 /System/Library/Frameworks/WebKit.framework/Versions/A/XPCServices/com.apple.WebKit.Networking.xpc/Contents/MacOS/com.apple.WebKit.Networking
amanda             870   0.0  0.0 106664844   5532   ??  Ss   19Dec18   0:18.97 /System/Library/Frameworks/WebKit.framework/Versions/A/XPCServices/com.apple.WebKit.WebContent.xpc/Contents/MacOS/com.apple.WebKit.WebContent
amanda             869   0.0  0.0  4378028   5056   ??  Ss   19Dec18   0:06.00 /System/Library/PrivateFrameworks/IMFoundation.framework/XPCServices/IMRemoteURLConnectionAgent.xpc/Contents/MacOS/IMRemoteURLConnectionAgent
amanda             868   0.0  0.0  4377312   1804   ??  S    19Dec18   1:42.21 /usr/libexec/SafariCloudHistoryPushAgent
amanda             866   0.0  0.1  4400124  15440   ??  S    19Dec18   0:33.76 /System/Library/PrivateFrameworks/SafariSafeBrowsing.framework/com.apple.Safari.SafeBrowsing.Service
amanda             864   0.0  0.0  4879324      8   ??  Ss   19Dec18   0:00.26 /System/Library/Frameworks/Metal.framework/Versions/A/XPCServices/MTLCompilerService.xpc/Contents/MacOS/MTLCompilerService
amanda             863   0.0  0.0  4378136   2232   ??  S    19Dec18   0:00.75 /usr/libexec/SafariNotificationAgent
amanda             862   0.0  0.0  4350328   1472   ??  S    19Dec18   0:13.46 /System/Library/Frameworks/ApplicationServices.framework/Versions/A/Frameworks/HIServices.framework/Versions/A/XPCServices/com.apple.hiservices-xpcservice.xpc/Contents/MacOS/com.apple.hiservices-xpcservice
amanda             861   0.0  0.0  4377016   5656   ??  S    19Dec18   0:01.14 /usr/libexec/videosubscriptionsd
amanda             860   0.0  0.0  4350916    736   ??  S    19Dec18   0:00.53 /usr/libexec/spindump_agent
amanda             855   0.0  0.0  4914156   4228   ??  Ss   19Dec18   0:14.95 /Applications/iTunes.app/Contents/XPCServices/VisualizerService.xpc/Contents/MacOS/VisualizerService
amanda             854   0.0  0.0  4377496   1400   ??  S    19Dec18   0:00.91 /System/Library/PrivateFrameworks/BookKit.framework/Versions/A/XPCServices/com.apple.BKAgentService.xpc/Contents/MacOS/com.apple.BKAgentService
amanda             853   0.0  0.1  4384944  10660   ??  S    19Dec18   1:38.07 /System/Library/PrivateFrameworks/CallHistory.framework/Support/CallHistoryPluginHelper
amanda             850   0.0  0.0  4378292   2300   ??  S    19Dec18   0:00.82 /System/Library/Frameworks/AudioToolbox.framework/AudioComponentRegistrar
amanda             849   0.0  0.1  4924608   9740   ??  Ss   19Dec18   0:31.07 /System/Library/CoreServices/Dock.app/Contents/XPCServices/com.apple.dock.extra.xpc/Contents/MacOS/com.apple.dock.extra
amanda             848   0.0  0.0  4380512   3520   ??  S    19Dec18   0:01.59 /System/Library/CoreServices/pbs
amanda             847   0.0  0.1  4879324  13032   ??  Ss   19Dec18   0:00.81 /System/Library/Frameworks/Metal.framework/Versions/A/XPCServices/MTLCompilerService.xpc/Contents/MacOS/MTLCompilerService
amanda             844   0.0  0.0  4376824   2020   ??  S    19Dec18   0:00.90 /System/Library/Frameworks/LocalAuthentication.framework/Support/coreauthd
amanda             843   0.0  0.1  4391112  21020   ??  S    19Dec18   0:17.36 /System/Library/PrivateFrameworks/SafariShared.framework/Versions/A/XPCServices/com.apple.Safari.History.xpc/Contents/MacOS/com.apple.Safari.History
amanda             841   0.0  0.1  4435040   8580   ??  Ss   19Dec18   0:32.17 /Applications/Utilities/Adobe Sync/CoreSync/Core Sync.app/Contents/PlugIns/ACCFinderSync.appex/Contents/MacOS/ACCFinderSync
amanda             839   0.0  0.0  4350496   4160   ??  Ss   19Dec18   0:17.32 /System/Library/PrivateFrameworks/CoreWLANKit.framework/Versions/A/XPCServices/WiFiProxy.xpc/Contents/MacOS/WiFiProxy
amanda             838   0.0  0.0  4879324      8   ??  Ss   19Dec18   0:00.21 /System/Library/Frameworks/Metal.framework/Versions/A/XPCServices/MTLCompilerService.xpc/Contents/MacOS/MTLCompilerService
amanda             835   0.0  0.0  4879324      8   ??  Ss   19Dec18   0:00.21 /System/Library/Frameworks/Metal.framework/Versions/A/XPCServices/MTLCompilerService.xpc/Contents/MacOS/MTLCompilerService
amanda             834   0.0  0.0  4350680   1656   ??  S    19Dec18   0:01.16 /usr/libexec/SidecarRelay
amanda             831   0.0  0.5  5111540  77304   ??  S    19Dec18   1:06.97 /System/Library/CoreServices/Spotlight.app/Contents/MacOS/Spotlight
amanda             825   0.0  1.7  5367148 285956   ??  S    19Dec18   7:21.15 /System/Library/CoreServices/Finder.app/Contents/MacOS/Finder
amanda             824   0.0  0.2  5044900  27316   ??  S    19Dec18   5:18.94 /System/Library/CoreServices/SystemUIServer.app/Contents/MacOS/SystemUIServer
amanda             823   0.0  0.2  5023220  26220   ??  S    19Dec18   2:32.83 /System/Library/CoreServices/Dock.app/Contents/MacOS/Dock
amanda             822   0.0  0.6  5298584 108732   ??  S    19Dec18   2:10.69 /Applications/iTunes.app/Contents/MacOS/iTunes -psn_0_258111
amanda             819   0.0  0.5  6050140  78144   ??  S    19Dec18  15:58.27 /Applications/Slack.app/Contents/MacOS/Slack-psn_0_249917
amanda             817   0.0  0.0  4387596   3736   ??  S    19Dec18   0:10.70 /System/Library/PrivateFrameworks/AssetCacheServices.framework/Versions/A/XPCServices/AssetCacheLocatorService.xpc/Contents/MacOS/AssetCacheLocatorService -a
amanda             815   0.0  0.1  4392512   9412   ??  S    19Dec18   0:17.42 /System/Library/PrivateFrameworks/CloudServices.framework/Versions/A/XPCServices/com.apple.sbd.xpc/Contents/MacOS/com.apple.sbd
amanda             811   0.0  1.1  5889276 182196   ??  S    19Dec18  26:49.31 /Applications/Mail.app/Contents/MacOS/Mail -psn_0_233529
amanda             808   0.0  0.1  4409560  17600   ??  S    19Dec18   5:18.30 /System/Library/PrivateFrameworks/GeoServices.framework/Versions/A/XPCServices/com.apple.geod.xpc/Contents/MacOS/com.apple.geod
amanda             807   0.0  0.0  4429256   4184   ??  Ss   19Dec18   0:06.36 /System/Library/Frameworks/MediaLibrary.framework/Versions/A/XPCServices/com.apple.MediaLibraryService.xpc/Contents/MacOS/com.apple.MediaLibraryService
amanda             805   0.0  0.0  4379600   2260   ??  S    19Dec18   0:12.67 /System/Library/PrivateFrameworks/CoreFollowUp.framework/Versions/A/Support/followupd
amanda             801   0.0  0.0  4393940   3436   ??  Ss   19Dec18   0:04.83 /System/Library/PrivateFrameworks/CloudDocsDaemon.framework/XPCServices/ContainerMetadataExtractor.xpc/Contents/MacOS/ContainerMetadataExtractor
amanda             800   0.0  0.0  4376832    724   ??  S    19Dec18   0:00.67 /System/Library/Frameworks/CoreServices.framework/Versions/A/Frameworks/DictionaryServices.framework/Versions/A/XPCServices/com.apple.DictionaryServiceHelper.xpc/Contents/MacOS/com.apple.DictionaryServiceHelper
amanda             799   0.0  0.5  4524324  79156   ??  S    19Dec18  14:43.03 /System/Library/PrivateFrameworks/PhotoAnalysis.framework/Versions/A/Support/photoanalysisd
amanda             798   0.0  0.1  4418648  15252   ??  Ss   19Dec18   0:40.67 /System/Library/PrivateFrameworks/PhotoLibraryPrivate.framework/Versions/A/Frameworks/PhotoLibraryServices.framework/Versions/A/XPCServices/com.apple.photomoments.xpc/Contents/MacOS/com.apple.photomoments
amanda             794   0.0  0.0  4349784   1272   ??  Ss   19Dec18   0:01.58 /System/Library/PrivateFrameworks/IMFoundation.framework/XPCServices/IMRemoteURLConnectionAgent.xpc/Contents/MacOS/IMRemoteURLConnectionAgent
amanda             793   0.0  0.0  4380296   1756   ??  S    19Dec18   0:02.81 /System/Library/CoreServices/ScopedBookmarkAgent
amanda             791   0.0  0.1  4467232  24300   ??  S    19Dec18   2:07.24 /System/Library/PrivateFrameworks/AssistantServices.framework/Versions/A/Support/assistantd
amanda             790   0.0  0.0  4378824    908   ??  S    19Dec18   0:02.09 /usr/libexec/swcd
amanda             789   0.0  0.0  4378736   1360   ??  S    19Dec18   0:02.55 /System/Library/CoreServices/backgroundtaskmanagementagent
amanda             788   0.0  0.1  4396260  14300   ??  S    19Dec18   2:11.59 /System/Library/PrivateFrameworks/CommerceKit.framework/Versions/A/Resources/commerce
amanda             785   0.0  0.2  4448492  38360   ??  S    19Dec18   6:14.83 /System/Library/PrivateFrameworks/PhotoLibraryPrivate.framework/Versions/A/Support/photolibraryd
amanda             777   0.0  0.0  4376480   1708   ??  S    19Dec18   0:00.58 /System/Library/PrivateFrameworks/QuickLookThumbnailing.framework/Support/com.apple.quicklook.ThumbnailsAgent
amanda             775   0.0  0.0  4382580    636   ??  S    19Dec18   0:00.58 /System/Library/PrivateFrameworks/CommerceKit.framework/Versions/A/Resources/storedownloadd
amanda             774   0.0  0.1  4463404  17676   ??  S    19Dec18   1:26.06 /System/Library/CoreServices/cloudphotosd.app/Contents/MacOS/cloudphotosd
amanda             773   0.0  0.0  4381072   5112   ??  S    19Dec18   0:10.21 /System/Library/CoreServices/diagnostics_agent
amanda             772   0.0  0.1  4389712  22428   ??  S    19Dec18   3:26.57 /System/Library/PrivateFrameworks/CloudDocsDaemon.framework/Versions/A/Support/bird
amanda             771   0.0  0.0  4879324      8   ??  Ss   19Dec18   0:00.22 /System/Library/Frameworks/Metal.framework/Versions/A/XPCServices/MTLCompilerService.xpc/Contents/MacOS/MTLCompilerService
amanda             770   0.0  0.0  4382392   4528   ??  S    19Dec18   0:08.25 /System/Library/PrivateFrameworks/CacheDelete.framework/deleted
amanda             769   0.0  0.0  4349768    604   ??  Ss   19Dec18   0:00.40 /System/Library/CoreServices/NotificationCenter.app/Contents/XPCServices/com.apple.notificationcenterui.WeatherSummary.xpc/Contents/MacOS/com.apple.notificationcenterui.WeatherSummary
amanda             768   0.0  0.0  4415356   6404   ??  S    19Dec18   0:28.04 /System/Library/CoreServices/CoreLocationAgent.app/Contents/MacOS/CoreLocationAgent
amanda             767   0.0  0.0  4376444    916   ??  S    19Dec18   0:00.68 /System/Library/PrivateFrameworks/CharacterPicker.framework/Versions/A/XPCServices/com.apple.CharacterPicker.FileService.xpc/Contents/MacOS/com.apple.CharacterPicker.FileService
amanda             765   0.0  0.1  4385184  13840   ??  Ss   19Dec18   1:22.59 /System/Library/PrivateFrameworks/CalendarNotification.framework/Versions/A/XPCServices/CalNCService.xpc/Contents/MacOS/CalNCService
amanda             764   0.0  0.0  4879324      8   ??  Ss   19Dec18   0:00.15 /System/Library/Frameworks/Metal.framework/Versions/A/XPCServices/MTLCompilerService.xpc/Contents/MacOS/MTLCompilerService
amanda             763   0.0  0.0  4349732   1240   ??  S    19Dec18   0:00.83 /System/Library/PrivateFrameworks/MediaRemote.framework/Support/mediaremoteagent
amanda             762   0.0  0.0  4351524   3940   ??  S    19Dec18   0:10.94 /System/Library/PrivateFrameworks/CommerceKit.framework/Versions/A/Resources/storeaccountd
amanda             761   0.0  0.0  4378028   5168   ??  Ss   19Dec18   0:05.04 /System/Library/PrivateFrameworks/IMFoundation.framework/XPCServices/IMRemoteURLConnectionAgent.xpc/Contents/MacOS/IMRemoteURLConnectionAgent
amanda             760   0.0  0.0  4390756   6928   ??  S    19Dec18   0:12.12 /usr/libexec/fmfd
amanda             759   0.0  0.3  4645460  42336   ??  S    19Dec18   0:43.04 /System/Library/CoreServices/iconservicesagent
amanda             758   0.0  0.0  4383340   6120   ??  S    19Dec18   2:19.84 /System/Library/PrivateFrameworks/UserActivity.framework/Agents/useractivityd
amanda             757   0.0  0.1  4525488  21632   ??  S    19Dec18   1:49.89 /System/Library/PrivateFrameworks/MessagesKit.framework/Resources/soagent.app/Contents/MacOS/soagent
amanda             755   0.0  0.0  4377760   4508   ??  S    19Dec18   0:59.45 /System/Library/PrivateFrameworks/ViewBridge.framework/Versions/A/XPCServices/ViewBridgeAuxiliary.xpc/Contents/MacOS/ViewBridgeAuxiliary
amanda             752   0.0  0.0  4378096    972   ??  S    19Dec18   0:00.76 /System/Library/PrivateFrameworks/FamilyCircle.framework/Versions/A/Resources/familycircled
amanda             748   0.0  0.0  4404208   5972   ??  S    19Dec18   0:25.44 /System/Library/CoreServices/Keychain CircleNotification.app/Contents/MacOS/Keychain Circle Notification
amanda             747   0.0  0.0  4349784   2340   ??  S    19Dec18   0:00.75 /System/Library/CoreServices/EscrowSecurityAlert.app/Contents/MacOS/EscrowSecurityAlert
amanda             746   0.0  0.0  4380540   3120   ??  S    19Dec18   0:02.74 /System/Library/PrivateFrameworks/ProtectedCloudStorage.framework/Helpers/ProtectedCloudKeySyncing
amanda             745   0.0  0.0  4404504   3592   ??  S    19Dec18   0:03.31 /System/Library/PrivateFrameworks/CloudPhotoServices.framework/Versions/A/Frameworks/CloudPhotosConfigurationXPC.framework/Versions/A/XPCServices/com.apple.CloudPhotosConfiguration.xpc/Contents/MacOS/com.apple.CloudPhotosConfiguration
amanda             744   0.0  0.0  4380208   1596   ??  S    19Dec18   0:00.98 /System/Library/PrivateFrameworks/CoreCDP.framework/Versions/A/Resources/cdpd
amanda             743   0.0  0.0  4381412   4868   ??  S    19Dec18   0:08.07 /System/Library/CoreServices/sharedfilelistd
amanda             742   0.0  0.3  4443976  50264   ??  S    19Dec18   6:59.63 /System/Library/PrivateFrameworks/CloudKitDaemon.framework/Support/cloudd
amanda             739   0.0  0.1  4392984   8872   ??  S    19Dec18   0:13.95 /usr/libexec/adprivacyd
amanda             737   0.0  0.1  4383604  11372   ??  S    19Dec18   2:21.82 /System/Library/CoreServices/SafariSupport.bundle/Contents/MacOS/SafariBookmarksSyncAgent
amanda             736   0.0  0.0  4414080   8160   ??  S    19Dec18   0:37.31 /System/Library/CoreServices/WiFiAgent.app/Contents/MacOS/WiFiAgent
amanda             735   0.0  0.6  4721776 101356   ??  S    19Dec18   4:13.41 /System/Library/PrivateFrameworks/CoreSuggestions.framework/Versions/A/Support/suggestd
amanda             733   0.0  0.2  4409864  27216   ??  S    19Dec18   6:29.76 /usr/libexec/sharingd
amanda             732   0.0  0.0  4387188   6604   ??  Ss   19Dec18   0:12.31 /System/Library/PrivateFrameworks/IMFoundation.framework/XPCServices/IMRemoteURLConnectionAgent.xpc/Contents/MacOS/IMRemoteURLConnectionAgent
amanda             729   0.0  0.1  4390524   9984   ??  S    19Dec18   0:17.45 /System/Library/PrivateFrameworks/PassKitCore.framework/passd
amanda             728   0.0  0.0  4408184   6012   ??  S    19Dec18   0:30.02 /System/Library/CoreServices/talagent
amanda             727   0.0  0.1  4391004  14116   ??  S    19Dec18   0:20.99 /System/Library/PrivateFrameworks/CoreParsec.framework/parsecd
amanda             725   0.0  0.0  4376604   2288   ??  S    19Dec18   0:01.27 /System/Library/PrivateFrameworks/CommunicationsFilter.framework/CMFSyncAgent
amanda             723   0.0  0.0  4380348   8212   ??  S    19Dec18   2:13.47 /System/Library/Frameworks/ApplicationServices.framework/Frameworks/ATS.framework/Support/fontd
amanda             722   0.0  0.3  5297624  52448   ??  S    19Dec18   2:20.93 /System/Library/CoreServices/NotificationCenter.app/Contents/MacOS/NotificationCenter
amanda             721   0.0  0.0  4350304    624   ??  S    19Dec18   0:00.39 /System/Library/CoreServices/APFSUserAgent
amanda             720   0.0  0.3  4427692  44028   ??  S    19Dec18   4:39.01 /System/Library/PrivateFrameworks/CalendarAgent.framework/Executables/CalendarAgent
amanda             719   0.0  0.0  4379072   1564   ??  S    19Dec18   0:02.89 /usr/libexec/networkserviceproxy
amanda             717   0.0  0.2  4953056  32560   ??  S    19Dec18   2:18.13 /System/Library/CoreServices/ControlStrip.app/Contents/MacOS/ControlStrip
amanda             716   0.0  0.1  4384280  11824   ??  S    19Dec18   1:22.28 /usr/libexec/nsurlstoraged
amanda             715   0.0  0.1  5126512  10020   ??  Ss   19Dec18   1:14.84 /System/Library/Input Methods/EmojiFunctionRowIM.app/Contents/PlugIns/EmojiFunctionRowIM_Extension.appex/Contents/MacOS/EmojiFunctionRowIM_Extension
amanda             714   0.0  0.0  4897840   5308   ??  Ss   19Dec18   0:25.22 /System/Library/Input Methods/PressAndHold.app/Contents/PlugIns/PAH_Extension.appex/Contents/MacOS/PAH_Extension
amanda             713   0.0  0.1  4394448  10412   ??  S    19Dec18   3:09.61 /usr/libexec/nsurlsessiond
amanda             712   0.0  0.1  4388524  17256   ??  S    19Dec18   0:27.50 /usr/sbin/usernoted
amanda             711   0.0  0.0  4391568   8324   ??  S    19Dec18   0:27.31 /System/Library/PrivateFrameworks/AuthKit.framework/Versions/A/Support/akd
amanda             710   0.0  0.1  4393540  21200   ??  S    19Dec18   0:54.31 /usr/libexec/routined LAUNCHED_BY_LAUNCHD
amanda             708   0.0  0.0  4378232   5684   ??  S    19Dec18   0:23.35 /usr/libexec/rapportd
amanda             706   0.0  0.0  4381672   7016   ??  S    19Dec18   0:29.34 /usr/libexec/pkd
amanda             705   0.0  0.0  4380768   3648   ??  S    19Dec18   0:19.12 /System/Library/Frameworks/InputMethodKit.framework/Resources/imklaunchagent
amanda             704   0.0  0.0  4349780   3576   ??  S    19Dec18   0:10.64 /System/Library/Frameworks/AddressBook.framework/Executables/ContactsAccountsService
amanda             703   0.0  0.2  4435784  35960   ??  S    19Dec18   0:52.56 /System/Library/PrivateFrameworks/IMDPersistence.framework/XPCServices/IMDPersistenceAgent.xpc/Contents/MacOS/IMDPersistenceAgent
amanda             702   0.0  0.0  4384052   6592   ??  S    19Dec18   0:08.81 /System/Library/PrivateFrameworks/TCC.framework/Resources/tccd
amanda             701   0.0  0.0  4384520   6684   ??  S    19Dec18   0:16.67 /usr/libexec/secinitd
amanda             700   0.0  0.1  4394024  12708   ??  S    19Dec18   0:31.98 /System/Library/PrivateFrameworks/IMCore.framework/imagent.app/Contents/MacOS/imagent
amanda             699   0.0  0.0  4377876   1068   ??  S    19Dec18   0:01.19 /usr/libexec/languageassetd --firstLogin
amanda             698   0.0  0.0  4381484   5832   ??  S    19Dec18   0:14.54 /System/Library/PrivateFrameworks/HomeKitDaemon.framework/Support/homed
amanda             696   0.0  0.2  4406480  27888   ??  S    19Dec18   1:55.44 /System/Library/PrivateFrameworks/IDS.framework/identityservicesd.app/Contents/MacOS/identityservicesd
amanda             695   0.0  0.2  4523664  25844   ??  S    19Dec18   3:13.92 /System/Library/Frameworks/Accounts.framework/Versions/A/Support/accountsd
amanda             694   0.0  0.1  4393876  14976   ??  S    19Dec18   0:24.01 /System/Library/PrivateFrameworks/SyncedDefaults.framework/Support/syncdefaultsd
amanda             693   0.0  0.1  4394084  20888   ??  S    19Dec18   1:51.87 /System/Library/PrivateFrameworks/TelephonyUtilities.framework/callservicesd
amanda             691   0.0  0.0  4351952   2848   ??  S    19Dec18   0:02.68 /usr/libexec/pboard
amanda             690   0.0  0.0  4391828   7188   ??  S    19Dec18   0:49.99 /System/Library/Frameworks/CoreTelephony.framework/Support/CommCenter -L
amanda             686   0.0  0.0  4379284   6768   ??  S    19Dec18   3:44.66 /usr/libexec/UserEventAgent (Aqua)
amanda             472   0.0  0.0  4378484    644   ??  S    18Dec18   0:01.79 /System/Library/Frameworks/CoreServices.framework/Frameworks/Metadata.framework/Versions/A/Support/mdworker -s mdworker-sizing -c MDSSizingWorker -m com.apple.mdworker.sizing
amanda             418   0.0  0.2  4975812  27936   ??  Ss   18Dec18   3:00.81 /System/Library/CoreServices/loginwindow.app/Contents/MacOS/loginwindow console
amanda             324   0.0  0.1  4395588  16380   ??  S    18Dec18   1:48.66 /usr/libexec/secd
amanda             321   0.0  0.0  4350932   5600   ??  S    18Dec18   1:01.26 /usr/sbin/distnoted agent
amanda             319   0.0  0.2  4399268  28980   ??  S    18Dec18   7:14.95 /usr/libexec/trustd --agent
amanda             318   0.0  0.0  4386904   6020   ??  S    18Dec18   0:16.73 /usr/libexec/lsd
amanda             317   0.0  0.0  4351800   6280   ??  S    18Dec18   1:34.55 /usr/sbin/cfprefsd agent
amanda           22521   0.0  0.0  4300364    524 s002  U+    1:46PM   0:00.00 grep amanda
amanda           22413   0.0  0.2  4790272  38840   ??  S     1:41PM   0:00.12 /Applications/Google Chrome.app/Contents/Versions/71.0.3578.98/Google Chrome Helper.app/Contents/MacOS/Google Chrome Helper --type=renderer --field-trial-handle=18050009161147368515,12073003594094258993,131072 --service-pipe-token=5059901864008534936 --lang=en-US --metrics-client-id=c4c85bd6-057c-4022-b575-d3dbada7fab5 --enable-offline-auto-reload --enable-offline-auto-reload-visible-only --num-raster-threads=4 --enable-zero-copy --enable-gpu-memory-buffer-compositor-resources --enable-main-frame-before-activation --service-request-channel-token=5059901864008534936 --renderer-client-id=3216 --no-v8-untrusted-code-mitigations --seatbelt-client=285
amanda           22410   0.0  0.4  4815080  59000   ??  S     1:41PM   0:00.30 /Applications/Google Chrome.app/Contents/Versions/71.0.3578.98/Google Chrome Helper.app/Contents/MacOS/Google Chrome Helper --type=renderer --field-trial-handle=18050009161147368515,12073003594094258993,131072 --service-pipe-token=3323522104890747421 --lang=en-US --metrics-client-id=c4c85bd6-057c-4022-b575-d3dbada7fab5 --enable-offline-auto-reload --enable-offline-auto-reload-visible-only --num-raster-threads=4 --enable-zero-copy --enable-gpu-memory-buffer-compositor-resources --enable-main-frame-before-activation --service-request-channel-token=3323522104890747421 --renderer-client-id=3213 --no-v8-untrusted-code-mitigations --seatbelt-client=145
amanda           22408   0.0  0.4  4815076  59500   ??  S     1:41PM   0:00.41 /Applications/Google Chrome.app/Contents/Versions/71.0.3578.98/Google Chrome Helper.app/Contents/MacOS/Google Chrome Helper --type=renderer --field-trial-handle=18050009161147368515,12073003594094258993,131072 --service-pipe-token=3161913386531545430 --lang=en-US --metrics-client-id=c4c85bd6-057c-4022-b575-d3dbada7fab5 --enable-offline-auto-reload --enable-offline-auto-reload-visible-only --num-raster-threads=4 --enable-zero-copy --enable-gpu-memory-buffer-compositor-resources --enable-main-frame-before-activation --service-request-channel-token=3161913386531545430 --renderer-client-id=3211 --no-v8-untrusted-code-mitigations --seatbelt-client=266
amanda           22403   0.0  0.8  4908208 134096   ??  S     1:40PM   0:03.27 /Applications/Google Chrome.app/Contents/Versions/71.0.3578.98/Google Chrome Helper.app/Contents/MacOS/Google Chrome Helper --type=renderer --field-trial-handle=18050009161147368515,12073003594094258993,131072 --service-pipe-token=11847648529536901504 --lang=en-US --metrics-client-id=c4c85bd6-057c-4022-b575-d3dbada7fab5 --enable-offline-auto-reload --enable-offline-auto-reload-visible-only --num-raster-threads=4 --enable-zero-copy --enable-gpu-memory-buffer-compositor-resources --enable-main-frame-before-activation --service-request-channel-token=11847648529536901504 --renderer-client-id=3206 --no-v8-untrusted-code-mitigations --seatbelt-client=205
amanda           22275   0.0  0.3  4822116  56940   ??  S     1:21PM   0:00.52 /Applications/Google Chrome.app/Contents/Versions/71.0.3578.98/Google Chrome Helper.app/Contents/MacOS/Google Chrome Helper --type=renderer --field-trial-handle=18050009161147368515,12073003594094258993,131072 --service-pipe-token=10828547691537106848 --lang=en-US --metrics-client-id=c4c85bd6-057c-4022-b575-d3dbada7fab5 --enable-offline-auto-reload --enable-offline-auto-reload-visible-only --num-raster-threads=4 --enable-zero-copy --enable-gpu-memory-buffer-compositor-resources --enable-main-frame-before-activation --service-request-channel-token=10828547691537106848 --renderer-client-id=3201 --no-v8-untrusted-code-mitigations --seatbelt-client=233
amanda           22271   0.0  0.3  4821096  56704   ??  S     1:20PM   0:00.33 /Applications/Google Chrome.app/Contents/Versions/71.0.3578.98/Google Chrome Helper.app/Contents/MacOS/Google Chrome Helper --type=renderer --field-trial-handle=18050009161147368515,12073003594094258993,131072 --service-pipe-token=9741075553642970197 --lang=en-US --metrics-client-id=c4c85bd6-057c-4022-b575-d3dbada7fab5 --enable-offline-auto-reload --enable-offline-auto-reload-visible-only --num-raster-threads=4 --enable-zero-copy --enable-gpu-memory-buffer-compositor-resources --enable-main-frame-before-activation --service-request-channel-token=9741075553642970197 --renderer-client-id=3200 --no-v8-untrusted-code-mitigations --seatbelt-client=254
amanda           22269   0.0  1.4  5008264 237228   ??  S     1:20PM   1:13.29 /Applications/Google Chrome.app/Contents/Versions/71.0.3578.98/Google Chrome Helper.app/Contents/MacOS/Google Chrome Helper --type=renderer --field-trial-handle=18050009161147368515,12073003594094258993,131072 --service-pipe-token=16759521736375997185 --lang=en-US --metrics-client-id=c4c85bd6-057c-4022-b575-d3dbada7fab5 --enable-offline-auto-reload --enable-offline-auto-reload-visible-only --num-raster-threads=4 --enable-zero-copy --enable-gpu-memory-buffer-compositor-resources --enable-main-frame-before-activation --service-request-channel-token=16759521736375997185 --renderer-client-id=3198 --no-v8-untrusted-code-mitigations --seatbelt-client=238
amanda           22267   0.0  0.7  4894424 121444   ??  S     1:19PM   0:02.99 /Applications/Google Chrome.app/Contents/Versions/71.0.3578.98/Google Chrome Helper.app/Contents/MacOS/Google Chrome Helper --type=renderer --field-trial-handle=18050009161147368515,12073003594094258993,131072 --service-pipe-token=10137989873323073114 --lang=en-US --metrics-client-id=c4c85bd6-057c-4022-b575-d3dbada7fab5 --enable-offline-auto-reload --enable-offline-auto-reload-visible-only --num-raster-threads=4 --enable-zero-copy --enable-gpu-memory-buffer-compositor-resources --enable-main-frame-before-activation --service-request-channel-token=10137989873323073114 --renderer-client-id=3196 --no-v8-untrusted-code-mitigations --seatbelt-client=234
amanda           22241   0.0  0.3  5087136  44632   ??  S     1:16PM   0:00.26 /private/var/folders/99/pccf2f9x1gz2y99n3m6hbdg40000gn/T/AppTranslocation/76BB7FC3-740A-4B11-BA03-58E8DE438C57/d/Visual Studio Code.app/Contents/Frameworks/Code Helper.app/Contents/MacOS/Code Helper /private/var/folders/99/pccf2f9x1gz2y99n3m6hbdg40000gn/T/AppTranslocation/76BB7FC3-740A-4B11-BA03-58E8DE438C57/d/Visual Studio Code.app/Contents/Resources/app/out/bootstrap-fork --type=searchService
amanda           22238   0.0  0.1  4363708  12996   ??  S     1:16PM   0:00.05 /System/Library/Frameworks/CoreServices.framework/Frameworks/Metadata.framework/Versions/A/Support/mdworker_shared -s mdworker -c MDSImporterWorker -m com.apple.mdworker.shared
amanda           22237   0.0  0.3  5093368  43564   ??  S     1:16PM   0:00.44 /private/var/folders/99/pccf2f9x1gz2y99n3m6hbdg40000gn/T/AppTranslocation/76BB7FC3-740A-4B11-BA03-58E8DE438C57/d/Visual Studio Code.app/Contents/Frameworks/Code Helper.app/Contents/MacOS/Code Helper /private/var/folders/99/pccf2f9x1gz2y99n3m6hbdg40000gn/T/AppTranslocation/76BB7FC3-740A-4B11-BA03-58E8DE438C57/d/Visual Studio Code.app/Contents/Resources/app/out/bootstrap-fork --type=watcherService
amanda           22236   0.0  0.7  5165860 116392   ??  S     1:16PM   0:04.62 /private/var/folders/99/pccf2f9x1gz2y99n3m6hbdg40000gn/T/AppTranslocation/76BB7FC3-740A-4B11-BA03-58E8DE438C57/d/Visual Studio Code.app/Contents/Frameworks/Code Helper.app/Contents/MacOS/Code Helper /private/var/folders/99/pccf2f9x1gz2y99n3m6hbdg40000gn/T/AppTranslocation/76BB7FC3-740A-4B11-BA03-58E8DE438C57/d/Visual Studio Code.app/Contents/Resources/app/out/bootstrap-fork --type=extensionHost
amanda           22226   0.0  1.1  5132268 177156   ??  S     1:15PM   0:05.39 /Applications/Notes.app/Contents/MacOS/Notes
amanda           22190   0.0  0.1  4395184  18200   ??  Ss   12:11PM   0:00.21 /System/Library/Frameworks/WebKit.framework/Versions/A/XPCServices/com.apple.WebKit.Storage.xpc/Contents/MacOS/com.apple.WebKit.Storage
amanda           22187   0.0  0.2  4387592  27068   ??  Ss   12:11PM   0:00.20 /System/Library/PrivateFrameworks/SafariShared.framework/Versions/A/XPCServices/com.apple.Safari.SearchHelper.xpc/Contents/MacOS/com.apple.Safari.SearchHelper
amanda           22186   0.0  0.1  4342748  14144   ??  Ss   12:11PM   0:00.04 /System/Library/PrivateFrameworks/SafariShared.framework/Versions/A/XPCServices/com.apple.Safari.ImageDecoder.xpc/Contents/MacOS/com.apple.Safari.ImageDecoder
amanda           22181   0.0  0.4  4429308  70072   ??  Ss   12:11PM   0:04.60 /System/Library/Frameworks/WebKit.framework/Versions/A/XPCServices/com.apple.WebKit.Networking.xpc/Contents/MacOS/com.apple.WebKit.Networking