# PLATINEXOS 1.0.0 — Windows 11 x64 Portable

[English](../README.md) | [Português (Brasil)](../README-pt-BR.md) | [Español (Latinoamérica)](../README-Espanol.md)


O **PLATINEXOS** é um aplicativo gratuito e independente para acompanhar sua biblioteca de jogos e seu progresso nas conquistas da Steam. Não é afiliado, patrocinado ou aprovado pela Valve Corporation. Steam é marca da Valve. O aplicativo não desbloqueia conquistas na Steam, não modifica jogos e não altera arquivos de salvamento.

## Funcionalidades

- Biblioteca Steam com pesquisa, filtros, indicadores e estatísticas.
- Consulta de conquistas, progresso e dados oficiais disponibilizados pela Steam.
- Favoritos e objetivos pessoais, associados à conta correspondente.
- Sincronização manual pela Steam Web API e sincronização na abertura somente mediante autorização específica para a conta e disponibilidade de chave salva.
- Interface em português brasileiro, inglês americano e espanhol latino-americano.
- Termos de Uso, Política de Privacidade e consulta das licenças de terceiros dentro do aplicativo.
- Verificação manual de atualizações da edição Portable pelas Releases públicas de `Sandr0F/PLATINEXOS`, sem download ou instalação automática.

## Requisitos e limitações conhecidos

- **Windows 11 x64**.
- Extração completa do ZIP em pasta acessível ao usuário.
- Internet para sincronizar e obter conteúdo remoto; dados já carregados podem ser consultados offline, conforme o manual.
- SteamID64 ou URL do perfil e chave Steam Web API válida para consultas autenticadas. A obtenção da chave depende das condições da Valve; os dados retornados dependem da privacidade do perfil e da disponibilidade dos serviços.

O pacote inclui .NET e Windows App SDK pelo processo self-contained. Não é necessário manter o cliente Steam aberto para consultar a Web API. A execução sem o cliente Steam instalado foi verificada anteriormente em um ambiente Windows 10; a versão 1.0.0 foi validada em Windows 11 x64. A detecção opcional de jogos instalados depende dos arquivos locais da Steam. Esses resultados não garantem funcionamento em todas as instalações do Windows nem eliminam eventuais requisitos de componentes nativos. Não foram definidos requisitos mínimos de CPU, memória ou espaço livre sem medição.

O executável 1.0.0 não possui assinatura digital. Confira a origem do download e mantenha as proteções do Windows habilitadas. O SHA-256 confirma integridade, não a identidade do editor.

## Como utilizar o Portable

Utilize os anexos desta Release:

1. Baixe o ZIP e seu arquivo `.sha256` exclusivamente nas [Releases oficiais](https://github.com/Sandr0F/PLATINEXOS/releases).
2. No PowerShell, na pasta do download, execute:

   ```powershell
   Get-FileHash -Algorithm SHA256 -LiteralPath '.\PLATINEXOS-1.0.0-win-x64-Portable.zip'
   ```

3. Compare o resultado com o SHA-256 abaixo e com o arquivo de verificação.
4. Extraia **todo** o ZIP para uma pasta do seu usuário. Não execute de dentro do ZIP nem copie apenas o EXE.
5. Abra `Platinexos.exe`, leia os documentos e decida se aceita os termos apresentados.
6. Siga `LEIA-ME.txt` e configure sua conta em **Configurações**.

O Portable mantém dados por perfil Windows. Extrair outra cópia em uma pasta diferente não cria um perfil de dados separado. Não exclua dados existentes para atualizar sem antes consultar as instruções e preservar o que desejar manter.

## Configurar a integração Steam

Obtenha legitimamente sua chave na [página oficial da Valve](https://steamcommunity.com/dev/apikey), utilizando sua própria conta Steam. Consulte suas próprias contas ou perfis cujos titulares tenham solicitado ou autorizado a consulta; o aplicativo não concede acesso a informações privadas.

Em Configurações, informe o SteamID64 ou a URL do perfil e a chave no campo próprio. Não forneça senha Steam nem códigos Steam Guard.

- Salvar a chave no Gerenciador de Credenciais do Windows é **opcional**.
- A autorização **Sincronizar esta conta Steam ao abrir o PLATINEXOS** é independente do salvamento da chave, começa desmarcada e pode ser revogada por conta.
- Sem autorização específica de inicialização, permanece disponível a sincronização manual.
- Não publique sua chave em Issues, capturas de tela, mensagens ou relatórios.
- Se suspeitar de comprometimento, revogue a chave no serviço oficial da Valve, cadastre outra e substitua a chave antiga no aplicativo. Removê-la do aplicativo não a revoga na Valve.

## Termos, privacidade e licenças

O pacote contém os Termos e as Políticas de Privacidade nos três idiomas em `Legal/`, além de `Legal/AVISOS-DE-DIREITOS-AUTORAIS.md`, `Legal/LICENCAS-DE-TERCEIROS.md` e os textos originais em `Legal/Licencas/`. Consulte os documentos integrais e as condições aplicáveis antes do aceite. Os avisos e direitos de terceiros permanecem preservados.

O aplicativo armazena seus arquivos no perfil Windows, com credenciais opcionais separadas no cofre do Windows. A Política explica comunicações externas e instruções de exclusão; excluir uma pasta local não revoga a chave na Valve nem apaga dados de serviços externos.

© 2026 Sandr0F — PLATINEXOS. A identificação não atribui ao desenvolvedor direitos sobre componentes de terceiros. A gratuidade não implica publicação do código-fonte privado ou concessão automática de direitos sobre ele.

## Suporte

Use o [GitHub Issues](https://github.com/Sandr0F/PLATINEXOS/issues) para problemas e sugestões. O canal é público: não envie chaves, senhas, bancos pessoais, caches ou dados sensíveis. Para assuntos privados e de privacidade: [platinexos@gmail.com](mailto:platinexos@gmail.com).

Contribuições ao desenvolvimento independente são voluntárias e não condicionam funcionalidades.

## Segurança e confiabilidade

O PLATINEXOS 1.0.0 é um aplicativo gratuito e independente, desenvolvido para acompanhar jogos, conquistas e progresso na Steam.

Antes de seu lançamento, o aplicativo passou por testes funcionais, verificações de integridade e análises de segurança realizadas por plataformas especializadas.

**Resultados das análises de segurança:**

- **VirusTotal:** nenhum dos 60 mecanismos antivírus detectou ameaças no pacote analisado (0/60).
- **Kaspersky OpenTIP:** arquivo classificado como **Clean (Limpo)**.
- **OPSWAT MetaDefender:** nenhuma detecção nos 21 mecanismos antivírus apresentados (0/21), com resultado geral **No Threats Detected**.

O pacote também passou por inspeções técnicas de seus componentes e dependências, sem identificação de comportamento malicioso que exigisse alterações no aplicativo.

O PLATINEXOS não solicita senhas Steam nem códigos Steam Guard. A integração com a Steam utiliza uma chave pessoal Steam Web API, com opção de armazenamento seguro no Gerenciador de Credenciais do Windows.

Os relatórios das plataformas estão disponíveis para consulta. O SHA-256 oficial permite conferir a integridade do arquivo distribuído, comparando seu conteúdo com o pacote original aprovado.

| Plataforma | Resultado selecionado | Consulta |
|---|---|---|
| VirusTotal | **0/60 detecções antivírus** — reanálise de 25/11/2026 | [Consultar análise no VirusTotal](https://www.virustotal.com/gui/file/eb3a4f50d6a796b35ef0678bbebbdb01c3bacc683ffaf57ab7a10bd4d122cecf/detection) |
| Kaspersky OpenTIP | **Clean (Limpo)** — ZIP definitivo | [Relatório do arquivo](https://opentip.kaspersky.com/EB3A4F50D6A796B35EF0678BBEBBDB01C3BACC683FFAF57AB7A10BD4D122CECF/results?tab=upload) |
| OPSWAT MetaDefender Cloud | **0/21 detecções antivírus**, resultado geral **No Threats Detected** | [Relatório do arquivo](https://metadefender.com/results/hash/EB3A4F50D6A796B35EF0678BBEBBDB01C3BACC683FFAF57AB7A10BD4D122CECF/overview) |

Os números acima são resultados antivírus. O VirusTotal também registrou um indicador comportamental Sigma investigado, e alguns módulos adicionais do MetaDefender não concluíram suas verificações. Consulte as evidências e o alcance dessas verificações no [documento público de segurança](../RELATORIO-DE-SEGURANCA-pt-BR.md), que apresenta as três plataformas selecionadas sem se declarar um histórico integral de todas as auditorias.
## Como consultar os relatórios

[Consultar análise no VirusTotal](https://www.virustotal.com/gui/file/eb3a4f50d6a796b35ef0678bbebbdb01c3bacc683ffaf57ab7a10bd4d122cecf/detection). Link direto confirmado pelo desenvolvedor em janela anônima. Não é necessário novo envio. Nomes de candidatos anteriores correspondem ao mesmo SHA-256.

## Integridade do arquivo aprovado

- Arquivo Portable: `PLATINEXOS-1.0.0-win-x64-Portable.zip`.
- Tamanho: **105.398.429 bytes**.
- Conteúdo: **575 arquivos**.
- SHA-256:

```text
EB3A4F50D6A796B35EF0678BBEBBDB01C3BACC683FFAF57AB7A10BD4D122CECF
```

Arquivo de verificação: `PLATINEXOS-1.0.0-win-x64-Portable.zip.sha256`.

Documentação pública: [Termos de Uso](../TERMOS-DE-USO.md), [Política de Privacidade](../POLITICA-DE-PRIVACIDADE.md), [índice de licenças](../LICENCAS-DE-TERCEIROS.md) e [Avisos de Direitos Autorais](../AVISOS-DE-DIREITOS-AUTORAIS.md).


[Capturas reais do aplicativo](../IMAGENS-pt-BR.md) · [Steam Web API Key](../Guia-Steam-Web-API-Key/GUIA-pt-BR.md) · [Leitura dos documentos jurídicos e licenças originais](../DOCUMENTOS-E-LICENCAS-pt-BR.md)
