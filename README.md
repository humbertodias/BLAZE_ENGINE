# BLAZE_ENGINE

Testado no Ubuntu 23.10 e Docker 24.0.6, build ed223bc

##  Compilar 

Clone o repositório **BLAZE_ENGINE** e entre na pasta 
```shell
git clone https://github.com/humbertodias/BLAZE_ENGINE 
cd BLAZE_ENGINE
```
Compile
```shell
make SGDK_VERSION=1.70 build-sgdk compile
```
O comando acima fez:
1. Baixa SGDK na versao variável em SGDK_VERSION=1.70
2. Constroi container docker com MingW e SGDK embutidos em /sgdk
3. Compila o projeto no diretorio atual com entrypoint make -f /sgdk/makefile.gen

> Por último, abra o arquivo gerado **./out/rom.bin** no seu emulador genesis "openemu,retroarch,etc"

![image](https://github.com/DanielMoura79/BLAZE_ENGINE/assets/9255997/8daad171-b0e4-4187-a869-056712b36459)

ou através do cmake

```shell
make build
```
