Team Members: 
Roberto Manra robertmanra@csu.fullerton.edu
Declan Tran declantran@csu.fullerton.edu


How to run the program
1. Open a terminal and go to where the program files are loacted 

2. Clean up leftover IPC resources (optional)
Run:
ipcs -m
ipcs -q

Then for each shmid and msqid:
ipcrm -m <shmid>
ipcrm -q <msqid>

3. Delete old compiled files and previous outputs (optional)
Run:
rm -f sender recv keyfile.txt *__recv

4. Recompile the programs
Run:
g++ sender.cpp -o sender
g++ recv.cpp -o recv

5. Open a second terminal window or tab you'll need one for the receiver and one for the sender

6. In Terminal 1: Start the receiver
Run:
./recv

7. In Terminal 2: Run the sender
Run:
./sender keyfile.txt
(Should print: The number of bytes sent is: 13)

9. Check Terminal 1 (receiver)
(Should print: The number of bytes received is: 13)

