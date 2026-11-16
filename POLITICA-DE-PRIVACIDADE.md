# Política de Privacidade do PLATINEXOS 1.0.0

## Aplicativo e finalidade

O PLATINEXOS, desenvolvido por Sandr0F, é um aplicativo gratuito e independente, sem afiliação com a Valve Corporation. Ele usa dados da Steam para mostrar biblioteca, conquistas e progresso. Favoritos, objetivos, confirmações manuais e preferências são usados para organizar sua experiência no aplicativo.

## Dados utilizados

Você pode informar seu SteamID64 ou a URL do perfil e uma chave pessoal da Steam Web API. Dependendo do que a Steam retornar, o aplicativo pode consultar o identificador e o nome do perfil, a biblioteca, AppIDs, metadados de jogos, nomes e descrições de conquistas, ícones, progresso e datas de desbloqueio. O aplicativo também pode guardar datas e resultados de sincronização, imagens em cache, preferências e os registros pessoais criados por você.

A identificação opcional de jogos instalados lê os arquivos e manifestos locais do cliente Steam. O PLATINEXOS não altera os jogos nem os arquivos de salvamento.

## Credenciais e sincronização na abertura

A chave da Steam Web API permanece em memória durante a sessão, a menos que você escolha salvá-la no Gerenciador de Credenciais do Windows. Nesse caso, ela fica associada ao usuário Windows. O aplicativo envia a chave ao endpoint oficial da Steam Web API para as operações que precisam dela. O aplicativo não solicita a senha Steam nem códigos do Steam Guard e não guarda a chave no banco SQLite, no cache ou nas preferências.

Uma sincronização pode começar automaticamente na abertura quando houver uma conta ativa cadastrada e uma chave salva que o aplicativo consiga recuperar. A tentativa automática ocorre uma vez por abertura e consulta a conta selecionada. Para impedir essa tentativa em futuras aberturas, remova a chave salva nas configurações do aplicativo. Também é possível usar a chave apenas em memória, para sincronizar manualmente durante a sessão. Remover a chave salva não apaga o histórico já armazenado.

## Onde os dados ficam

O aplicativo mantém SQLite, preferências e caches na pasta `%LOCALAPPDATA%\SteamAchievementTracker` do perfil Windows em uso. A credencial salva, quando escolhida, fica no Gerenciador de Credenciais. O aceite dos Termos de Uso é registrado separadamente em `%LOCALAPPDATA%\PLATINEXOS\terms-acceptance.json`, com a versão dos termos, o identificador do documento e a data e a hora do aceite em UTC. O armazenamento pelo aplicativo ocorre no dispositivo onde ele é usado. O país em que os arquivos locais ficam armazenados depende de onde o dispositivo estiver localizado. Essa descrição não se estende aos dados tratados por serviços externos, como a Steam, que seguem as políticas e a infraestrutura dos respectivos operadores. O desenvolvedor não define um país fixo nem mantém um servidor para esses arquivos. Backups ou cópias feitos pelo usuário ou por serviços configurados no Windows seguem as configurações desses serviços.

Contas Windows diferentes usam perfis locais separados. Pessoas que compartilham a mesma conta Windows podem ter acesso aos dados guardados naquele perfil. O aplicativo não criptografa o SQLite nem os arquivos de cache.

## Conexões externas e diagnóstico

As consultas à Steam Web API transmitem à Valve a chave da API e os identificadores e parâmetros necessários à operação, conforme o tipo de consulta. O tratamento realizado pela Valve é independente do armazenamento local do PLATINEXOS. A loja e as redes de distribuição da Steam podem receber solicitações para buscar metadados, capas e ícones. Na abertura, o aplicativo também pode buscar o avatar público do desenvolvedor. Esses serviços podem receber informações da conexão, como o endereço IP. Links abertos no navegador, inclusive guias e opções de contribuição voluntária, seguem as políticas dos respectivos sites. [Política de Privacidade da Valve](https://store.steampowered.com/privacy_agreement/)

O PLATINEXOS não implementa telemetria própria, publicidade ou envio automático de relatórios ao desenvolvedor. O diagnóstico detalhado da Steam Web API é opcional e apresentado no aplicativo antes de sua execução. Revise qualquer relatório antes de compartilhar.

## Retenção e controle

O armazenamento local permite consultar dados já carregados sem nova sincronização. O aplicativo não elimina esses registros automaticamente por prazo. Para guardar uma cópia do banco local, feche o aplicativo antes de fazer o backup.

**Como interromper novas sincronizações automáticas:** remova, nas Configurações do PLATINEXOS, a chave da Steam Web API que foi salva no Gerenciador de Credenciais do Windows. Isso não apaga os dados já sincronizados.

**Como remover os dados locais:** feche completamente o PLATINEXOS. Se desejar, faça antes uma cópia de segurança. Depois, pelo Explorador de Arquivos, acesse `%LOCALAPPDATA%\SteamAchievementTracker` e exclua os arquivos dessa pasta que não queira manter; para apagar todos os arquivos do aplicativo armazenados nessa pasta, exclua a pasta inteira. Essa operação pode remover permanentemente o banco SQLite, preferências, objetivos, confirmações manuais e caches, conforme os arquivos presentes. Não a execute se houver informações que deseje preservar. Remova separadamente eventual chave armazenada no Gerenciador de Credenciais do Windows, de preferência pelo próprio aplicativo. A exclusão de arquivos locais não remove dados mantidos pela Valve nem cópias de segurança feitas por terceiros.

Essas instruções referem-se ao armazenamento conhecido da versão 1.0.0 e não apagam automaticamente dados em serviços externos.

## Contato e suporte

Para dúvidas técnicas gerais, utilize o [GitHub Issues do repositório público do PLATINEXOS](https://github.com/Sandr0F/PLATINEXOS/issues), quando esse repositório estiver disponível. **Esse canal é público: não publique chaves, bancos locais, identificadores pessoais, relatórios não revisados ou capturas sensíveis.**

**Contato privado para privacidade:** [platinexos@gmail.com](mailto:platinexos@gmail.com). Utilize esse endereço para solicitações que envolvam dados pessoais; não encaminhe esses dados ao GitHub Issues público.
