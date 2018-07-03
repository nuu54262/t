```console
pentesterlab@2e642c30b796:/home/victim$ ls
pentesterlab@2e642c30b796:/home/victim$ ls -a
.  ..  .bash_history  .bash_logout  .bashrc  .profile
pentesterlab@2e642c30b796:/home/victim$ cat .bash_history 
ls
cp dk.sh dk6.sh
vi dk6.sh 
cd
cd
ls
git pull
cd
ls
uname
cat /etc/passwd
2213f137-429b-493c-aa92-0aca52af9286
```
```console
pentesterlab@faeac2a6f5af:/home$ ls
pentesterlab  victim14  victim20  victim27  victim33  victim4   victim46  victim52  victim59  victim65  victim71  victim78
victim0       victim15  victim21  victim28  victim34  victim40  victim47  victim53  victim6   victim66  victim72  victim79
victim1       victim16  victim22  victim29  victim35  victim41  victim48  victim54  victim60  victim67  victim73  victim8
victim10      victim17  victim23  victim3   victim36  victim42  victim49  victim55  victim61  victim68  victim74  victim80
victim11      victim18  victim24  victim30  victim37  victim43  victim5   victim56  victim62  victim69  victim75  victim9
victim12      victim19  victim25  victim31  victim38  victim44  victim50  victim57  victim63  victim7   victim76
victim13      victim2   victim26  victim32  victim39  victim45  victim51  victim58  victim64  victim70  victim77
pentesterlab@faeac2a6f5af:/home$ find /home/ -name .bash_history
/home/victim48/.bash_history
pentesterlab@faeac2a6f5af:/home$ cd victim48 
pentesterlab@faeac2a6f5af:/home/victim48$ cat .bash_history 
ls
cp dk.sh dk6.sh
vi dk6.sh 
cd
cd -
git status
git pull
cd
ls
uname
cat /etc/passwd
cp /etc/passwd ~/backup_passwd
./check_ptlab_key 2213f137-429b-493c-aa92-0aca52af9286
ls
cd
git status
git pull
cd
ls
cat /etc/passwd
```
```console
pentesterlab@877191309e41:/srv/victim99$ cat /etc/passwd
...
victim78:x:1079:1079::/home/victim78:/bin/bash
victim79:x:1080:1080::/home/victim79:/bin/bash
victim80:x:1081:1081::/home/victim80:/bin/bash
victim99:x:1082:1082::/srv/victim99:/bin/bash
pentesterlab@877191309e41:/srv/victim99$ find /srv/victim99/ -exec grep key {} \;
grep: /srv/victim99/: Is a directory
./check_ptlab_key 2213f137-429b-493c-aa92-0aca52af9286
```


![saml](https://user-images.githubusercontent.com/14318209/42239686-3d15f292-7f37-11e8-897f-a137b758b285.png)
