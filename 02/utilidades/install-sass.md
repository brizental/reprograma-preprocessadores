# Como instalar o SCSS/Sass no Windows

> Esse passo a passo explica como instalar o Sass e tornar ele um comando na linha de comando. Existem que GUIs permitem que você compile o Sass sem ter que tocar em código e elas estão listadas aqui: http://sass-lang.com/install

1. Faça o download do dart-sass pelo link: https://github.com/sass/dart-sass/releases/tag/1.2.0 . Para Windows existem duas versões, dependendo se seu Windows é 32 ou 64bit. Escolha a versão correta para o seu sistema.
2. Extraia o conteúdo da pasta que você acabou de fazer o download.
3. Entre dentro da pasta até encontrar o arquivo `sass`. Copie o caminho para pasta encontrada.
4. Dentro do explorador de arquivos, na barra da esquerda, encontre o link `Meu Computador`, clique com o botão direito nele e selecione o último link da lista.
5. Na barra esquerda da nova janela que foi aberta, clique no link `Configurações avançadas do sistema`.
6. Na parte inferior da nova janela que foi aberta, clique em `Variáveis de ambiente`.
7. Clique no item `Path` na lista de variáveis do sistema.
8. Adicione o caminho da pasta que contém o arquivo `sass` ao `Path`.
9. Salve tudo e reinicie a linha de comando, caso ela esteja aberta.
10. Digite `sass` na linha de comando e certifique-se de que ele reconhece o comando.

---

# Extensão do VSCode para compilar SCSS/Sass

> https://github.com/ritwickdey/vscode-live-sass-compiler

---

# Extensão do Sublime Text para compilar SCSS/Sass

> https://packagecontrol.io/packages/SassBuilder