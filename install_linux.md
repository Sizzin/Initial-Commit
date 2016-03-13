

Guia para Idiotas de como Instalar uma Máquina Virtual com SliTaz
======

#### Introdução
Nesse guia aprenderemos como baixar, instalar e criar uma máquina virtual. Os itens necessários são:
- **Máquina Virtual** - [Oracle VM VirtualBox](https://www.virtualbox.org);
- **Distribuição Linux** - [Slitaz 32bit](http://www.slitaz.org/pt/get/)
- **Pen Drive ou algum emulador de imagem de CD** - ex.: [Daemon Tools](http://www.daemon-tools.cc/por/downloads) 

##### Instalando o VirtualBox
- Abra o navegador
- Entre no endereço: [VirtualBox.org](https://www.virtualbox.org)
- Clique no menu "_Downloads_"
- Baixe o Virtual Box (nesse guia, usaremos *VirtualBox 5.0.14 for Windows Hosts*)
- Ao terminar de baixar, execute o arquivo .exe
- Clique "_Next_" para avançar
- Caso queira mudar o local da instalação, clique em "_Browser_" e escolha o local que preferir. Caso contrário, clique "_Next_" para avançar
- Clique "_Next_" para avançar
- Clique "_Yes_"
- Clique, então, em "_Install_". _Caso necessário, dê permissão como Administrador._
- Clique "Yes" para cada vez que o programa quiser instalar algo.
- Ao finalizar a instalação, clique em "Finish".

##### Criando uma Máquina Virtual
- Abra o Oracle VM VirtualBox
- Para criar uma máquina virtual, clique no botão "_Novo_"
- Em "_Nome:_", escreva "_Linux_"
- Em "_Versão:_", selecione "_Other Linux (32 bit)_" e clique em "_Próximo (N)_"
- Ajuste o tamanho da memória para _512MB_ e clique em "_Próximo(N)_"
- Selecione "_Criar um disco rígido virtual agora_" e clique em "_Criar_"
- Clique em "_Ocultar Descrição_" (ou "_Modo Expert_") e mude o "_Tamanho do arquivo (S)_" para "_60,00 GB_". Deixe o resto como está.
- Clique em "_Criar_"
 
##### Instalando Slitaz 32bit na Máquina Vitual

###### Iniciando o LiveCD
- Faça o download do [Slitaz](http://www.slitaz.org/pt/get/)
- Clique em "_Iniciar (T)_" na página principal do VirtualBox
- Na nova tela, selecione o drive que contém o disco/imagem do sistema Linux que deseja instalar na máquina virtual e clique em "_Iniciar_"
- Selecione _Slitaz Live_ ou apenas espere o sistema selecioná-lo automaticamente
- Na escolha de idiomas, selecione _en_US_ (Não se preocupe, mudaremos isso em breve) e clique em "_Ok_"
- Na escolha de teclados, selecione _br-abnt2_" e clique em "_Ok_", o sistema será iniciado.

###### Criando uma Partição
- Clique em "_Applications_" no canto inferior esquerdo da tela
- No menu "_System Tools_", selecione "_GParted Partition Editor"
- Será necessário inserir o _password_ (senha) de administrador, insira-a e clique em "_Ok_".
    - **Senha padrão** - root 
- No menu no canto superior da tela, clique em "_Device_", depois em "_Create Partition Table..._"
- Clique em "_Apply_"
- Clique com o _botão direito_ na partição "_unallocated_" e clique em "_New_"
- Ajuste o tamanho da partição (_New Size (MiB):_) para algo entre 57GB e 58GB, a exatidão não tem importância
- Em "_File System:_", selecione "_ext3_"
- Clique em "_Add_", aparecerá uma nova partição.
- Clique na partição "_unallocated_" com o _botão direito_ e selecione "_New_"
- Em "_File System:_", selecione "_linux swap_"
- Clique em "_Add_", agora terão duas partições
- No menu no canto superior da tela, clique em "_Aplly_", então clique em "_Yes_"
- Ao terminar de aplicar as mudanças, clique em "_Close_" e feche a janela do _GParted_  
    _Para mais informações sobre Partições, [clique aqui.](https://www.vivaolinux.com.br/artigo/Particionamento-de-disco-%28HD%29)_

###### Instalando o SliTaz na Máquina Virtual
- Clique em "_Applications_" no canto inferior esquerdo da tela
- No menu "_System Tools_" selecione "_SliTaz Panel_"
- Será necessário inserir usuário e senha para ter acesso ao painel. Insira-os e clique em "_Ok_"
    - **Usuário** - root  
    - **Senha** - root
- No menu no canto superior da tela, clique em "_Install_" e então em "_Install SliTaz_"
- Clique em "_Continue installation_" no final da página
- Em "_Slitaz source Media_", selecione "_LiveCD_" se você utilizou o _Daemon Tools_; se você utilizou um _Pen Drive_, então selecione "_LiveUSB_"
- Em "_Hard Disk Drive_", selecione "_/dev/hda1_" em "_Install Slitaz to partition:_"
- Em "_Options_", você pode mudar o nome de usuário em "_User login:_" e colocar uma nova senha, em "_User passwd_". Caso contrário, o _login_ e _senha_ padrões são "_tux_"
- Selecione "_Install Grub bootloader_" (_para mais informações sobre Grub, [clique aqui](https://www.vivaolinux.com.br/artigo/O-gerenciador-de-boot-GRUB)_)
- Clique em "_Procced with SliTaz installation_" e clique em "_Ok_"
- Se tudo ocorrer bem, no final da instalação aparecerá um "_Completed_". Clique em "_Installation complete. You can now restart (reboot)_" e o sistema reiniciará.
- Ao reiniciar o sistema, será novamente pedido que você escolha idioma seguido de teclado. Dessa vez selecione o idioma "_pt_BR_" e o teclado "_br-abnt2_".
- Coloque seu usuário e senha (caso não tenha mudado, o padrão é "_tux_" sem aspas para ambos) e o sistema iniciará normalmente.