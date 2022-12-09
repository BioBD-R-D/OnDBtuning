Segue abaixo algumas anotações que tenho de como realizei a configuração da VM, acesso ao VNC e no final algumas referências que me ajudaram no acesso gráfico a MV.


# 1 - Configurando a MV 

$ sudo apt update

$ sudo apt install xfce4 xfce4-goodies

//Não conseguiu localizar:

$ lsb_release -a   //consegui descobrir detalhes da distribuição que é bionic

<img src="../image/bionic.PNG">

https://packages.ubuntu.com/

<img src="../image/search.PNG">

<img src="../image/ubuntu.PNG">

$ sudo add-apt-repository universe

$ sudo apt update

$ sudo apt install tightvncserver

$ vncserver

<img src="../image/vncserver.PNG">

//(tem que configurar uma senha que será utilizada depois no TightVNC Connection)

$ vncserver -kill :1

$ mv ~/.vnc/xstartup ~/.vnc/xstartup.bak

<img src="../image/xstartup.PNG">

$ nano ~/.vnc/xstartup

// adicionar o conteúdo abaixo nesse arquivo

<img src="../image/nano.PNG">



$ sudo chmod +x ~/.vnc/xstartup



#  2 - Executando o VNC

 A - Na linha de comando da conexão via ssh que fiz com o Putty, digitei:



<img src="../image/vncserver2.PNG">


B- Na linha de comando (cmd) da minha máquina digitei:

C:\Users\Luciana>ssh -L 5901:127.0.0.1:5901 -N -f -l  cloud-di vm065.cloud.inf.puc-rio.br  

A SENHA AQUI é a do cloud-di :


<img src="../image/clouddi.PNG">



**TightVNC Connection***

<img src="../image/tignvnc.PNG">


SENHA CADASTRADA NA CONFIGURAÇÃO

<img src="../image/autenticacao.PNG">




#  Referências
<https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-vnc-on-ubuntu-18-04-pt>

<https://www.youtube.com/watch?v=QTlU1EZQZg0>

<https://itsfoss.com/unable-to-locate-package-error-ubuntu/>

<https://packages.ubuntu.com/>

<https://packages.ubuntu.com/search?keywords=xfce4&searchon=names&suite=bionic&section=all>

<https://linuxize.com/post/how-to-install-and-configure-vnc-on-ubuntu-18-04/>