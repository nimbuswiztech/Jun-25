# Linux commands All

#### ✅ **Linux Commands (Clean & Renumbered)**

1. `pwd` – Print current working directory
2. `ls` – List files and directories
3. `ls -l` – Long listing format
4. `ls -lt` – Sort by modification time (recent first)
5. `ls -lrt` – Sort by time (oldest first), long format
6. `ls -a` – Show hidden files
7. `ls -l | wc -l` – Count number of files/folders
8. `ls -ltr | wc -l` – Count using long + time sort
9. `cd ..` – Move one directory up
10. `cd ../..` – Move two levels up
11. `cd /home/user/path` – Move to absolute path
12. `mkdir <directory_name>` – Create one directory
13. `mkdir dir1 dir2 dir3` – Create multiple directories
14. `mkdir -p dir1/dir2/dir3` – Create nested directories
15. `touch <file_name>` – Create empty file
16. `touch f1 f2 f3` – Create multiple files
17. `touch directory_name/filename` – Create file in a dir
18. `vi file_name` – Open file in vi editor
    * `i` → insert mode
    * `Esc :wq!` → save & quit
    * `Esc :q!` → quit without saving
19. `cat filename` – Display file content
20. `:/pattern` – Search pattern in `vi`
21. `:%s/old/new/g` – Replace all in file (vi)
22. `:1 s/old/new/g` – Replace in line 1 (vi)
23. `:5,$ s/old/new/g` – Replace from line 5 to end
24. `:1,5 s/old/new/g` – Replace from line 1 to 5
25. `wc filename` – Word, line, byte count
26. `wc -l f1` – Line count
27. `wc -w f1` – Word count
28. `wc -c f1` – Byte count
29. `wc -m f1` – Character count
30. `echo "statement"` – Print to terminal
31. `echo -e "line1\nline2"` – Multiline print
32. `>` – Redirect/overwrite output to file
33. `>>` – Append output to file
34. `du filename` – Disk usage of file
35. `du -sh filename` – Human-readable file size
36. `du -sh directory_name` – Size of directory
37. `du -sh *` – Size of all items in current dir
38. `head filename` – Show first 10 lines
39. `head -3 f1` – Show first 3 lines
40. `head -20 f1` – Show first 20 lines
41. `tail f1` – Show last 10 lines
42. `tail -2 f1` – Show last 2 lines
43. `tail -20 f1` – Show last 20 lines
44. `|` – Pipe output from one command to another
45. `head -10 file | tail -1` – Get 10th line
46. `head -8 f1 | tail -1 | wc -w` – Word count in 8th line
47. grep
48. grep -i "devops" f1
49. grep -in "pattern" filename
50. grep -ic "pattern" filename
51. grep -iw "devops" f1
52. grep -li "devops" \*
53. grep -ilr "devops" \*
54. grep -ie "devops" -e "teams" f1
55. grep -i "devops" file
56. grep -in "devops" file
57. grep -ic "devops" file
58. grep -iw "devops" file
59. grep -il "devops" \*
60. grep -ilR "devops" \*
61. grep -ie "pattern1" -ie "pattern2" -ie "pattern3" file
62. chown user:group file
63. chown user filename
64. sed
65. sed 's/pattern/change\_pattern/g' filename
66. sed -i 's/pattern/change\_pattern/g' filename
67. sed '2s/unix/linux/g' filename
68. sed '5,$s/pattern/change\_pattern/g' filename
69. sed '2s/development/devops/2' f2
70. sed -n '4p' f2
71. sed -n '144p' f2
72. sed '3d' f2
73. sed '30d' f2
74. Print 10 and 25 line content at a time? → (You can use: sed -n -e '10p' -e '25p' filename)
75. cp -i f2 f4
76. cut -d " " -f4 checklist
77. cut -d " " -f1 checklist
78. cut -d " " -f2,4 checklist
79. awk -F " " '{print $2}' checklist
80. awk -F " " '{print $4}' checklist
81. awk -F " " '{print $2,$4}' checklist
82. ps -ef | grep -i "service\_name"
83. ps -ef | grep -ie "jenkins" -e "tomcat"
84. ps -u "user\_name"
85. kill -9 "PID"



#### 📊 **Linux Command Table with Real-Time Scenarios**

| No. | Command                          | Description                 | Real-Time Use Case                                                             |
| --- | -------------------------------- | --------------------------- | ------------------------------------------------------------------------------ |
| 1   | `pwd`                            | Print current directory     | Useful to know your location in a deep folder structure while troubleshooting. |
| 2   | `ls`                             | List files/directories      | Quickly see what files are in your current working directory.                  |
| 3   | `ls -l`                          | Long listing format         | Check file permissions, owners, sizes, and timestamps.                         |
| 4   | `ls -lt`                         | Sort by time, newest first  | Identify which files were recently modified, useful for log files.             |
| 5   | `ls -lrt`                        | Sort by time, oldest first  | See the oldest file first, helps with archive and cleanup decisions.           |
| 6   | `ls -a`                          | Show hidden files           | View dotfiles like `.gitignore`, `.env` for editing or checking configs.       |
| 7   | \`ls -l                          | wc -l\`                     | Count number of files/folders                                                  |
| 8   | \`ls -ltr                        | wc -l\`                     | Count with long & time sort                                                    |
| 9   | `cd ..`                          | Go up one directory         | Navigate back in folder structure during config or deployment work.            |
| 10  | `cd ../..`                       | Go up two levels            | Quickly jump from nested to parent project root.                               |
| 11  | `cd /home/user/path`             | Move to absolute path       | Used in scripts or manually jumping to known working directories.              |
| 12  | `mkdir <dir_name>`               | Create a directory          | Create a folder for a new microservice component.                              |
| 13  | `mkdir dir1 dir2 dir3`           | Create multiple dirs        | Setup multiple staging or environment folders at once.                         |
| 14  | `mkdir -p dir1/dir2/dir3`        | Create nested dirs          | Setup a full directory structure for deployment automation.                    |
| 15  | `touch <file>`                   | Create empty file           | Create placeholder files like `.env`, `readme.md`.                             |
| 16  | `touch f1 f2 f3`                 | Create multiple files       | Quickly setup multiple test config files.                                      |
| 17  | `touch dir/filename`             | Create file in dir          | Add logs or config files to specific locations.                                |
| 18  | `vi filename`                    | Open file in vi             | Open and edit files directly from terminal.                                    |
| —   | `i`                              | Insert mode in vi           | Start typing or editing the content.                                           |
| —   | `Esc :wq!`                       | Save and force quit         | Save changes even to read-only files.                                          |
| —   | `Esc :q!`                        | Quit without saving         | Discard changes and exit vi.                                                   |
| 19  | `cat filename`                   | Display file content        | View configuration or output files quickly.                                    |
| 20  | `:/pattern`                      | Search pattern in vi        | Navigate to keyword while editing large files.                                 |
| 21  | `:%s/old/new/g`                  | Replace all in vi           | Replace all instances, e.g., change “staging” to “production”.                 |
| 22  | `:1 s/old/new/g`                 | Replace only on line 1      | Fix header or first line comment in a script.                                  |
| 23  | `:5,$ s/old/new/g`               | Replace from line 5 onward  | Skip metadata and edit only the actual content.                                |
| 24  | `:1,5 s/old/new/g`               | Replace lines 1 to 5        | Update copyright or version info in script headers.                            |
| 25  | `wc filename`                    | Word, line, byte count      | Quickly audit size and structure of a file.                                    |
| 26  | `wc -l f1`                       | Line count                  | Know how many lines exist in a log or script.                                  |
| 27  | `wc -w f1`                       | Word count                  | Analyze size or verbosity of notes or reports.                                 |
| 28  | `wc -c f1`                       | Byte count                  | Check file size before pushing to limited storage.                             |
| 29  | `wc -m f1`                       | Character count             | Check content size for fixed-width systems.                                    |
| 30  | `echo "statement"`               | Print to terminal           | Debug values in scripts or commands.                                           |
| 31  | `echo -e "line1\nline2"`         | Print multiline             | Simulate or test formatted output.                                             |
| 32  | `>`                              | Redirect output (overwrite) | Overwrite logs or config with new data.                                        |
| 33  | `>>`                             | Append output               | Add logs or output to an existing file without losing previous data.           |
| 34  | `du filename`                    | File disk usage             | Check how much space a file is taking.                                         |
| 35  | `du -sh filename`                | Human-readable file size    | Same as above, easier to read (e.g., MB/KB).                                   |
| 36  | `du -sh directory`               | Directory size              | See space usage by code or data folders.                                       |
| 37  | `du -sh *`                       | Size of all items           | Check which folders/files are consuming disk space.                            |
| 38  | `head filename`                  | Show first 10 lines         | Preview beginning of logs or config.                                           |
| 39  | `head -3 f1`                     | Show first 3 lines          | Check metadata/header of a file.                                               |
| 40  | `head -20 f1`                    | Show first 20 lines         | Inspect larger log or script start.                                            |
| 41  | `tail f1`                        | Show last 10 lines          | Check end of logs for recent entries.                                          |
| 42  | `tail -2 f1`                     | Show last 2 lines           | Check last few operations in logs.                                             |
| 43  | `tail -20 f1`                    | Show last 20 lines          | Get recent application errors from a log.                                      |
| 44  | \`                               | \` (pipe)                   | Pass output to next command                                                    |
| 45  | `head -10 file \| tail -1`       | Get 10th line               | Used to extract a specific line from file.                                     |
| 46  | `head -8 f1 \| tail -1 \| wc -w` | Word count of 8th line      | Analyze specific log or config content.                                        |

| No. | Command                                   | Description                           | Real-Time Use Case                                                   |
| --- | ----------------------------------------- | ------------------------------------- | -------------------------------------------------------------------- |
| 54  | `grep -i "devops" f1`                     | Case-insensitive search               | Find all mentions of “DevOps” in logs, regardless of case.           |
| 55  | `grep -in "pattern" filename`             | Case-insensitive search + line number | Locate functions in a script and show line numbers for editing.      |
| 56  | `grep -ic "pattern" filename`             | Count matches, case-insensitive       | Count how many times “error” appears in logs.                        |
| 57  | `grep -iw "devops" f1`                    | Match exact word, case-insensitive    | Search “devops” as a separate word, not substrings like “devops123”. |
| 58  | `grep -li "devops" *`                     | List files with match, ignore case    | Find which config files mention “devops”.                            |
| 59  | `grep -ilr "devops" *`                    | Recursive search for files with match | Search entire project folders for files containing “devops”.         |
| 60  | `grep -ie "devops" -e "teams" f1`         | Search multiple patterns              | Highlight if resume has “devops” or “teams”.                         |
| 61  | `grep -i "devops" file`                   | Search ignoring case                  | Same as 54, alternate usage.                                         |
| 62  | `grep -in "devops" file`                  | Search with line numbers              | Locate all “devops” mentions in README for refactoring.              |
| 63  | `grep -ic "devops" file`                  | Count occurrences                     | Count how many times “devops” appears in documentation.              |
| 64  | `grep -iw "devops" file`                  | Match exact word                      | Avoid partial matches like “devops-tools”.                           |
| 65  | `grep -il "devops" *`                     | List matching files                   | Like 58, used in audit checks.                                       |
| 66  | `grep -ilR "devops" *`                    | Recursive version of 65               | Audit all files in repo for usage of “devops”.                       |
| 67  | `grep -ie "pattern1" -ie "pattern2" file` | Match multiple keywords               | Search for “ERROR”, “FAIL”, or “CRITICAL” in logs.                   |
| 68  | `chown user:group file`                   | Change owner and group                | Assign Jenkins ownership to a config file.                           |
| 69  | `chown user filename`                     | Change only file owner                | Transfer file ownership from root to a dev user.                     |
| 70  | `sed`                                     | Stream editor for files               | Used for quick, scriptable edits in large files.                     |
| 71  | `sed 's/pattern/change/g' filename`       | Replace pattern globally              | Change all “http” to “https” in a URL list.                          |
| 72  | `sed -i 's/pattern/change/g' filename`    | In-place replacement                  | Replace environment in `.env` before deployment.                     |
| 73  | `sed '2s/unix/linux/g'`                   | Replace only on line 2                | Fix typo in instruction manual line 2.                               |
| 74  | `sed '5,$s/pattern/change/g'`             | Replace from line 5 onward            | Skip headers and modify logs below.                                  |
| 75  | `sed '2s/dev/devops/2' f2`                | Replace second occurrence on line 2   | Fix second mention of term in templated email.                       |
| 76  | `sed -n '4p' f2`                          | Print line 4                          | Extract version or key info from line 4.                             |
| 77  | `sed -n '144p' f2`                        | Print line 144                        | View specific error log line.                                        |
| 78  | `sed '3d' f2`                             | Delete line 3                         | Remove faulty entry from config.                                     |
| 79  | `sed '30d' f2`                            | Delete line 30                        | Cleanup deprecated instruction.                                      |
| 80  | `sed -n -e '10p' -e '25p'`                | Print lines 10 and 25                 | View summary or markers in logs.                                     |
| 81  | `cp -i f2 f4`                             | Copy with prompt if exists            | Safeguard against overwriting in prod.                               |
| 82  | `cut -d " " -f4 checklist`                | Extract 4th field                     | Get command executed from checklist.                                 |
| 83  | `cut -d " " -f1 checklist`                | Extract 1st field                     | Get date of log entries.                                             |
| 84  | `cut -d " " -f2,4 checklist`              | Extract multiple fields               | Fetch status and command from logs.                                  |
| 85  | `awk -F " " '{print $2}' checklist`       | Print 2nd field                       | Extract usernames from logs.                                         |
| 86  | `awk -F " " '{print $4}' checklist`       | Print 4th field                       | Get executed service names.                                          |
| 87  | `awk -F " " '{print $2,$4}' checklist`    | Print multiple fields                 | Match user and their action in audit log.                            |
| 88  | \`ps -ef                                  | grep -i "service\_name"\`             | Find process by name                                                 |
| 89  | \`ps -ef                                  | grep -ie "jenkins" -e "tomcat"\`      | Search multiple services                                             |
| 90  | `ps -u "user"`                            | Show user’s processes                 | See all jobs run by `deploy` user.                                   |
| 91  | `kill -9 PID`                             | Force kill a process                  | Terminate stuck or zombie deployment process.                        |

