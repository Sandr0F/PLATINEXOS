# Política de Privacidade do PLATINEXOS 1.0.0

Última atualização: 24 de novembro de 2026. Versão 1.0.0.

## Aplicativo e finalidade

O PLATINEXOS, desenvolvido por Sandr0F, é um aplicativo gratuito e independente, sem afiliação com a Valve Corporation. Ele usa dados da Steam para mostrar biblioteca, conquistas e progresso. Favoritos, objetivos, confirmações manuais e preferências são usados para organizar sua experiência no aplicativo.

## Dados utilizados

Você pode informar seu SteamID64 ou a URL do perfil e uma chave pessoal da Steam Web API. Dependendo do que a Steam retornar, o aplicativo pode consultar o identificador e o nome do perfil, a biblioteca, AppIDs, metadados de jogos, nomes e descrições de conquistas, ícones, progresso e datas de desbloqueio. O aplicativo também pode guardar datas e resultados de sincronização, imagens em cache, preferências e os registros pessoais criados por você.

A identificação opcional de jogos instalados lê os arquivos e manifestos locais do cliente Steam. O PLATINEXOS não altera os jogos nem os arquivos de salvamento.

## Credenciais e sincronização na abertura

A chave da Steam Web API permanece em memória durante a sessão, a menos que você escolha salvá-la no Gerenciador de Credenciais do Windows. Nesse caso, ela fica associada ao usuário Windows. O aplicativo envia a chave ao endpoint oficial da Steam Web API para as operações que precisam dela. O aplicativo não solicita a senha Steam nem códigos do Steam Guard e não guarda a chave no banco SQLite, no cache ou nas preferências.

A sincronização na abertura ocorre uma vez e somente se a conta Steam ativa tiver autorização em **Sincronizar esta conta Steam ao abrir o PLATINEXOS** e houver uma chave salva disponível. Salvar a chave é uma decisão separada. Desmarque essa opção em Configurações para revogar a autorização da conta sem remover a chave. Sem autorização, você pode sincronizar manualmente com uma chave válida, salva ou usada apenas em memória.

Se suspeitar de comprometimento da chave, revogue-a e cadastre outra na [página oficial de chaves Steam Web API da Valve](https://steamcommunity.com/dev/apikey). Depois, remova a chave antiga salva no PLATINEXOS e informe a nova. Remover a chave do aplicativo não a revoga na Valve.

## Onde os dados ficam

O aplicativo mantém SQLite, preferências e caches na pasta `%LOCALAPPDATA%\SteamAchievementTracker` do perfil Windows em uso. A credencial salva, quando escolhida, fica no Gerenciador de Credenciais. O aceite dos Termos de Uso é registrado separadamente em `%LOCALAPPDATA%\PLATINEXOS\terms-acceptance.json`, com a versão dos termos, o identificador do documento e a data e a hora do aceite em UTC. A autorização de sincronização na abertura é guardada por conta Steam na subpasta `StartupSynchronization`, no mesmo perfil Windows. Os arquivos que o aplicativo grava localmente ficam no país em que o dispositivo está localizado. O desenvolvedor não recebe esses arquivos nem mantém um servidor para armazená-los. O tratamento realizado pela Valve e as cópias feitas pelo usuário ou por serviços de backup seguem as regras desses serviços.

Contas Windows diferentes usam perfis locais separados. Pessoas que compartilham a mesma conta Windows podem ter acesso aos dados guardados naquele perfil. O aplicativo não criptografa o SQLite nem os arquivos de cache.

A verificação manual de atualizações pode manter um arquivo de coordenação em `%LOCALAPPDATA%\PLATINEXOS\updates\check.lock`. O aplicativo não utiliza esse arquivo para armazenar a chave ou dados da Steam.

## Conexões externas e diagnóstico

As consultas à Steam Web API transmitem à Valve a chave da API e os identificadores e parâmetros necessários à operação, conforme o tipo de consulta. O tratamento realizado pela Valve é independente do armazenamento local do PLATINEXOS. A loja e as redes de distribuição da Steam podem receber solicitações para buscar metadados, capas e ícones. Na abertura, a assinatura by Sandr0F pode consultar por HTTPS o [perfil público Steam de Sandr0F](https://steamcommunity.com/id/Sandr0F/) no formato XML (`?xml=1`) e baixar seu avatar dos servidores de imagens da Steam. Essa consulta não utiliza a chave Steam Web API do usuário. Esses serviços podem receber informações da conexão, como o endereço IP. Links abertos no navegador, inclusive guias e opções de contribuição voluntária, seguem as políticas dos respectivos sites. [Política de Privacidade da Valve](https://store.steampowered.com/privacy_agreement/)

O PLATINEXOS não implementa telemetria própria, publicidade ou envio automático de relatórios ao desenvolvedor. O diagnóstico detalhado da Steam Web API é opcional e apresentado no aplicativo antes de sua execução. Revise qualquer relatório antes de compartilhar.

Na modalidade Portable, o botão Verificar atualizações consulta a API pública do GitHub para verificar as Releases de Sandr0F/PLATINEXOS, sem enviar a chave Steam Web API. Essa consulta é manual e pode transmitir informações de conexão ao GitHub; ela não baixa nem instala atualizações automaticamente.

## Retenção e controle

O armazenamento local permite consultar dados já carregados sem nova sincronização. O aplicativo não elimina esses registros automaticamente por prazo. Para guardar uma cópia do banco local, feche o aplicativo antes de fazer o backup.

**Como interromper novas sincronizações automáticas:** selecione a conta Steam em Configurações e desmarque **Sincronizar esta conta Steam ao abrir o PLATINEXOS**. A chave salva e os dados já sincronizados permanecem. Você pode remover a chave separadamente.

**Como remover os dados locais:** feche completamente o PLATINEXOS. Se desejar, faça antes uma cópia de segurança. Depois, pelo Explorador de Arquivos, acesse `%LOCALAPPDATA%\SteamAchievementTracker` e exclua os arquivos dessa pasta que não queira manter; para apagar todos os arquivos do aplicativo armazenados nessa pasta, exclua a pasta inteira. Essa operação pode remover permanentemente o banco SQLite, preferências, objetivos, confirmações manuais, autorizações de sincronização na abertura e caches, conforme os arquivos presentes. Não a execute se houver informações que deseje preservar. Para remover também o registro local de aceitação dos Termos de Uso, exclua separadamente `%LOCALAPPDATA%\PLATINEXOS\terms-acceptance.json`, se existir; essa exclusão poderá exigir nova aceitação ao abrir o aplicativo. Remova separadamente eventual chave armazenada no Gerenciador de Credenciais do Windows, de preferência pelo próprio aplicativo. A exclusão de arquivos locais não remove dados mantidos pela Valve nem cópias de segurança feitas por terceiros.

Essas instruções referem-se ao armazenamento conhecido da versão 1.0.0 e não apagam automaticamente dados em serviços externos.

## Contato e suporte

Para dúvidas técnicas, relatos de problemas e sugestões, utilize o GitHub Issues do PLATINEXOS: [https://github.com/Sandr0F/PLATINEXOS/issues](https://github.com/Sandr0F/PLATINEXOS/issues). Esse canal é público. Não compartilhe chaves de acesso, senhas, bancos de dados locais, informações pessoais, relatórios não revisados ou capturas de tela que contenham dados sensíveis. Para assuntos privados ou relacionados à privacidade, entre em contato pelo e-mail [platinexos@gmail.com](mailto:platinexos@gmail.com).

**Contato privado para privacidade:** [platinexos@gmail.com](mailto:platinexos@gmail.com). Utilize esse endereço para solicitações que envolvam dados pessoais; não encaminhe esses dados ao GitHub Issues público.
