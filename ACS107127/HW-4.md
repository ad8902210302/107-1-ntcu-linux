#  1.�޲z�s�զ@�θ�ƪ��v���]�p�G</br></br>

####  ��"groupadd name"�s�W�s�աC</br>
![Alt text](https://github.com/ad8902210302/107-1-ntcu-linux/raw/HW-4/ACS107127/screen4/1.png)</br></br>

##  *�إ߱b���W�٬��G myuser1, myuser2, myuser3 �A�q�q�[�J mygroup�A�B�K�X�� MyPassWord </br>
####  ��"useradd -g mygroup name "�إߤ@�Ӹs�լ�"mygroup"���b���C </br>
![Alt text](https://github.com/ad8902210302/107-1-ntcu-linux/raw/HW-4/ACS107127/screen4/2.png)</br></br>

##  *�إ߱b���W�٬��G nouser1, nouser2, nouser3 �A�q�q�[�J nogroup�A�B�K�X�� MyPassWord </br>
####  ��"useradd -g nogroup name "�إߤ@�Ӹs�լ�"nogroup"���b���C </br>
![Alt text](https://github.com/ad8902210302/107-1-ntcu-linux/raw/HW-4/ACS107127/screen4/3.png)</br></br>

##  *�إߤ@�ӦW�� /srv/myproject ���ؿ��A�o�ӥؿ��i�H�� mygroup �s�դ����ϥΪ̧���ϥΡA�B�i�s�ت��ɮ׾֦��s�աj�� mygroup �C���L��L�H���঳�����v��</br>
####  ��"mkdir"�إ߷s�ؿ��A��"chmod"����v���A��"chgrp"���s�աA�A��"ll"�˵��C</br>
![Alt text](https://github.com/ad8902210302/107-1-ntcu-linux/raw/HW-4/ACS107127/screen4/4.png)</br></br>

##  *�Ȯɤ������� myuser1 �������A�ëe�� /srv/myproject �ؿ��A���իإߤ@�ӦW�� myuser1.data ���ɮסA����n�X myuser1�C </br>
####  ��"cd"�e���ؿ��A��"touch name"�s�W�ɮסA�A��"exit"�n�X�b���C</br>
![Alt text](https://github.com/ad8902210302/107-1-ntcu-linux/raw/HW-4/ACS107127/screen4/5.png)</br></br>

##  *�ƻs/usr/bin/ls��/usr/local/bin/myls��A�����U�C�ާ@ </br>
####  ��"cp -r A B"�NA�����ƻs��B�W(�Ѽ�r�������ƻs���\��)�C</br>
![Alt text](https://github.com/ad8902210302/107-1-ntcu-linux/raw/HW-4/ACS107127/screen4/6.png)</br></br>

##    *���M nogroup �s�դ����Τ��� /srv/myproject ���ӨS�������v���A���� nogroup �����Τ���� /usr/local/bin/myls �ɡA�i�H���ͻP ls �ۦP����T�A�B�Ȯɾ֦� mygroup �s�ժ��v���A�]���i�H�d�ߨ� /srv/myproject �ؿ������ɦW��T�C �]�N�O���A��A�ϥ� nouser1 ����������imyls /srv/myproject�j�ɡA���ӬO����d�\��ӥؿ������ɦW��T�C </br> 
####  ��nouser1����imyls /srv/myproject�j�ɡA�L�k�}���ɮסC
![Alt text](https://github.com/ad8902210302/107-1-ntcu-linux/raw/HW-4/ACS107127/screen4/7.png)</br></br>

####  �n��"chmod u+s"�����ϥΪ�SUID���v��(�u�n����H��x�������v�A��Τ����ɡA�|�۰ʳz�LSUID�ഫ������owner�A���ܬ�root������)�C</br>
####  ����imyls /srv/myproject�j�C</br>
![Alt text](https://github.com/ad8902210302/107-1-ntcu-linux/raw/HW-4/ACS107127/screen4/8.png)</br></br>

#  2.�ϥε{���[����O�A�f�t grep ������r�d�ߥ\��A�N��쪺 rsyslog �������{�Ǫ� PID, PRI, NI, COMMAND ����T��s�� /root/process_syslog.txt �ɮפ��C(�f�t>���ɦV��X) </br>
####  ��"ps aux |grep rsyslog"�[��{�ǡA�å�">"�N��Ʋ������w�ɮסA�A��"cat"�˵��ɮפ��e�C</br>
![Alt text](https://github.com/ad8902210302/107-1-ntcu-linux/raw/HW-4/ACS107127/screen4/11.png)</br></br>

#  3.�ϥ� find ��X /usr/bin �� /usr/sbin ��ӥؿ����A�t�� SUID ���S���ɮ��ɦW�A�èϥ� ls -l �h�C�X��쪺�ɮת������v����A�N�ù������s�� /root/findsuidsgid.txt �ɮפ��C(�ۦ�d��find���O�Ϊk�A�H�Ψϳz�L���ɦV�Ÿ�>��X�ɮ�) </br>

####  ��"find / -perm /u=s"�C�X�t�Τ��Ҧ� SUID ���ɮסA�æb�᭱�[�J"-exec ls -l {} \;"�C</br>
####  ��">"�N��Ʋ���C</br>
![Alt text](https://github.com/ad8902210302/107-1-ntcu-linux/raw/HW-4/ACS107127/screen4/14.png)</br>

####  ��"cat"�˵��ɮפ��e�C</br>
![Alt text](https://github.com/ad8902210302/107-1-ntcu-linux/raw/HW-4/ACS107127/screen4/15.png)</br>