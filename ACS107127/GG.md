*�`�N:* �Ш�[Gitú��@�~�y�{](#Gitú��@�~�y�{), �ߤ@���P�B�O�@�~2��HW-2���a��b�@�~10���HW-10����



1. �Х�ӽҰ�W�m�ߡA�z�Lsystemd�޲z�G��sshd�A�ȡA�����ĤG��sshd�A�Ȫ� port ���� 2222�C������i�H�ϥΫ��O `netstat -alntp | grep ssh` �T�{�O�_�ҰʤG��sshd�A�ȡA�d�Ҧp�U�G


```sh

$ netstat -alntp | grep ssh

tcp        0      0 0.0.0.0:22     0.0.0.0:*     LISTEN      1300/sshd

tcp        0      0 0.0.0.0:2222   0.0.0.0:*     LISTEN      15275/sshd 

tcp6       0      0 :::22          :::*          LISTEN      1300/sshd

tcp6       0      0 :::2222        :::*          LISTEN      15275/sshd

```


 
    Note 1: CentOS���ϥ�SELinux �A�G�w�]�u���\ SSH �ϥΰ� 22�A�Y�n�ϥΰ� 2222�A�ϽХΤU�C���}�Ҩ��ˬd


 
    ```sh

    $ semanage port -a -t ssh_port_t -p tcp 2222

    $ semanage port -l | grep ssh

    ssh_port_t tcp 2202, 22

    ```  



    Note 2: CentOS�w�]��������firewalld�|�T��X�ݰ�2222�A�Y�n�z�L2222��sssh�A�Х�����firewalld�C
