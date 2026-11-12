# JARVIS Android — pacote para gerar APK

Este projeto contém o aplicativo Android em Java e um fluxo do GitHub Actions que compila um APK de depuração.

## Gerar o APK pelo GitHub (sem escrever código)

1. Envie o conteúdo desta pasta para um repositório GitHub.
2. Abra a aba **Actions**.
3. Selecione **Gerar APK do JARVIS** e toque em **Run workflow** (ou aguarde a compilação após enviar para `main`).
4. Quando aparecer um visto verde, abra a execução e baixe **JARVIS-APK** em **Artifacts**.
5. Extraia o ZIP baixado e instale `app-debug.apk` no Android.

Se a execução ficar vermelha, abra-a e envie uma captura da mensagem de erro para receber ajuda.

## Comando Spotify

Com o JARVIS aberto e em primeiro plano, diga:
- “Olá, bebê, papai chegou”; ou
- “Acorda, bebê, papai chegou”.

O aplicativo tenta abrir no Spotify a faixa “Should I Stay or Should I Go”, do The Clash.

**Limites:** o reconhecimento não fica ativo com o aplicativo fechado ou em segundo plano. A abertura da faixa não garante reprodução automática; isso depende do Spotify e do estado da conta/aplicativo.

## IA e resposta por voz

Para conversar com a IA e usar a síntese de voz, também é necessário publicar o backend Node.js e configurar `SERVER_URL` em `MainActivity.java`, além das variáveis `OPENAI_API_KEY` e `FISH_API_KEY` no ambiente do servidor. Não coloque chaves secretas no repositório nem no APK.

O APK de depuração gerado pelo fluxo serve para testes pessoais; não é um pacote de publicação na Play Store.
