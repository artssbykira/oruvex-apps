# Oruvex — seu sinal. Seu controle.


Aplicativos nativos e simples para lives no Windows. Design e direção de produto: João Rodrigues / Kira, com desenvolvimento assistido por IA.


## Download: 0.2.0-beta.1


[Oruvex Cam](https://github.com/artssbykira/oruvex-apps/releases/download/v0.2.0-beta.1/Oruvex-Cam-0.2.0-beta.1-Windows.zip) · [Oruvex Voice](https://github.com/artssbykira/oruvex-apps/releases/download/v0.2.0-beta.1/Oruvex-Voice-0.2.0-beta.1-Windows.zip) · [Release e instruções](https://github.com/artssbykira/oruvex-apps/releases/tag/v0.2.0-beta.1)


Beta gratuita para teste, não uma promessa de compatibilidade universal. Extraia o ZIP inteiro antes de executar. Binários ainda sem assinatura de código: não ignore alertas de segurança automaticamente.


## Oruvex Cam


Identifica o modelo Canon EOS USB e permite escolher entre as câmeras detectadas. Preview opcional, foco, exposição quando suportada, cinco espaços salvos e bandeja. Ajustes avançados ficam recolhidos.


**O ZIP público não inclui as DLLs proprietárias da Canon.** Obtenha o EDSDK pelo [programa oficial da Canon](https://www.usa.canon.com/support/sdk), conforme suas condições. Use “Adicionar SDK da Canon (x86)” e selecione a pasta binária de 32 bits; depois reabra. Não depende de digiCamControl.


Apenas **EOS Rebel T7** foi verificada no ambiente de desenvolvimento. Outras Canon dependem do SDK, firmware e Live View: suporte experimental. Não suporta Nikon, Sony ou webcams UVC. No OBS/TikTok, selecione **KCC Camera**, identificador legado preservado para não quebrar fontes existentes.


1920×1080/60 pode ampliar e repetir quadros: não garante captura nativa. O modo 1024×576/30 reduz o trabalho de saída. Registro da câmera virtual exige administrador uma vez e após mover a pasta.


## Oruvex Voice


RNNoise na CPU, força ajustável, portão opcional, retorno de teste com volume independente e bandeja. Sem CUDA ou processamento de IA na GPU; não significa consumo zero.


Microfone em **48.000 Hz**, PCM 16 bits ou float 32 bits. No OBS/TikTok escolha **CABLE Output (VB-Audio Virtual Cable)**. Se necessário, use “Instalar saída virtual” e reinicie o Windows. Use fones ao testar o retorno.


**VB-CABLE é donationware da VB-Audio**, não um driver Oruvex. Instalador oficial incluído sem modificações. Origem, download e participação: https://www.vb-cable.com/ · https://vb-audio.com/Services/licensing.htm


## Requisitos, privacidade e testes


Windows 10/11 x64 e .NET Framework 4.x. Cam usa processo x86; Voice x64. Processamento local, sem telemetria ou envio de voz/imagem a servidor nesta versão. Configurações antigas preservadas em `%LOCALAPPDATA%\K Cam App` e `HKCU\Software\KMNC`.


Preview desligado corta o desenho local, não o custo de enviar vídeo. Blocos RNNoise de 10 ms não são uma medida de latência ponta a ponta. Desempenho e compatibilidade variam por máquina. Teste fora de uma live importante.


[Relate problemas](https://github.com/artssbykira/oruvex-apps/issues) com modelo, Windows e versão do SDK. Não envie números de série, gravações privadas, tokens ou logs sem revisá-los.


## Créditos e condições


Softcam (MIT), RNNoise (BSD-3-Clause), NAudio 1.10.0 (Ms-PL) e VB-CABLE (VB-Audio donationware): licenças e créditos nos ZIPs. Canon EDSDK é proprietário e não redistribuído. Sem afiliação ou certificação Canon, OBS, NVIDIA, TikTok ou VB-Audio.


Binários Oruvex gratuitos para avaliação, sem garantia de compatibilidade ou desempenho, respeitados os direitos obrigatórios aplicáveis. Licenças dos terceiros continuam independentes. Código-fonte dos apps não está publicado nesta versão.
