# PLATINEXOS

O PLATINEXOS é um aplicativo gratuito para **Windows 11 x64** que ajuda você a acompanhar sua biblioteca de jogos e seu progresso nas conquistas da Steam.

- Consulte sua biblioteca Steam e acompanhe as conquistas de cada jogo.
- Veja indicadores de progresso e estatísticas da biblioteca.
- Organize jogos favoritos e objetivos pessoais.
- Sincronize os dados disponíveis pela Steam Web API.
- Use a interface em português brasileiro, inglês americano ou espanhol latino-americano.

O PLATINEXOS é um projeto independente, sem afiliação, patrocínio ou aprovação da Valve Corporation. Steam é marca da Valve Corporation. O aplicativo não desbloqueia conquistas na Steam.

## Downloads e execução

O ZIP Portable para **Windows 11 x64** estará disponível nas [Releases oficiais](https://github.com/Sandr0F/PLATINEXOS/releases) quando a primeira versão for publicada.

Quando o pacote estiver disponível:

1. Baixe o ZIP e o arquivo `.sha256` correspondente na mesma Release.
2. No PowerShell, use `Get-FileHash -Algorithm SHA256 -LiteralPath '.\nome-do-arquivo.zip'`, substituindo o nome pelo do ZIP baixado. Compare o resultado com o arquivo `.sha256`.
3. Extraia todo o ZIP para uma pasta do seu usuário e abra `Platinexos.exe` sem privilégios de administrador.

O pacote inclui .NET e Windows App SDK e pode ser aberto sem o cliente Steam instalado. A identificação de jogos instalados usa os arquivos locais do cliente Steam. O executável 1.0.0 está sem assinatura digital, por isso o Windows poderá apresentar avisos. Confira a procedência do arquivo e mantenha as proteções do sistema habilitadas. Use o SHA-256 para conferir a integridade do arquivo e baixe o ZIP pela página oficial do projeto.

Na edição **Portable**, use **Configurações → Verificar atualizações** para consultar as Releases públicas do GitHub. Quando houver uma versão mais recente, o aplicativo oferece um link para a página oficial. O download e a instalação são manuais. A futura edição **Microsoft Store** será distribuída e atualizada pela própria loja.

## Sincronização com a Steam

Em **Configurações**, informe o SteamID64 ou a URL do perfil e uma chave pessoal válida da Steam Web API. A sincronização requer conexão à internet e depende dos dados que a Steam disponibiliza. Use a chave somente no campo próprio do aplicativo. [Página oficial para registro da chave](https://steamcommunity.com/dev/apikey)

As preferências, o banco de dados e os caches ficam no perfil do Windows. Salvar a chave no Gerenciador de Credenciais do Windows é opcional. Quando houver uma conta ativa e uma chave salva disponível, a sincronização Steam pode ocorrer ao abrir o aplicativo. Para detalhes sobre armazenamento e remoção de dados, consulte a [Política de Privacidade](POLITICA-DE-PRIVACIDADE.md).

## Documentação

- [Termos de Uso](TERMOS-DE-USO.md)
- [Política de Privacidade](POLITICA-DE-PRIVACIDADE.md)
- [Avisos de Direitos Autorais](AVISOS-DE-DIREITOS-AUTORAIS.md)

Os textos integrais e o índice das licenças de terceiros acompanham o ZIP Portable.

## Suporte

Use o [GitHub Issues do PLATINEXOS](https://github.com/Sandr0F/PLATINEXOS/issues) para relatar problemas e sugerir melhorias. O canal é público. Mantenha senhas, chaves Steam, bancos locais e outras informações sensíveis fora das mensagens e dos anexos.

Para assuntos privados ou relacionados à privacidade, envie um e-mail para [platinexos@gmail.com](mailto:platinexos@gmail.com).
