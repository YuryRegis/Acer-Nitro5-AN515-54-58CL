# Acer-Nitro5-AN515-54-58CL

EFI files to boot Mojave Hackintosh on Acer Nitro 5


<p align="center">
  <img width="460" height="300" src="https://i.ibb.co/8jMNF6B/Captura-de-Tela-2020-10-12-a-s-11-41-27.png">
</p>


## Instruções

1. Baixe a ISO do macOS Mojave no site [Olarila](https://www.olarila.com/topic/6278-new-vanilla-olarila-images/);
2. Siga as instruções para [criar seu pendrive bootável](https://www.olarila.com/topic/5794-hackintosh-guide-install-macos-with-vanilla-olarila-image-step-by-step-install-and-post-install-windows-linux-or-mac/);
3. Altere o BOOT na BIOS para o seu pendrive e inicie o processo de Instalação (evite tocar o trackpad, isso irá causar bug que desativa o teclado, você irá precisar de um mouse USB);
4. Após instalação, inicie o macOS Mojave utilizando seu pendrive criado para instalação;
5. Abra as partições EFI do HD/SSD escolhido e do pendrive, através do Clover. Copie e substitua, se precisar, os arquivos do seu HD/SSD pelos arquivos contidos no pendrive (coloquei os arquivos contidos do EFI do meu pendrive na pasta PENDRIVE_BOOT_EFI, caso prefira usar o que eu utilizo);
5. Ejete o pendrive e reinicie o computador, altere o BOOT da BIOS para a partição do seu HD/SSD utilizado para instalação do macOS Mojave;
6. No menu do Clover, escolha iniciar o macOS Mojave, lembre-se de não encostar no trackpad/touchpad para não travar seu teclado, caso isso aconteça será necessário reiniciar o seu Nitro 5;
7. Use o Clover para montar as partições EFI do seu HD/SSD escolhido para instalação do macOS Mojave. Substitua a pasta KEXTS da sua partição EFI>CLOVER pela mesma pasta KEXTS que disponibilizei no GitHub (EFI>CLOVER>KEXTS);
8. Reinicie o seu Hackintosh (pode demorar um pouco mais de 3 minutos para inicializar, mesmo com SSD).

## Observações

Para corrigir o bug do trackpad que inutiliza o teclado, utilizo um kext voodoo que desabilita o trackpad durante as tentativas de ativação do mesmo, dessa forma, podemos usar o teclado sem medo de enconstar no trackpad. O ponto negativo é que este Kext faz 3 tentativas de instalação com intervalos de até 60 segundos cada, o que gera atraso no boot do macOS, mesmo instalado em um SSD.

Deixe um comentário caso encontre uma alternativa melhor para solucionar este problema.

Kext para Airport com placa wireless Intel adicionado. Usar aplicação Heliport para reconhecer as redes disponíveis (créditos: [Alexandre Lima](https://github.com/aclima01)).
- [Airport Kext](https://github.com/OpenIntelWireless/itlwm/releases/tag/v1.2.0-alpha);
- [Heliport App](https://github.com/OpenIntelWireless/HeliPort/releases/tag/v1.0.1)

## Roda ou não roda ?

- Placa de vídeo dedicada Nvidea ❌;
- Intel UHD Graphics 630  ✔️;
- Trackpad ❌;
- WebCam ✔️;
- Teclado ✔️;
- Audio ✔️;
- Rede Ethernet (limitado a 100Mbps) ✔️;
- Rede Wifi ✔️;
- Bluetooth ❌
