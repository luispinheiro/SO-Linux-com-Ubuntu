# LINUX PRIMEIROS PASSOS COM O TERMINAL

## A história e a linha do tempo da computação

## [**Tudo sobre a computação**](historia_da_computacao)

## Instalação do ZSH, OhMyZSH, NodeJS e Docker no terminal Ubuntu

### Instalação do Curl

```sh
sudo apt install curl
[sudo] senha para user: 
Lendo listas de pacotes... Pronto
Construindo árvore de dependências... Pronto
Lendo informação de estado... Pronto        
Os NOVOS pacotes a seguir serão instalados:
  curl
0 pacotes atualizados, 1 pacotes novos instalados, 0 a serem removidos e 1 não atualizados.
É preciso baixar 216 kB de arquivos.
Depois desta operação, 490 kB adicionais de espaço em disco serão usados.
Obter:1 http://br.archive.ubuntu.com/ubuntu mantic-updates/main amd64 curl amd64 8.2.1-1ubuntu3.2 [216 kB]
Baixados 216 kB em 8s (26,8 kB/s)                                                                                   
A seleccionar pacote anteriormente não seleccionado curl.
(Lendo banco de dados ... 182309 ficheiros e diretórios atualmente instalados.)
A preparar para desempacotar .../curl_8.2.1-1ubuntu3.2_amd64.deb ...
A descompactar curl (8.2.1-1ubuntu3.2) ...
Configurando curl (8.2.1-1ubuntu3.2) ...
A processar 'triggers' para man-db (2.11.2-3) ...
```

### Instalação do Git

```sh
$ sudo apt install git
Lendo listas de pacotes... Pronto
Construindo árvore de dependências... Pronto
Lendo informação de estado... Pronto        
Os pacotes adicionais seguintes serão instalados:
  git-man liberror-perl
Pacotes sugeridos:
  git-daemon-run | git-daemon-sysvinit git-doc git-email git-gui gitk gitweb git-cvs git-mediawiki git-svn
Os NOVOS pacotes a seguir serão instalados:
  git git-man liberror-perl
0 pacotes atualizados, 3 pacotes novos instalados, 0 a serem removidos e 1 não atualizados.
É preciso baixar 4.694 kB de arquivos.
Depois desta operação, 24,0 MB adicionais de espaço em disco serão usados.
Você quer continuar? [S/n] s
Obter:1 http://br.archive.ubuntu.com/ubuntu mantic/main amd64 liberror-perl all 0.17029-2 [25,6 kB]
Obter:2 http://br.archive.ubuntu.com/ubuntu mantic/main amd64 git-man all 1:2.40.1-1ubuntu1 [1.085 kB]              
12% [2 git-man 303 kB/1.085 kB 28%]                                                               Obter:3 http://br.archive.ubuntu.com/ubuntu mantic/main amd64 git amd64 1:2.40.1-1ubuntu1 [3.583 kB]
Baixados 4.694 kB em 3min 16s (23,9 kB/s)                                                                           
A seleccionar pacote anteriormente não seleccionado liberror-perl.
(Lendo banco de dados ... 182315 ficheiros e diretórios atualmente instalados.)
A preparar para desempacotar .../liberror-perl_0.17029-2_all.deb ...
A descompactar liberror-perl (0.17029-2) ...
A seleccionar pacote anteriormente não seleccionado git-man.
A preparar para desempacotar .../git-man_1%3a2.40.1-1ubuntu1_all.deb ...
A descompactar git-man (1:2.40.1-1ubuntu1) ...
A seleccionar pacote anteriormente não seleccionado git.
A preparar para desempacotar .../git_1%3a2.40.1-1ubuntu1_amd64.deb ...
A descompactar git (1:2.40.1-1ubuntu1) ...
Configurando liberror-perl (0.17029-2) ...
Configurando git-man (1:2.40.1-1ubuntu1) ...
Configurando git (1:2.40.1-1ubuntu1) ...
A processar 'triggers' para man-db (2.11.2-3) ...
```

### Configuração do GIT local e SSH

> https://docs.github.com/en/authentication/connecting-to-github-with-ssh

> Enviar o nome do usuário

```sh
(14:12:23 on master ✭)──> git config --global user.name "user Eduardo dos S Pinheiro"                                                     
```

> Enviar o email do usuário

```sh
(14:25:43 on master ✭)──> git config --global user.email "lepinheiro100@terra.com.br"
```

> Verificar os dados de configuração para sair do terminal digitar q

```sh
(17:24:17 on master ✭)──> git config --list
```

![Alt text](img/image-16.png)

> Mostrar arquivos ocultos pelo gerenciador de arquivos

![Alt text](img/image-14.png)

![Alt text](img/image-15.png)

### Criar um acesso SSH do GIT pelo terminal

![ssh.md mostrada apenas local](img/image-10.png)

> Digitar o comando para criação do ssh e digitar enter até criar. Ver o arquivo gerado no arquivo abaixo.

```sh
(14:56:26 on master ✭)──> ssh-keygen -t ed25519 -C "email@provedor.com.br"
```

> Como mostrar a chave gerada pelo terminal

```sh
(16:13:30 on master ✭)──> cat ~/.ssh/id_ed25519.pub                                                           
ssh-ed25519  lepinheiro100@terra.com.br
```

### Comandos GIT nicialização local

```sh
$ git init --initial-branch=main                                    
Repositório vazio Git inicializado em  /home/luis/linux/linux-primeiros-passos/.git/
```

```
 $ git status                                                  
No ramo main

No commits yet

Arquivos não monitorados:
  (utilize "git add <arquivo>..." para incluir o que será submetido)
        .gitignore
        README.md
        img/

nada adicionado ao envio mas arquivos não registrados estão presentes (use "git add" to registrar)
```


```sh
(17:45:41 on master ✭)──> git add .
```

```sh
(17:45:48 on master ✚)──> git status                                                                 
No ramo master

No commits yet

Mudanças a serem submetidas:
  (utilize "git rm --cached <arquivo>..." para não apresentar)
        new file:   .gitignore
        new file:   README.md
        new file:   img/image-1.png
        new file:   img/image-11.png
        new file:   img/image-12.png
        new file:   img/image-13.png
        new file:   img/image-14.png
        new file:   img/image-15.png
        new file:   img/image-16.png
        new file:   img/image-2.png
        new file:   img/image-3.png
        new file:   img/image-4.png
        new file:   img/image-5.png
        new file:   img/image-6.png
        new file:   img/image-7.png
        new file:   img/image-8.png
        new file:   img/image-9.png
        new file:   img/image.png
        new file:   teste.txt
```

```sh
git commit -m "First commit"                                                                
[master (root-commit) e691964] First commit
 19 files changed, 1178 insertions(+)
 create mode 100644 .gitignore
 create mode 100644 README.md
 create mode 100644 img/image-1.png
 create mode 100644 img/image-11.png
 create mode 100644 img/image-12.png
 create mode 100644 img/image-13.png
 create mode 100644 img/image-14.png
 create mode 100644 img/image-15.png
 create mode 100644 img/image-16.png
 create mode 100644 img/image-2.png
 create mode 100644 img/image-3.png
 create mode 100644 img/image-4.png
 create mode 100644 img/image-5.png
 create mode 100644 img/image-6.png
 create mode 100644 img/image-7.png
 create mode 100644 img/image-8.png
 create mode 100644 img/image-9.png
 create mode 100644 img/image.png
 create mode 100644 teste.txt
```

```sh
17:56:41 on master)──> git status                                                                 
No ramo master
nothing to commit, working tree clean
```

![Alt text](img/image-19.png)

![Alt text](img/image-20.png)

```sh
(17:31:55 on main ✚)──> git push -u origin main                                                                                                                                      
Enumerating objects: 22, done.
Counting objects: 100% (22/22), done.
Delta compression using up to 3 threads
Compressing objects: 100% (20/20), done.
Writing objects: 100% (22/22), 1.72 MiB | 742.00 KiB/s, done.
Total 22 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/luispinheiro/Instala-o-do-UBUNTU-e-dos-programas-ZSH-OhMyZSH-GIT-NVM-DOCKER-.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
```

### Instalação do ZSH

```sh
$ sudo apt install zsh
[sudo] senha para user: 
Lendo listas de pacotes... Pronto
Construindo árvore de dependências... Pronto
Lendo informação de estado... Pronto        
Os pacotes adicionais seguintes serão instalados:
  zsh-common
Pacotes sugeridos:
  zsh-doc
Os NOVOS pacotes a seguir serão instalados:
  zsh zsh-common
0 pacotes atualizados, 2 pacotes novos instalados, 0 a serem removidos e 1 não atualizados.
É preciso baixar 4.982 kB de arquivos.
Depois desta operação, 19,1 MB adicionais de espaço em disco serão usados.
Você quer continuar? [S/n] s
Obter:1 http://br.archive.ubuntu.com/ubuntu mantic/main amd64 zsh-common all 5.9-5ubuntu1 [4.174 kB]
23% [1 zsh-common 1.436 kB/4.174 kB 34%]                                                                             Obter:2 http://br.archive.ubuntu.com/ubuntu mantic/main amd64 zsh amd64 5.9-5ubuntu1 [808 kB]                       
Baixados 4.982 kB em 2min 58s (28,1 kB/s)                                                                           
A seleccionar pacote anteriormente não seleccionado zsh-common.
(Lendo banco de dados ... 180795 ficheiros e diretórios atualmente instalados.)
A preparar para desempacotar .../zsh-common_5.9-5ubuntu1_all.deb ...
A descompactar zsh-common (5.9-5ubuntu1) ...
A seleccionar pacote anteriormente não seleccionado zsh.
A preparar para desempacotar .../zsh_5.9-5ubuntu1_amd64.deb ...
A descompactar zsh (5.9-5ubuntu1) ...
Configurando zsh-common (5.9-5ubuntu1) ...
Configurando zsh (5.9-5ubuntu1) ...
A processar 'triggers' para debianutils (5.8-1) ...
A processar 'triggers' para man-db (2.11.2-3) ...
```

### Desinstalar o ZSH

```sh
$ sudo apt autoremove zsh
```

### Instalação do OhMyZSH

```sh
$ sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

Cloning Oh My Zsh...
remote: Enumerating objects: 1370, done.
remote: Counting objects: 100% (1370/1370), done.
remote: Compressing objects: 100% (1320/1320), done.
remote: Total 1370 (delta 30), reused 1148 (delta 26), pack-reused 0
Receiving objects: 100% (1370/1370), 2.01 MiB | 471.00 KiB/s, done.
Resolving deltas: 100% (30/30), done.
From https://github.com/ohmyzsh/ohmyzsh
 * [new branch]      master     -> origin/master
branch 'master' set up to track 'origin/master'.
Already on 'master'
/home/user/linux/linux-primeiros-passos

Looking for an existing zsh config...
Using the Oh My Zsh template file and adding it to /home/user/.zshrc.

Time to change your default shell to zsh:
Do you want to change your default shell to zsh? [Y/n] y
Changing your shell to /usr/bin/zsh...
[sudo] senha para user: 
Shell successfully changed to '/usr/bin/zsh'.

         __                                     __   
  ____  / /_     ____ ___  __  __   ____  _____/ /_  
 / __ \/ __ \   / __ `__ \/ / / /  /_  / / ___/ __ \ 
/ /_/ / / / /  / / / / / / /_/ /    / /_(__  ) / / / 
\____/_/ /_/  /_/ /_/ /_/\__, /    /___/____/_/ /_/  
                        /____/                       ....is now installed!


Before you scream Oh My Zsh! look over the `.zshrc` file to select plugins, themes, and options.

• Follow us on Twitter: https://twitter.com/ohmyzsh
• Join our Discord community: https://discord.gg/ohmyzsh
• Get stickers, t-shirts, coffee mugs and more: https://shop.planetargon.com/collections/oh-my-zsh
```

![Alt text](img/image.png)

![Alt text](img/image-1.png)

### Arquivo de Configuração mudar o Tema, Plugins autocomplete e outros... OhMyzsh

> Para instalação do Tema e dos plugins pode-se apenas inserir as urls no arquivo de configuração, fechar e abrir o terminal que eles serão instalados ou clonar como abaixo.

```
# adicionar as linhas abaixo no arquivo .zshrc
zinit light zdharma-continuum/fast-syntax-highlighting
zinit light zsh-users/zsh-autosuggestions
zinit light zsh-users/zsh-completions
```

> Buscar no browser pelas palavras:<br/>
<mark>oh my zsh zsh autosuggestions and autocomplete</mark>

>Themas: https://github.com/ohmyzsh/ohmyzsh/wiki/themes

> Plugins: https://gist.github.com/n1snt/454b879b8f0b7995740ae04c5fb5b7df

![Alt text](img/image-4.png)  

![Alt text](img/image-3.png)

```sh
(17:55:55)──> git clone --depth 1 -- https://github.com/marlonrichert/zsh-autocomplete.git $ZSH_CUSTOM/plugins/zsh-autocomplete
Cloning into '/home/user/.oh-my-zsh/custom/plugins/zsh-autocomplete'...
remote: Enumerating objects: 55, done.
remote: Counting objects: 100% (55/55), done.
remote: Compressing objects: 100% (53/53), done.
remote: Total 55 (delta 0), reused 36 (delta 0), pack-reused 0
Receiving objects: 100% (55/55), 1.64 MiB | 434.00 KiB/s, done.
```

```sh
(17:55:55)──> git clone --depth 1 -- https://github.com/marlonrichert/zsh-autocomplete.git $ZSH_CUSTOM/plugins/zsh-autocomplete
Cloning into '/home/user/.oh-my-zsh/custom/plugins/zsh-autocomplete'...
remote: Enumerating objects: 55, done.
remote: Counting objects: 100% (55/55), done.
remote: Compressing objects: 100% (53/53), done.
remote: Total 55 (delta 0), reused 36 (delta 0), pack-reused 0
Receiving objects: 100% (55/55), 1.64 MiB | 434.00 KiB/s, done.
```

```sh
18:05:12)──> git clone https://github.com/zdharma-continuum/fast-syntax-highlighting.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/plugins/fast-syntax-highlighting
Cloning into '/home/user/.oh-my-zsh/custom/plugins/fast-syntax-highlighting'...
remote: Enumerating objects: 3365, done.
remote: Counting objects: 100% (97/97), done.
remote: Compressing objects: 100% (61/61), done.
remote: Total 3365 (delta 45), reused 70 (delta 31), pack-reused 3268
Receiving objects: 100% (3365/3365), 1.38 MiB | 1.56 MiB/s, done.
Resolving deltas: 100% (2272/2272), done.
```

```sh
$ sudo nano ~/.zshrc
```

> Para abrir com o editor VSCode

```sh
$ sudo code ~/.zshrc
```

![Alt text](img/image-2.png)

![Alt text](img/image-6.png)

### Instalação de fontes com ligaturas e estilizar o terminal com Powerlevel10k

Escolher dentre as fontes que possuem a ligaturas.

https://github.com/tonsky/FiraCode?tab=readme-ov-file

### __Fira Code__

Cascadia Code

Operator Mono

Inconsolata

Monoid

Dank Mono

```sh
mkdir ~/.fonts
```

```sh
wget -P ~/.fonts 'https://github.com/ryanoasis/nerd-#/releases/download/v2.1.0/BitstreamVeraSansMono.zip' 
```

```sh
unzip ~/.fonts/BitstreamVeraSansMono.zip -d ~/.fonts
```

```sh
(20:40:01)──> mkdir ~/.fonts                                  
```

```sh
(21:45:23)──> wget -P ~/.fonts 'https://github.com/ryanoasis/nerd-fonts/releases/download/v2.1.0/BitstreamVeraSansMono.zip' 

--2023-12-22 21:45:50--  https://github.com/ryanoasis/nerd-fonts/releases/download/v2.1.0/BitstreamVeraSansMono.zip
Resolvendo github.com (github.com)... 20.201.28.151
Conectando-se a github.com (github.com)|20.201.28.151|:443... conectado.
A requisição HTTP foi enviada, aguardando resposta... 302 Found
Localização: https://objects.githubusercontent.com/github-production-release-asset-2e65be/27574418/17e84200-4532-11ea-8e09-245ca48a6ce8?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAIWNJYAX4CSVEH53A%2F20231223%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20231223T004550Z&X-Amz-Expires=300&X-Amz-Signature=4bf9d92219ff794489e1c4928cdae9a273888dee73b7e015b0528edf22a18f2d&X-Amz-SignedHeaders=host&actor_id=0&key_id=0&repo_id=27574418&response-content-disposition=attachment%3B%20filename%3DBitstreamVeraSansMono.zip&response-content-type=application%2Foctet-stream [redirecionando]
--2023-12-22 21:45:50--  https://objects.githubusercontent.com/github-production-release-asset-2e65be/27574418/17e84200-4532-11ea-8e09-245ca48a6ce8?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAIWNJYAX4CSVEH53A%2F20231223%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20231223T004550Z&X-Amz-Expires=300&X-Amz-Signature=4bf9d92219ff794489e1c4928cdae9a273888dee73b7e015b0528edf22a18f2d&X-Amz-SignedHeaders=host&actor_id=0&key_id=0&repo_id=27574418&response-content-disposition=attachment%3B%20filename%3DBitstreamVeraSansMono.zip&response-content-type=application%2Foctet-stream
Resolvendo objects.githubusercontent.com (objects.githubusercontent.com)... 185.199.111.133, 185.199.108.133, 185.199.109.133, ...
Conectando-se a objects.githubusercontent.com (objects.githubusercontent.com)|185.199.111.133|:443... conectado.
A requisição HTTP foi enviada, aguardando resposta... 200 OK
Tamanho: 8238313 (7,9M) [application/octet-stream]
Salvando em: ‘/home/luis/.fonts/BitstreamVeraSansMono.zip’

BitstreamVeraSansMo 100%[===================>]   7,86M   586KB/s    em 14s     

2023-12-22 21:46:05 (587 KB/s) - ‘/home/luis/.fonts/BitstreamVeraSansMono.zip’ salvo [8238313/8238313]
```

```sh
(21:46:05)──> unzip ~/.fonts/BitstreamVeraSansMono.zip -d ~/.fonts
Archive:  /home/luis/.fonts/BitstreamVeraSansMono.zip
  inflating: /home/luis/.fonts/Bitstream Vera Sans Mono Bold Nerd Font Complete Mono Windows Compatible.ttf  
  inflating: /home/luis/.fonts/Bitstream Vera Sans Mono Bold Nerd Font Complete.ttf  
  inflating: /home/luis/.fonts/Bitstream Vera Sans Mono Bold Nerd Font Complete Mono.ttf  
  inflating: /home/luis/.fonts/Bitstream Vera Sans Mono Bold Nerd Font Complete Windows Compatible.ttf  
  inflating: /home/luis/.fonts/Bitstream Vera Sans Mono Bold Oblique Nerd Font Complete.ttf  
  inflating: /home/luis/.fonts/Bitstream Vera Sans Mono Bold Oblique Nerd Font Complete Mono Windows Compatible.ttf  
  inflating: /home/luis/.fonts/Bitstream Vera Sans Mono Bold Oblique Nerd Font Complete Mono.ttf  
  inflating: /home/luis/.fonts/Bitstream Vera Sans Mono Bold Oblique Nerd Font Complete Windows Compatible.ttf  
  inflating: /home/luis/.fonts/Bitstream Vera Sans Mono Nerd Font Complete Mono.ttf  
  inflating: /home/luis/.fonts/Bitstream Vera Sans Mono Nerd Font Complete Mono Windows Compatible.ttf  
  inflating: /home/luis/.fonts/Bitstream Vera Sans Mono Nerd Font Complete Windows Compatible.ttf  
  inflating: /home/luis/.fonts/Bitstream Vera Sans Mono Nerd Font Complete.ttf  
  inflating: /home/luis/.fonts/Bitstream Vera Sans Mono Oblique Nerd Font Complete.ttf  
  inflating: /home/luis/.fonts/Bitstream Vera Sans Mono Oblique Nerd Font Complete Mono.ttf  
  inflating: /home/luis/.fonts/Bitstream Vera Sans Mono Oblique Nerd Font Complete Mono Windows Compatible.ttf  
  inflating: /home/luis/.fonts/Bitstream Vera Sans Mono Oblique Nerd Font Complete Windows Compatible.ttf  
 ```

```sh
(21:47:18)──> sudo apt install fonts-firacode 
[sudo] senha para luis: 
Lendo listas de pacotes... Pronto
Construindo árvore de dependências... Pronto
Lendo informação de estado... Pronto        
Os NOVOS pacotes a seguir serão instalados:
  fonts-firacode
0 pacotes atualizados, 1 pacotes novos instalados, 0 a serem removidos e 7 não atualizados.
É preciso baixar 1.514 kB de arquivos.
Depois desta operação, 3.005 kB adicionais de espaço em disco serão usados.
Obter:1 http://br.archive.ubuntu.com/ubuntu mantic/universe amd64 fonts-firacode all 6.2-2 [1.514 kB]
Baixados 1.514 kB em 3s (542 kB/s)          
A seleccionar pacote anteriormente não seleccionado fonts-firacode.
(Lendo banco de dados ... 185752 ficheiros e diretórios atualmente instalados.)
A preparar para desempacotar .../fonts-firacode_6.2-2_all.deb ...
A descompactar fonts-firacode (6.2-2) ...
Configurando fonts-firacode (6.2-2) ...
A processar 'triggers' para fontconfig (2.14.2-4ubuntu1) ...
```

```sh
17:44:15)──> git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
Cloning into '/home/luis/.oh-my-zsh/custom/themes/powerlevel10k'...
remote: Enumerating objects: 92, done.
remote: Counting objects: 100% (92/92), done.
remote: Compressing objects: 100% (75/75), done.
remote: Total 92 (delta 18), reused 77 (delta 13), pack-reused 0
Receiving objects: 100% (92/92), 347.08 KiB | 2.59 MiB/s, done.
Resolving deltas: 100% (18/18), done.
```

```sh
(17:45:08)──> code ~/.zshrc 
```
> Mudar o tema para <mark>ZSH_THEME="powerlevel10k/powerlevel10k"</mark>

![Alt text](img/image-21.png)

![Alt text](img/image-39.png)


![Alt text](img/image-40.png)


### Estilizar a telas de configuração do terminal com Powerlevel10k

```
$ p10k configure
```
> Seguir os passos da imagem abaixo e escolher a configuração desejada, mostro minhas escolhas em cada etapa.


![Alt text](img/image-22.png)

```
y
``` 

![Alt text](img/image-23.png)

```
y
``` 

![Alt text](img/image-24.png)

```
y
``` 

![Alt text](img/image-25.png)

```
y
``` 

![Alt text](img/image-26.png)

```
3
``` 

![Alt text](img/image-27.png)

```
1
``` 

![Alt text](img/image-28.png)

```
1
``` 

![Alt text](img/image-29.png)

```
2
``` 

![Alt text](img/image-30.png)

```
1
``` 

![Alt text](img/image-31.png)

```
2
``` 

![Alt text](img/image-32.png)

```
2
``` 

![Alt text](img/image-33.png)

```
2
``` 

![Alt text](img/image-34.png)

```
n
``` 

![Alt text](img/image-35.png)

```
1
``` 

![Alt text](img/image-36.png)

```
y
``` 

![Alt text](img/image-37.png)

> Caso queira modificar precisa digitar no terminal para ser modificado.

```
p10k configure
```

### Instalação do NVM Node via ZSH terminal Ubuntu

Acessar o link: https://github.com/lukechilds/zsh-nvm

![Alt text](img/image-8.png)

As an Oh My ZSH! custom plugin
Clone zsh-nvm into your custom plugins repo

git clone https://github.com/lukechilds/zsh-nvm ~/.oh-my-zsh/custom/plugins/zsh-nvm
Then load as a plugin in your .zshrc

plugins+=(zsh-nvm)
Keep in mind that plugins need to be added before oh-my-zsh.sh is sourced.

Manually
Clone this repository somewhere (~/.zsh-nvm for example)

```sh
git clone https://github.com/lukechilds/zsh-nvm.git ~/.zsh-nvm
```

Then source it in your .zshrc (or .bashrc)

```sh
source ~/.zsh-nvm/zsh-nvm.plugin.zsh
```

```sh
(12:26:41)──> git clone https://github.com/lukechilds/zsh-nvm ~/.oh-my-zsh/custom/plugins/zsh-nvm                                                                
Cloning into '/home/user/.oh-my-zsh/custom/plugins/zsh-nvm'...
remote: Enumerating objects: 583, done.
remote: Counting objects: 100% (57/57), done.
remote: Compressing objects: 100% (35/35), done.
remote: Total 583 (delta 31), reused 39 (delta 21), pack-reused 526
Receiving objects: 100% (583/583), 86.82 KiB | 2.41 MiB/s, done.
Resolving deltas: 100% (309/309), done.
```

> Para abrir com o editor Nano

```sh
$ sudo nano ~/.zshrc
```

> Para abrir com o editor VSCode

```sh
$ sudo code ~/.zshrc
```

![Alt text](img/image-9.png)

```sh
(12:34:04)──> source ~/. zshrc                                                                 
Installing nvm...
Cloning into '/home/user/.nvm'...
remote: Enumerating objects: 9279, done.
remote: Counting objects: 100% (2068/2068), done.
remote: Compressing objects: 100% (196/196), done.
remote: Total 9279 (delta 1965), reused 1896 (delta 1871), pack-reused 7211
Receiving objects: 100% (9279/9279), 3.57 MiB | 561.00 KiB/s, done.
Resolving deltas: 100% (5968/5968), done.
```

```sh
(12:34:32)──> nvm --version 0.39.7
```

```sh
nvm install node                                                                   
Downloading and installing node v21.4.0...
Downloading https://nodejs.org/dist/v21.4.0/node-v21.4.0-linux-x64.tar.xz...
##################################################################################################################################################################################### 100.0%
Computing checksum with sha256sum
Checksums matched!
Now using node v21.4.0 (npm v10.2.4)
Creating default alias: default -> node (-> v21.4.0)
```

```sh
(12:38:44)──> node --version                                                        
v21.4.0
```

```sh
12:40:06)──> npm --version
10.2.4
```

```sh
(12:40:17)──> nvm ls 
->      v21.4.0
default -> node (-> v21.4.0)
iojs -> N/A (default)
unstable -> N/A (default)
node -> stable (-> v21.4.0) (default)
stable -> 21.4 (-> v21.4.0) (default)
lts/* -> lts/iron (-> N/A)
lts/argon -> v4.9.1 (-> N/A)
lts/boron -> v6.17.1 (-> N/A)
lts/carbon -> v8.17.0 (-> N/A)
lts/dubnium -> v10.24.1 (-> N/A)
lts/erbium -> v12.22.12 (-> N/A)
lts/fermium -> v14.21.3 (-> N/A)
lts/gallium -> v16.20.2 (-> N/A)
lts/hydrogen -> v18.19.0 (-> N/A)
lts/iron -> v20.10.0 (-> N/A)
```

### Instalação do VSCode

> https://code.visualstudio.com/docs/setup/linux

> Para abrir o VSCode em algum determinado diretório basta digitar

> irei suprimir os valores antes dos códigos digitados no terminal linux conforme a imagem abaixo demonstra

![Alt text](img/image-38.png)

```
-> ~/linux/linux/linux-primeiros-passos code
```

### Instalação do Yarn e PNPM no terminal Ubuntu

> https://pnpm.io/pt/installation

```sh
(18:50:21 on main ✹)──> npm install --g npm                                                                    
added 1 package in 8s

1 package is looking for funding
  run `npm fund` for details
```

```sh
(19:06:08 on main)──> pnpm --version                                                                                                               
8.12.1
``` 

### Atalhos no VSCode

> Para abrir o terminal

Crtl + Shift + '(Acento agudo)

# <mark>#####|||!IMPORTANTE|||#####</mark>

> ## É possível instalar diversas versões do NODEJS com o PNPM para gereciá-las

pnpm é um gerenciador de pacotes para JavaScript, semelhante ao npm(Node Package Manager) e yarn. É usado para gerenciar dependências em um projeto Node.js. No contexto de pnpm, “exe” e “cli” referem-se a diferentes aspectos de sua funcionalidade.

pnpm-cli: esta é a interface de linha de comando (CLI) para pnpm. Quando as pessoas se referem à pnpmCLI, geralmente estão falando sobre os comandos e opções de linha de comando que você usa para interagir com o pnpm. Por exemplo, executar comandos como "pnpm install" para instalar dependências ou "pnpm run start" para executar um script definido em seu arquivo package.json.

pnpm executável ( pnpm.exeno Windows) : Este é o arquivo executável real que é executado quando você usa pnpm comandos. No Windows, o executável pode ter uma .exeextensão. Quando você instala pnpmglobalmente em sua máquina usando um gerenciador de pacotes como npmou yarn, ele instala o pnpmexecutável que você pode usar em seu terminal.

Em resumo, “cli” refere-se à interface de linha de comando e ao conjunto de comandos que você usa, enquanto “exe” refere-se ao arquivo executável que é executado quando você emite esses comandos.

Aqui está um exemplo rápido:

Exemplo de CLI : pnpm installé um comando que você executa em seu terminal usando a pnpmCLI. É um comando que a pnpmCLI entende e processa.

Exemplo de executável : ao instalar pnpmglobalmente, você pode usar um comando como npm install -g pnpmou yarn global add pnpm. Isso instala o pnpmexecutável em sua máquina, permitindo usar os pnpmcomandos CLI.

Na prática, para a maioria dos usuários, a distinção entre a pnpmCLI e o pnpmexecutável pode não ser crucial, pois eles funcionam perfeitamente juntos para gerenciar dependências em seus projetos Node.js.

<br/>
<mark>==|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||===
</mark>=<br/><br/>


> Para acessar o shell do zsh no terminal, basta difitar o comando <mark>" zsh "</mark>

```sh
$ zsh
```

> Para retornar o Shell para o bash só digitar <mark>" bash "</mark>

```sh
$ bash
```

![Alt text](img/image-5.png)

> Reload do terminal

```sh
──> source ~/.zshrc  
```

### Instalação do Docker Engine via terminal

> Será instalado o Docker Engine pois o Docker Desktop é um pouco mais pesado.

https://docs.docker.com/engine/install/ubuntu/

![Alt text](/img/image-17.png)

```sh
sudo apt update                                
[sudo] senha para user: 
Atingido:1 https://dl.google.com/linux/chrome/deb stable InRelease
Obter:2 http://security.ubuntu.com/ubuntu mantic-security InRelease [109 kB]
Atingido:3 http://br.archive.ubuntu.com/ubuntu mantic InRelease
Obter:4 http://br.archive.ubuntu.com/ubuntu mantic-updates InRelease [109 kB]
Obter:5 http://security.ubuntu.com/ubuntu mantic-security/main amd64 Packages [177 kB]
Atingido:6 http://br.archive.ubuntu.com/ubuntu mantic-backports InRelease
Obter:7 http://security.ubuntu.com/ubuntu mantic-security/main Translation-en [49,8 kB]
Obter:8 http://security.ubuntu.com/ubuntu mantic-security/universe amd64 Packages [71,6 kB]
Obter:9 http://security.ubuntu.com/ubuntu mantic-security/universe Translation-en [26,0 kB]
Obter:10 http://br.archive.ubuntu.com/ubuntu mantic-updates/main amd64 Packages [218 kB]
Obter:11 http://br.archive.ubuntu.com/ubuntu mantic-updates/main Translation-en [62,7 kB]
Obter:12 http://br.archive.ubuntu.com/ubuntu mantic-updates/universe amd64 Packages [92,0 kB]
Obter:13 http://br.archive.ubuntu.com/ubuntu mantic-updates/universe Translation-en [33,7 kB]
Baixados 948 kB em 4s (266 kB/s)     
Lendo listas de pacotes... Pronto
Construindo árvore de dependências... Pronto
Lendo informação de estado... Pronto        
8 pacotes podem ser atualizados. Corra 'apt list --upgradable' para vê-los.
```

```sh
(11:10:45)──> sudo install -m 0755 -d /etc/apt/keyrings      
```

```sh
(11:12:31)──> curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
```

```sh
(11:12:47)──> sudo chmod a+r /etc/apt/keyrings/docker.gpg    
```

```sh
(11:13:25)──> echo \                                         
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
Obter:1 https://download.docker.com/linux/ubuntu mantic InRelease [48,8 kB]
Obter:2 https://download.docker.com/linux/ubuntu mantic/stable amd64 Packages [3.095 B]
Atingido:3 http://br.archive.ubuntu.com/ubuntu mantic InRelease                
Atingido:4 https://dl.google.com/linux/chrome/deb stable InRelease             
Atingido:5 http://br.archive.ubuntu.com/ubuntu mantic-updates InRelease        
Atingido:6 http://br.archive.ubuntu.com/ubuntu mantic-backports InRelease      
Atingido:7 http://security.ubuntu.com/ubuntu mantic-security InRelease         
Baixados 51,9 kB em 3s (19,2 kB/s)                     
Lendo listas de pacotes... Pronto
(11:14:28)──> sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
Lendo listas de pacotes... Pronto
Construindo árvore de dependências... Pronto
Lendo informação de estado... Pronto        
Os pacotes adicionais seguintes serão instalados:
  docker-ce-rootless-extras libslirp0 pigz slirp4netns
Pacotes sugeridos:
  aufs-tools cgroupfs-mount | cgroup-lite
Os NOVOS pacotes a seguir serão instalados:
  containerd.io docker-buildx-plugin docker-ce docker-ce-cli
  docker-ce-rootless-extras docker-compose-plugin libslirp0 pigz slirp4netns
0 pacotes atualizados, 9 pacotes novos instalados, 0 a serem removidos e 8 não atualizados.
É preciso baixar 115 MB de arquivos.
Depois desta operação, 411 MB adicionais de espaço em disco serão usados.
Você quer continuar? [S/n] s
Obter:1 https://download.docker.com/linux/ubuntu mantic/stable amd64 containerd.io amd64 1.6.26-1 [29,5 MB]
Obter:2 http://br.archive.ubuntu.com/ubuntu mantic/universe amd64 pigz amd64 2.6-1 [63,6 kB]
Obter:3 http://br.archive.ubuntu.com/ubuntu mantic/main amd64 libslirp0 amd64 4.7.0-1ubuntu1 [63,2 kB]
Obter:4 http://br.archive.ubuntu.com/ubuntu mantic/universe amd64 slirp4netns amd64 1.2.0-1 [33,5 kB]
Obter:5 https://download.docker.com/linux/ubuntu mantic/stable amd64 docker-buildx-plugin amd64 0.11.2-1~ubuntu.23.10~mantic [28,2 MB]
Obter:6 https://download.docker.com/linux/ubuntu mantic/stable amd64 docker-ce-cli amd64 5:24.0.7-1~ubuntu.23.10~mantic [13,3 MB]
Obter:7 https://download.docker.com/linux/ubuntu mantic/stable amd64 docker-ce amd64 5:24.0.7-1~ubuntu.23.10~mantic [22,6 MB]
Obter:8 https://download.docker.com/linux/ubuntu mantic/stable amd64 docker-ce-rootless-extras amd64 5:24.0.7-1~ubuntu.23.10~mantic [9.034 kB]
Obter:9 https://download.docker.com/linux/ubuntu mantic/stable amd64 docker-compose-plugin amd64 2.21.0-1~ubuntu.23.10~mantic [11,9 MB]
Baixados 115 MB em 3s (34,0 MB/s)                   
A seleccionar pacote anteriormente não seleccionado pigz.
(Lendo banco de dados ... 185493 ficheiros e diretórios atualmente instalados.)
A preparar para desempacotar .../0-pigz_2.6-1_amd64.deb ...
A descompactar pigz (2.6-1) ...
A seleccionar pacote anteriormente não seleccionado containerd.io.
A preparar para desempacotar .../1-containerd.io_1.6.26-1_amd64.deb ...
A descompactar containerd.io (1.6.26-1) ...
A seleccionar pacote anteriormente não seleccionado docker-buildx-plugin.
A preparar para desempacotar .../2-docker-buildx-plugin_0.11.2-1~ubuntu.23.10~mantic_amd64.deb ...
A descompactar docker-buildx-plugin (0.11.2-1~ubuntu.23.10~mantic) ...
A seleccionar pacote anteriormente não seleccionado docker-ce-cli.
A preparar para desempacotar .../3-docker-ce-cli_5%3a24.0.7-1~ubuntu.23.10~mantic_amd64.deb ...
A descompactar docker-ce-cli (5:24.0.7-1~ubuntu.23.10~mantic) ...
A seleccionar pacote anteriormente não seleccionado docker-ce.
A preparar para desempacotar .../4-docker-ce_5%3a24.0.7-1~ubuntu.23.10~mantic_amd64.deb ...
A descompactar docker-ce (5:24.0.7-1~ubuntu.23.10~mantic) ...
A seleccionar pacote anteriormente não seleccionado docker-ce-rootless-extras.
A preparar para desempacotar .../5-docker-ce-rootless-extras_5%3a24.0.7-1~ubuntu.23.10~mantic_amd64.deb ...
A descompactar docker-ce-rootless-extras (5:24.0.7-1~ubuntu.23.10~mantic) ...
A seleccionar pacote anteriormente não seleccionado docker-compose-plugin.
A preparar para desempacotar .../6-docker-compose-plugin_2.21.0-1~ubuntu.23.10~mantic_amd64.deb ...
A descompactar docker-compose-plugin (2.21.0-1~ubuntu.23.10~mantic) ...
A seleccionar pacote anteriormente não seleccionado libslirp0:amd64.
A preparar para desempacotar .../7-libslirp0_4.7.0-1ubuntu1_amd64.deb ...
A descompactar libslirp0:amd64 (4.7.0-1ubuntu1) ...
A seleccionar pacote anteriormente não seleccionado slirp4netns.
A preparar para desempacotar .../8-slirp4netns_1.2.0-1_amd64.deb ...
A descompactar slirp4netns (1.2.0-1) ...
Configurando docker-buildx-plugin (0.11.2-1~ubuntu.23.10~mantic) ...
Configurando containerd.io (1.6.26-1) ...
Created symlink /etc/systemd/system/multi-user.target.wants/containerd.service → /lib/systemd/system/containerd.service.
Configurando docker-compose-plugin (2.21.0-1~ubuntu.23.10~mantic) ...
Configurando docker-ce-cli (5:24.0.7-1~ubuntu.23.10~mantic) ...
Configurando libslirp0:amd64 (4.7.0-1ubuntu1) ...
Configurando pigz (2.6-1) ...
Configurando docker-ce-rootless-extras (5:24.0.7-1~ubuntu.23.10~mantic) ...
Configurando slirp4netns (1.2.0-1) ...
Configurando docker-ce (5:24.0.7-1~ubuntu.23.10~mantic) ...
Created symlink /etc/systemd/system/multi-user.target.wants/docker.service → /lib/systemd/system/docker.service.
Created symlink /etc/systemd/system/sockets.target.wants/docker.socket → /lib/systemd/system/docker.socket.
A processar 'triggers' para man-db (2.11.2-3) ...
A processar 'triggers' para libc-bin (2.38-1ubuntu6) ...
```

<br/>
<mark>==|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||=====|||===
</mark>=<br/><br/>

## Comandos linux

As três partes principais de um comando são:

> CommandName (nome). É a regra em si que você quer executar.
Flag (opção). É um modificador para a operação do comando. Você pode incluí-lo no comando usando um hífen (-) ou dois (–).
Argument (parâmetro). Serve para adicionar informações ou contexto ao comando.

NomeDoComando [opção/opções] [parâmetro(s)]


VPS
jul 21, 2023

Ariane G.

https://www.hostinger.com.br/tutoriais/comandos-linux


O Linux é uma família de sistemas operacionais Unix de código aberto, baseados no kernel Linux.

Conteúdo
Tutorial em Vídeo
O Que É Um Comando Linux?
Comandos Mais Usados no Linux
Lista Os 40 Principais Comandos Linux
Dicas e Truques Bônus
Comandos Linux Perguntas Frequentes
Tutorial em Vídeo
No vídeo abaixo, você pode conferir alguns dos 15 comandos Linux mais úteis para iniciantes.

As três partes principais de um comando são:

CommandName (nome). É a regra em si que você quer executar.
Flag (opção). É um modificador para a operação do comando. Você pode incluí-lo no comando usando um hífen (-) ou dois (–).
Argument (parâmetro). Serve para adicionar informações ou contexto ao comando.
Tendo isso em mente, a sintaxe básica de um comando Linux é a seguinte:

NomeDoComando [opção/opções] [parâmetro(s)]

Em alguns casos, um comando pode rodar sem a necessidade de opções ou parâmetros, mas a maioria deles exigirá esses elementos para ser executado corretamente. Tenha em mente, também, que os comandos são sensíveis a maiúsculas e minúsculas.

Comandos Mais Usados no Linux
Confira abaixo uma lista com os 8 comandos mais usados nos sistemas operacionais baseados em Linux:

pwd: encontra o caminho completo do diretório atual.
cd: permite navegar até determinada pasta.
ls: lista todos os arquivos e pastas dentro de um diretório.
cat: lista os conteúdos de um arquivo de texto na saída padrão (sdout).
cp: copia arquivos do diretório atual para uma pasta diferente.
mv: pode ser usado para mover ou renomear arquivos.
mkdir: cria um novo diretório.
rm: remove arquivos e diretórios.
sudo: executa um comando como superusuário.
find: para buscar arquivos em diretórios.

Lista: Os 40 Principais Comandos Linux
Antes de entrarmos na lista de principais comandos Linux, primeiro você precisa abrir a linha de comando do sistema. Se você ainda tem insegurança sobre a interface de linha de comando, confira nosso tutorial sobre CLI.

Embora os passos abaixo possam ser ligeiramente diferentes dependendo da distribuição que você estiver usando, você geralmente encontra a linha de comando na seção Utilities (Utilidades).

#### 1. Comando pwd
Use o comando pwd para encontrar o caminho para o diretório atual (da pasta) em que você está. O comando vai retornar um caminho completo (cheio), que é basicamente um caminho que começa com uma barra inclinada (/). Um exemplo de um caminho completo é /home/username.

O comando pwd usa a seguinte sintaxe:

pwd [opção]

Ele tem duas opções aceitáveis:

-L ou –logical imprime o conteúdo da variável de ambiente, incluindo links simbólicos.
-P ou –physical imprime o caminho real do diretório atual.

#### 2. Comando cd
Para navegar pelos arquivos e diretórios Linux, use o comando cd. Ele requer ou um caminho completo ou o nome de um diretório, dependendo do diretório atual em que você estiver.

Vamos dizer que você esteja em /home/username/Documents e quer ir para Photos, um subdiretório de Documents. Para fazer isso, simplesmente digite cd Photos.

Outro cenário em que você quer mudar completamente de diretório, digamos, para /home/username/Movies. Nesse caso, você tem que digitar cd seguido pelo caminho absoluto do diretório.   

Existem alguns ds que você pode usar para navegar mais rapidamente.:

Use cd .. (com dois pontos seguidos) para subir diretório acima
Use cd ~[username] para acessar o diretório inicial de outro usuário.
Use cd– (com um hífen) para mover para os diretórios anteriores.

#### 3. Comando ls
O comando ls é usado para visualizar conteúdos em um diretório. Por padrão, esse comando vai mostrar os conteúdos apenas do diretório atual em que você estiver.

Se você quiser ver o conteúdo de outros diretórios, digite ls e, então, o caminho do diretório. Por exemplo, digite ls /home/username/Documents para ver os conteúdos de Documents.

Existem variações que você pode usar com o comando Is:

ls -R vai listar todos os arquivos nos subdiretórios.
ls -a vai mostrar todos os arquivos ocultos.
ls -lh vai listar todos os tamanhos de arquivos em formatos fáceis, como MB, GB ou TB.

```sh
(20:16:48)──> ls -a                                           
 .                   linux                       Vídeos
 ..                  .local                      .viminfo
'Área de trabalho'   Modelos                     .vscode
 .bash_history       Músicas                     .zcompdump
 .bash_logout        .oh-my-zsh                  .zcompdump-hostname-5.9
 .bashrc             .pki                        .zcompdump-hostname-5.9.zwc
 .cache              .profile                    .zsh_history
 .config             Público                     .zshrc
 Documentos          .shell.pre-oh-my-zsh        .zshrc.save
 Downloads           snap                        .zshrc.swp
 .gnupg              .ssh
 Imagens             .sudo_as_admin_successful

(20:45:37)──> ls -lh                                          
total 40K
drwxr-xr-x 2 user user 4,0K nov  2 22:31 'Área de trabalho'
drwxr-xr-x 2 user user 4,0K nov  2 22:31  Documentos
drwxr-xr-x 2 user user 4,0K dez  9 10:35  Downloads
drwxr-xr-x 3 user user 4,0K dez 16 14:50  Imagens
drwxrwxr-x 3 user user 4,0K dez 15 19:39  linux
drwxr-xr-x 2 user user 4,0K nov  2 22:31  Modelos
drwxr-xr-x 2 user user 4,0K nov  2 22:31  Músicas
drwxr-xr-x 2 user user 4,0K nov  2 22:31  Público
drwx------ 8 user user 4,0K dez  9 22:15  snap
drwxr-xr-x 2 user user 4,0K nov  2 22:31  Vídeos

(20:45:50)──> ls                                              
'Área de trabalho'   Downloads   linux     Músicas   snap
 Documentos          Imagens     Modelos   Público   Vídeos
(20:47:06)──> ls -R                                           
.:
'Área de trabalho'   Downloads   linux     Músicas   snap
 Documentos          Imagens     Modelos   Público   Vídeos

'./Área de trabalho':

./Documentos:

./Downloads:
google-chrome-stable_current_amd64.deb

./Imagens:
'Capturas de tela'

'./Imagens/Capturas de tela':
'Captura de tela de 2023-12-16 14-50-11.png'
'Captura de tela de 2023-12-16 14-51-14.png'
'Captura de tela de 2023-12-16 15-03-09.png'
'Captura de tela de 2023-12-16 15-11-21.png'
'Captura de tela de 2023-12-16 15-11-35.png'
'Captura de tela de 2023-12-16 15-28-34.png'
'Captura de tela de 2023-12-16 17-44-30.png'
'Captura de tela de 2023-12-16 18-58-13.png'
'Captura de tela de 2023-12-16 19-10-27.png'
'Captura de tela de 2023-12-16 20-16-52.png'
'Captura de tela de 2023-12-16 20-47-02.png'

./linux:
linux-primeiros-passos

./linux/linux-primeiros-passos:
image-1.png  image-3.png  image-5.png  image-7.png  README.md
image-2.png  image-4.png  image-6.png  image.png

./Modelos:

./Músicas:

./Público:

./snap:
code     firmware-updater  snapd-desktop-integration
firefox  hello-world       snap-store

./snap/code:
147  148  common  current

./snap/code/147:

./snap/code/148:

./snap/code/common:

./snap/firefox:
3216  3506  common  current

./snap/firefox/3216:

./snap/firefox/3506:

./snap/firefox/common:

./snap/firmware-updater:
109  common  current

./snap/firmware-updater/109:

./snap/firmware-updater/common:

./snap/hello-world:
29  common  current

./snap/hello-world/29:

./snap/hello-world/common:

./snap/snapd-desktop-integration:
83  common  current

./snap/snapd-desktop-integration/83:
Desktop  Documents  Downloads  Music  Pictures  Public  Templates  Videos

./snap/snapd-desktop-integration/83/Desktop:

./snap/snapd-desktop-integration/83/Documents:

./snap/snapd-desktop-integration/83/Downloads:

./snap/snapd-desktop-integration/83/Music:

./snap/snapd-desktop-integration/83/Pictures:

./snap/snapd-desktop-integration/83/Public:

./snap/snapd-desktop-integration/83/Templates:

./snap/snapd-desktop-integration/83/Videos:

./snap/snapd-desktop-integration/common:

./snap/snap-store:
1046  common  current

./snap/snap-store/1046:

./snap/snap-store/common:

./Vídeos
```

#### 4. Comando cat
O cat (abreviação para concatenar) é um dos comandos Linux mais usados. Ele é usado para visualizar, criar e relacionar arquivos. Para executar esse comando, digite cat seguido pelo nome do arquivo e sua extensão. Por exemplo: cat nomedoarquivo.txt.

Aqui estão outras maneiras de usar o comando cat:

cat > nomedoarquivo.txt cria um novo arquivo
cat nomedoarquivo1.txt nomedoarquivo2.txt > nomedoarquivo3.txt junta dois arquivos (1 e 2) em um novo (3).
tac nomedoarquivo.txt exibe o conteúdo do arquivo em ordem reversa.

#### 5. Comando cp
Use o comando cp para copiar arquivos ou diretórios e seu conteúdo. Abaixo, listamos alguns exemplos.

Para copiar um arquivo do diretório atual para outro, digite cp seguido do nome do arquivo e do diretório de destino. Por exemplo:

cp nomedoarquivo.txt /home/username/Documents

Para copiar arquivos para um diretório, digite os nomes dos arquivos seguidos do diretório de destino:

cp nomedoarquivo1.txt nomedoarquivo2.txt nomedoarquivo3.txt /home/username/Documents

Para copiar o conteúdo de um arquivo para um novo arquivo no mesmo diretório, digite cp seguido do arquivo de origem e do arquivo de destino:

cp nomedoarquivo1.txt nomedoarquivo2.txt

Para copiar um diretório inteiro, passe o sinalizador -R antes de digitar o diretório de origem, seguido pelo diretório de destino:

cp -R /home/username/Documents /home/username/Documents_backup

#### 6. Comando mv
O uso mais comum do comando mv é mover arquivos, mas ele também pode ser usado para renomear arquivos.

Basta digitar mv seguido do nome do arquivo e do diretório de destino. Por exemplo, você deseja mover o arquivo nomedoarquivo.txt para o diretório /home/username/Documents:

mv nomedoarquivo.txt /home/username/Documents.

Você também pode usar o comando mv para renomear um arquivo:

mv nomedoarquivo_antigo.txt nome_novo.txt

#### 7. Comando mkdir
Use o comando mkdir para criar um ou vários diretórios de uma só vez e definir permissões para cada um deles. O usuário que executa esse comando deve ter o privilégio de criar uma nova pasta no diretório principal, caso contrário, poderá receber um erro de permissão negada.

Aqui está a sintaxe básica:

mkdir [opção] nome_do_diretório

Por exemplo, você deseja criar um diretório chamado Music:

mkdir Music

Para criar um novo diretório chamado Songs dentro de Music, use este comando:

mkdir Music/Songs

O comando mkdir aceita muitas opções, como:

-p ou –parents cria um diretório entre duas pastas existentes. Por exemplo, mkdir -p Music/2020/Songs criará o novo diretório “2020”.
-m define as permissões do arquivo. Por exemplo, para criar um diretório com permissões completas de leitura, gravação e execução para todos os usuários, digite mkdir -m777 nome_do_diretório.
-v imprime uma mensagem para cada diretório criado.

#### 8. Comando rmdir
Para excluir permanentemente um diretório vazio, use o comando rmdir. Lembre-se de que o usuário que executa esse comando deve ter privilégios sudo no diretório pai.

Por exemplo, você deseja remover um subdiretório vazio chamado personal1 e sua pasta principal mydir:

rmdir -p mydir/personal1

#### 9. Comando rm
O comando rm é usado para excluir arquivos em um diretório. Certifique-se de que o usuário que executa esse comando tenha permissões de gravação.

Lembre-se do local do diretório, pois isso apagará o(s) arquivo(s) permanentemente e não há como desfazer a ação.

Aqui está a sintaxe geral:

rm nome_do_arquivo

Para remover vários arquivos, digite o seguinte comando:

rm nome_do_arquivo1 nome_do_arquivo2 nome_do_arquivo3

Aqui estão algumas opções que você pode adicionar:

-i solicita a confirmação do sistema antes de excluir um arquivo.
-f permite que o sistema faça a remoção sem confirmação.
-r exclui arquivos e diretórios recursivamente.

#### 10. Comando touch
O comando touch permite criar um arquivo vazio ou gerar e modificar um registro de data e hora na linha de comando do Linux.

Por exemplo, digite o seguinte comando para criar um arquivo HTML chamado Web no diretório Documents:

touch /home/username/Documents/Web.html

#### 11. Comando locate
Você pode o comando locate para localizar um arquivo, assim como você faz para procurar um arquivo no Windows. Além disso, usando o argumento -i junto com esse comando faz com que ele se torne insensível a maiúsculas ou minúsculas, permitindo que você pesquise por um arquivo mesmo sem saber exatamente o nome dele.

Para procurar um arquivo que contém duas ou mais palavras, use um asterisco (*). Por exemplo, use o comando locate -i school*note para encontrar qualquer arquivo que tenha as palavras “school” e “note”, não importando se existem letras maiúsculas ou minúsculas.

#### 12. Comando find
Similar ao comando locate, o comando find ajuda você a procurar por arquivos. A diferença é que você usa o find para localizar arquivos dentro de um diretório específico.

Como exemplo, digite find /home/ -name notes.txt para procurar por um arquivo chamado notes.txt dentro do diretório home e seus subdiretórios.

Outras variações na hora de usar o find são:

find -name nomedoarquivo.txt para localizar arquivos no diretório atual.
find ./ -type d -name nomedodiretorio para procurar diretórios.

#### 13. Comando grep
Outro comando básico do Linux que merece ser citado é o grep. Ele permite que você encontre uma palavra pesquisando todo o conteúdo de um arquivo específico.

Quando o comando grep encontra uma correspondência, ele imprime todas as linhas que contêm o padrão específico. Esse comando ajuda a filtrar arquivos de registro grandes.

Por exemplo, se você deseja pesquisar a palavra blue (azul) no arquivo notepad.txt:

grep blue notepad.txt 

A saída do comando exibirá as linhas que contêm a palavra blue.

#### 14. Comando sudo
Correspondente a SuperUser Do, sudo é um dos comandos básicos mais populares do Linux. Ele permite executar tarefas que exigem permissões administrativas ou de root.

Ao usar o sudo, o sistema solicitará que os usuários se autentiquem com uma senha. Em seguida, o sistema Linux registrará um registro de data e hora como um rastreador. Por padrão, todo usuário root pode executar comandos sudo por 15 minutos/sessão.

Se você tentar executar o sudo na linha de comando sem se autenticar, o sistema registrará a atividade como um evento de segurança.

Aqui está a sintaxe geral:

sudo [comando]

Você também pode adicionar uma opção, por exemplo:

-k ou –reset-timestamp invalida o arquivo de registro de data e hora.
-g ou –group=group executa comandos como um nome ou ID de grupo especificado.
-h ou –host=host executa comandos no host.

#### 15. Comando df
Use o comando df para obter informações sobre o uso do espaço em disco do sistema, mostrado em porcentagem e quilobyte (KB). Esta é a sintaxe geral:

df [opções] [arquivo]

Por exemplo, digite o seguinte comando se quiser ver quanto espaço o atual diretório ocupa em um formato legível por humanos:

df -h

Essas são algumas opções que você pode usar:

O df -m exibe informações sobre o uso do sistema de arquivos em MBs.
df -k exibe o uso do sistema de arquivos em KBs.
df -T mostra o tipo de sistema de arquivos em uma nova coluna.

#### 16. Comando du
Se você quiser verificar quanto de espaço um arquivo ou diretório ocupa, use o comando du. Você pode executar esse comando para identificar qual parte do sistema usa excessivamente o armazenamento do seu sistema.

Lembre-se de que você deve especificar o caminho do diretório ao usar o comando du. Por exemplo, para verificar /home/user/Documents, digite:

du /home/user/Documents

Adicionar um sinalizador ao comando du modificará a operação, por exemplo:

-s oferece o tamanho total de uma pasta especificada.
-m fornece informações sobre pastas e arquivos em MB 
k exibe informações em KB.
-h informa a data da última modificação das pastas e arquivos exibidos.

#### 17. Comando head
O comando head permite que você visualize as primeiras dez linhas de um texto. A adição de uma opção permite que você altere o número de linhas mostradas. O comando head também é usado para enviar dados canalizados para a CLI.

Aqui está a sintaxe geral:

head [opção] [arquivo]

Por exemplo, se você deseja visualizar as primeiras dez linhas do arquivo note.txt, localizado no diretório atual:

head note.txt

Abaixo estão algumas opções que você pode adicionar:

-n ou –lines imprime o primeiro número personalizado de linhas. Por exemplo, digite head -n 5 nomedoarquivo.txt para exibir as cinco primeiras linhas de nomedoarquivo.txt.
-c ou –bytes imprime o primeiro número personalizado de bytes de cada arquivo.
-q ou –quiet não imprimirá cabeçalhos que especifiquem o nome do arquivo.

#### 18. Comando tail
O comando tail tem função similar ao comando head, mas mostrando as últimas 10 linhas de um arquivo de texto.

Este é o formato geral:

tail [opção] [arquivo]

Por exemplo, você deseja mostrar as últimas dez linhas do arquivo colors.txt:

tail -n colors.txt

#### 19. Comando diff
O comando diff (diferença) compara o conteúdo de dois arquivos linha por linha. Depois de analisar esses arquivos, ele vai mostrar as linhas que não são comuns entre eles.

Os programadores frequentemente usam este comando quando precisam fazer pequenas alterações em programas. Assim, eles não precisam reescrever o código inteiro.

Este é o formato geral:

diff [opção] arquivo1 arquivo2

Por exemplo, você deseja comparar dois arquivos de texto — note.txt e note_update.txt:

diff note.txt note_update.txt

Aqui estão algumas opções para adicionar:

-q mostra apenas se os arquivos são diferentes ou não, sem especificar as diferenças.
-i torna o comando diff insensível a maiúsculas e minúsculas.
-b ignora espaços em branco como possíveis diferenças.

#### 20. Comando tar
O comando tar reúne vários arquivos em um arquivo TAR — um formato do Linux semelhante ao ZIP, com compactação opcional.

Aqui está a sintaxe básica:

tar [options] [archive_file] [arquivo ou diretório a ser arquivado]

Por exemplo, você deseja criar um novo arquivo TAR chamado novoarquivo.tar no diretório /home/user/Documents:

tar -cvf novoarquivo.tar /home/user/Documents

O comando tar aceita muitas opções, como:

-x extrai um arquivo.
-t lista o conteúdo de um arquivo.
-u arquiva e adiciona a um arquivo existente.

#### 21. Comando chmod
O chmod é um comando que modifica as permissões de leitura, gravação e execução de um arquivo ou diretório. No Linux, cada arquivo está associado a três classes de usuários: proprietário, membro do grupo e outros.

Aqui está a sintaxe básica:

chmod [opção] [permissão] [nome_do_arquivo]

Por exemplo, o proprietário é atualmente o único com permissões totais para alterar o arquivo note.txt. Para permitir que os membros do grupo e outros possam ler, gravar e executar o arquivo, altere-o para o tipo de permissão -rwxrwxrwx, cujo valor numérico é 777:

chmod 777 note.txt

O comando chmod oferece suporte a várias opções, incluindo:

-c ou –changes exibe informações quando uma alteração é feita.
-f ou –silent suprime as mensagens de erro.
-v ou –verbose exibe um diagnóstico para cada arquivo processado.

#### 22. Comando chown
No Linux, todos os arquivos são de propriedade de um usuário específico. O comando chown permite alterar a propriedade de um arquivo, diretório ou link simbólico para um nome de usuário específico. 

Este é o formato básico:

chown [opção] proprietário[:grupo] arquivo(s)

Por exemplo, você deseja tornar o linuxuser2 o proprietário do arquivo filename.txt:

chown linuxuser2 filename.txt

#### 23. Comando jobs
Um job é um processo que iniciado pelo shell. O comando jobs exibirá todos os processos em execução juntamente com seus status. Lembre-se de que esse comando só está disponível nos shells csh, bash, tcsh e ksh.

Essa é a sintaxe básica:

jobs [opções] jobID

Para verificar o status dos trabalhos no shell atual, basta digitar jobs na CLI.

Aqui estão algumas opções que você pode usar:

-l lista as IDs de processo juntamente com suas informações.
-n lista os processos cujos status foram alterados desde a última notificação.
-p lista somente IDs de processos.

#### 24. Comando kill
Se você tem um programa que não está respondendo bem, você pode finalizá-lo manualmente pelo comando kill. Ele vai mandar um certo sinal ao aplicativo com mau funcionamento e instruir que ele seja encerrado sozinho logo na sequência.

Existe um total de 64 avisos que você pode usar, mas, geralmente, as pessoas usam apenas 2 deles:

SIGTERM (15) – pede que um programa pare de rodar e dá algum tempo para salvar todo o seu progresso. Se você não especificar o aviso quando executar o comando kill, é este aviso que será usado.
SIGKILL (9) – força um programa a parar imediatamente, em que todo o progresso não salvo será perdido.
Além de saber os avisos (sinais, notificações), você também precisa conhecer o número de identificação do processo (PID) do programa que você quer matar (kill). Se você não souber o PID, apenas execute o comando ps ux.  

Depois de saber qual aviso você quer usar e o PID do programa, use a sintaxe abaixo:

kill [signal option] PID.

#### 25. Comando ping
O comando ping é um dos comandos básicos do Linux mais usados para verificar se uma rede ou um servidor está acessível. Além disso, ele é usado para solucionar vários problemas de conectividade.

Este é o formato geral:

ping [opção] [nome_do_hospedeiro_ou_endereço_IP]

Por exemplo, você quer saber se pode se conectar ao Google e medir seu tempo de resposta:

ping google.com

#### 26. Comando wget
A linha de comando do Linux permite que você baixe arquivos da Internet usando o comando wget. Ele funciona em segundo plano, sem atrapalhar outros processos em execução.

O comando wget baixa arquivos usando os protocolos HTTP, HTTPS e FTP. Ele pode executar downloads recursivos, que transferem partes de sites seguindo estruturas de diretórios e links, criando versões locais de páginas da web.

Para usá-lo, digite o seguinte comando:

wget [opção] [url]

Por exemplo, digite o seguinte comando para baixar a versão mais recente do WordPress:

wget https://wordpress.org/latest.zip

#### 27. Comando uname
O comando uname, que significa Unix Name, vai mostrar informações detalhadas sobre seu sistema Linux. Isso inclui o nome da máquina, do sistema operacional, do kernel e assim por diante.

uname [opção]

Essas são algumas das opções que você pode usar:

-a exibe todas as informações do sistema.
-s exibe o nome do kernel.
-n exibe o hostname do node do sistema.

> Arquivo de configuração do nome do hostname

```sh
(12:04:17)──> sudo nano /etc/hostname
```
![Alt text](img/image-18.png)

#### 28. Comando top
Equivalente ao gerenciador de tarefas do Windows, o comando top vai mostrar uma lista de processos que estão em execução e o quanto de CPU cada processo usa. Ele é muito útil para monitorar o uso dos recursos do sistema, especialmente para saber qual processo deve ser encerrado por consumir muitos recursos. Basta digitar top na CLI para executá-lo.

#### 29. Comando history
Com o history, o sistema listará até 500 comandos executados anteriormente, permitindo que você os reutilize sem precisar digitá-los novamente. Lembre-se de que somente os usuários com privilégios sudo podem executar esse comando. A forma de execução desse comando também depende do shell do Linux que você usa.

Para executá-lo, digite o comando abaixo:

history [opção]

Esse comando oferece suporte a várias opções, como:

-c limpa a lista completa do histórico.
-d offset exclui o registro do histórico na posição OFFSET.
-a acrescenta linhas de histórico.

#### 30. Comando man
O comando man fornece um manual completo para todos comandos ou utilitários que podem ser executados no Terminal, incluindo o nome, a descrição e as opções.

Ele consiste em nove seções:

Programas executáveis ou comandos do shell
Chamadas de sistema
Chamadas da biblioteca
Jogos
Arquivos especiais
Formatos e convenções de arquivos
Comandos de administração do sistema
Rotinas do kernel
Diversos
Para exibir o manual completo, digite:

man [nome_do_comando]

Por exemplo, se você deseja acessar o manual do comando ls:

man ls

Digite esse comando se quiser especificar a seção exibida:

man [opção] [número_da_seção] [nome_do_comando]

Por exemplo, você deseja ver a seção 2 do manual do comando ls:

man 2 ls

#### 31. Comando echo
O comando echo é um utilitário nativo que exibe uma linha de texto ou cadeia de caracteres (string) usando a saída padrão. Veja a seguir a sintaxe básica:

echo [opção] [string]

Por exemplo, você pode exibir o texto Hostinger Tutoriais digitando:

echo “Hostinger Tutoriais” 

Esse comando oferece suporte a várias opções, como:

-n exibe a saída sem a nova linha final.
-e permite a interpretação dos seguintes escapes de barra invertida:
\a reproduz um alerta sonoro.
\b remove os espaços entre um texto.
\c não produz mais nenhum resultado.
-E exibe a opção padrão e desativa a interpretação dos escapes de barra invertida.

#### 32. Comandos zip e unzip
Use o comando zip para compactar seus arquivos em um arquivo ZIP, um formato universal comumente usado no Linux. Ele pode escolher automaticamente a melhor taxa de compactação. 

O comando zip também é útil para arquivar arquivos e diretórios e reduzir o uso do disco.

Para usá-lo, digite a seguinte sintaxe:

zip [opções] zipfile file1 file2….

Por exemplo, se você tem um arquivo chamado note.txt que deseja compactar em archive.zip no diretório atual:

zip archive.zip note.txt

Por outro lado, o comando unzip extrai os arquivos compactados de um arquivo. Este é o formato geral:

unzip [opção] nome_do_arquivo.zip

Portanto, para descompactar um arquivo chamado archive.zip no diretório atual, digite:

unzip archive.zip

#### 33. Comando hostname
Execute o comando hostname para saber o nome do host do sistema. Você pode executá-lo com ou sem uma opção. Aqui está a sintaxe geral:

hostname [opção]

Há muitos sinalizadores opcionais a serem usados, incluindo:

-a ou –alias exibe o alias do nome do host.
-A ou –all-fqdns exibe o nome de domínio totalmente qualificado (FQDN) da máquina.
-i ou –ip-address exibe o endereço IP da máquina.
Por exemplo, digite o seguinte comando para saber o endereço IP de seu computador:

hostname -i

#### 34. Comandos useradd e userdel
O Linux é um sistema multiusuário, o que significa que mais de uma pessoa pode usá-lo simultaneamente. useradd é usado para criar uma nova conta, enquanto o comando passwd permite adicionar uma senha. Somente aqueles com privilégios de root ou sudo podem executar o comando useradd. 

Quando você usa o comando useradd, ele realiza algumas alterações importantes:

Edita os arquivos /etc/passwd, /etc/shadow, /etc/group e /etc/gshadow para as contas recém-criadas.
Cria e preenche um diretório inicial para o usuário.
Define as permissões e a propriedade dos arquivos no diretório inicial.
Aqui está a sintaxe básica:

useradd [opção] nome_de_usuário

Para definir a senha:

passwd a_senha_escolhida

Por exemplo, para adicionar uma nova pessoa chamada Paulo, digite o seguinte comando simultaneamente:

useradd Paulo 

passwd 123456789

Para excluir uma conta de usuário, use o comando userdel:

userdel nome_de_usuário

#### 35. Comando apt-get
O apt-get é uma ferramenta de linha de comando para lidar com as bibliotecas da Advanced Package Tool (APT) no Linux. Ele permite que você obtenha informações e pacotes de fontes autenticadas para gerenciar, atualizar, remover e instalar softwares e suas dependências.

A execução do comando apt-get exige que você tenha privilégios sudo ou root.

Aqui está a sintaxe principal:

apt-get [opções] (comando)

Esses são os comandos mais comuns que você pode adicionar ao apt-get:

update sincroniza os arquivos de pacote de suas fontes.
upgrade instala a versão mais recente de todos os pacotes instalados.
check atualiza o cache de pacotes e verifica dependências quebradas.

#### 36. comandos nano, vi e jed ou VSCode
O Linux permite que os usuários editem e gerenciem arquivos por meio de um editor de texto usando comandos como o nano, o vi ou o jed. O nano e o vi são nativos do sistema operacional, enquanto o jed precisa ser instalado.

O comando nano denota palavras-chave e pode funcionar com a maioria dos idiomas. Para usá-lo, digite o seguinte comando:

nano [nome do arquivo]

O vi usa dois modos operacionais para trabalhar: insert e Command. O insert é usado para editar e criar um arquivo de texto. Por outro lado, o command executa operações, como salvar, abrir, copiar e colar um arquivo.

Para usar o vi em um arquivo, digite:

vi [nome do arquivo]

O jed tem uma interface de menu suspenso que permite aos usuários executar ações sem digitar combinações ou comandos do teclado. Como o vi, ele tem modos para carregar módulos ou plugins para escrever textos específicos.

"VSCode" refere-se ao Visual Studio Code, um popular editor de código-fonte desenvolvido pela Microsoft. É gratuito e de código aberto e oferece suporte a várias linguagens de programação,

Para usar o code para abrir um arquivo, digite:
code [nome do arquivo]

Para abrir o programa, basta digitar jed na linha de comando.

#### 37. Comandos alias e unalias

O alias permite que você crie um atalho com a mesma funcionalidade de um comando, nome de arquivo ou texto. Quando executado, ele instrui o shell a substituir uma string por outra.

Para usar o comando alias, digite a seguinte sintaxe:

alias Name=String

Por exemplo, você deseja tornar k o alias do comando kill:

alias k=’kill’

Por outro lado, o comando unalias exclui um alias existente.

Veja a seguir como é a sintaxe geral:

unalias [nome_do_alias]

#### 38. Comando su
O comando switch user, ou su, permite executar um programa como um usuário diferente. Ele altera a conta administrativa na sessão de login atual. Esse comando é especialmente útil para acessar o sistema por meio de SSH ou usar o gerenciador de exibição da GUI quando o usuário raiz não está disponível.

Esta é a sintaxe geral do comando:

su [opções] [nome de usuário [argumento]]

Quando executado sem nenhuma opção ou argumento, o comando su é executado com privilégios de root. Ele solicitará que você se autentique e use os privilégios sudo temporariamente.

Aqui estão algumas que você pode usar:

-p ou –preserve-environment mantém o mesmo ambiente de shell, composto por HOME, SHELL, USER e LOGNAME.
-s ou –shell permite especificar um ambiente de shell diferente para execução.
-l ou –login executa um script de login para mudar para um nome de usuário diferente. Para executá-lo, é necessário digitar a senha do usuário.

#### 39. Comando htop
O comando htop é um programa interativo que monitora os recursos do sistema e os processos do servidor em tempo real. Ele está disponível na maioria das distribuições Linux e você pode instalá-lo usando o gerenciador de pacotes padrão.

Em comparação com o comando top, o htop tem muitos aprimoramentos e recursos adicionais, como a operação com o mouse e indicadores visuais.

Para usá-lo, execute o seguinte comando:

htop [opções]

Você também pode adicionar opções, como:

-d ou –delay mostra o atraso entre as atualizações em décimos de segundos.
-C ou –no-color ativa o modo monocromático.
-h ou –help exibe a mensagem de ajuda e sai.

#### 40. Comando ps
O status do processo, ou comando ps, produz um snapshot de todos os processos em execução em seu sistema. Os resultados estáticos são obtidos dos arquivos virtuais no sistema de arquivos /proc.

A execução do comando ps sem uma opção ou argumento listará os processos em execução no shell, juntamente com:

A ID exclusiva do processo (PID)
O tipo de terminal (TTY)
O tempo de execução (TIME)
O comando que inicia o processo (CMD)
Aqui estão algumas opções que você pode usar:

-T exibe todos os processos associados à sessão atual do shell.
-u nome_de_usuário lista os processos associados a um usuário específico.
-A ou -e mostra todos os processos em execução.


## WSL2 Windows
