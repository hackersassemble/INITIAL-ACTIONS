# INITIAL-ACTIONS

1) Unchecking AD - allows us to see how many servers and workstations are in the network, as well as information about users and their positions, and after unchecking AD we sorted it in order to sort out only what we need - we will show it to you later

2) The sharefinder is a way to determine where we have access to this user (to other computers).

3) Kerberos attack - pulls hashes from memory, if successfully removed and successfully decrypted - we are guaranteed domainAdmin

4) If we have system rights, with the command "hashdump" and "logonpasswords" we can pull hashes and mimics and we will have the password of a domain user, and sometimes even the domain admin

5) If we have found a login and hash of the admin domain and we have not been able to hash, we do the following command pth Domain\Admin pass (as hash), using the command shell dir \ip or hostname\c$ we check access to the server or workstations

6) If we find the login\pass domain of the administrator or user, we can put his token, the command looks like make_token Domain\Admin Pass , if you want to remove the token, the command rev2self

7) If the session has a process system , with the getsystem command you can raise the system rights in the session, point (4)

8) Do not forget to watch the processes with the command ps, there you can find the user, migrate to his process > Explore > Process list > then select the user process (the user must be different, not the one in the session) and press inject, select the SSL listener

9) After migrating to the new user you also need to remove balls to see where you can break through with it.

10) When you remove the balloons, at the end of the removal of the directory C:\ProgramData and there is sh.txt or shares.txt, download it and see how many "remote admin" in the textbook, if there is more than one, it means that you have access to another computer

11) Click on session > File Browser > write path\flie or hostname of the computer you have access to\c$, put there payload, I will give it to you later

12) Launch the package depends on its format eh or dll, I will explain later personally

13) To ping the server and workstation, we need p.bat, I will throw it in the group. Create a txt file, call it domains.txt, put there hostnames servers or minutes. Hostnames are taken from the withdrawn AD, with the script, they will show how to use

14) If you found a password, you can also run it through smb_login - an instrument in metasploit, I will give a metasploit and tell you how to use it. smb_login will show which servers or workstations, have access to these scripts

CREDITS: Learners Room @dtob1804
