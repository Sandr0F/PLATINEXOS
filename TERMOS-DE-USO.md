# Termos de Uso do PLATINEXOS 1.0.0

## 1. Sobre o aplicativo

O **PLATINEXOS** é um aplicativo gratuito para Windows 11 x64, desenvolvido por **Sandr0F**, destinado ao acompanhamento da biblioteca de jogos da Steam, à consulta do progresso de conquistas e à organização de favoritos e objetivos pessoais.

O PLATINEXOS não desbloqueia conquistas na Steam, não modifica jogos e não altera arquivos de salvamento.

Eventuais contribuições financeiras ao desenvolvedor são inteiramente voluntárias. Nenhuma funcionalidade do aplicativo depende de pagamento.

O PLATINEXOS é um projeto independente, sem afiliação, patrocínio ou aprovação da **Valve Corporation**. Steam é uma marca da Valve Corporation. As demais marcas, nomes de jogos e serviços pertencem aos respectivos titulares.

## 2. Integração com a Steam

Para configurar a sincronização com a Steam, o usuário deverá informar seu SteamID64 ou a URL do seu perfil Steam, além de uma chave pessoal válida da Steam Web API, na seção Configurações do PLATINEXOS.

A sincronização depende de conexão à internet, da disponibilidade dos serviços da Steam e das informações disponibilizadas pela plataforma para o perfil consultado.

A indicação de um perfil Steam não comprova sua titularidade nem concede acesso a informações privadas ou restritas.

O uso da integração está sujeito aos [Termos da Steam Web API](https://steamcommunity.com/dev/apiterms).

### 2.1. Segurança das credenciais

A chave Steam Web API deve ser obtida legitimamente pelo próprio usuário, em sua conta Steam, no serviço oficial da Valve. O usuário deve consultar suas próprias contas Steam ou perfis de terceiros cujos titulares tenham solicitado ou autorizado a consulta. O PLATINEXOS não concede autorização para acessar informações privadas de terceiros.

O usuário deve manter sua chave da Steam Web API em sigilo e não compartilhá-la com terceiros.

O PLATINEXOS não solicita a senha da conta Steam nem códigos de autenticação do Steam Guard.

O armazenamento persistente da chave no Gerenciador de Credenciais do Windows é opcional.

### 2.2. Sincronização na inicialização

O PLATINEXOS sincroniza a conta Steam ativa na abertura somente se você ativar **Sincronizar esta conta Steam ao abrir o PLATINEXOS** para essa conta e se houver uma chave salva disponível. A opção começa desmarcada, inclusive para contas que já tenham chave salva.

Você pode desmarcar essa opção em Configurações sem apagar a chave e continuar usando a sincronização manual. Consulte a [Política de Privacidade](POLITICA-DE-PRIVACIDADE.md).

A aceitação destes Termos de Uso não substitui as escolhas específicas relacionadas ao armazenamento da chave e à configuração da integração Steam.

## 3. Disponibilidade, garantias e responsabilidade na integração com a Steam

A integração depende da disponibilidade da infraestrutura e dos serviços da Valve. Os dados da Steam podem chegar com atraso, estar incompletos ou apresentar divergências. Os dados e serviços podem ficar temporariamente indisponíveis, e os serviços podem ser alterados, restringidos ou interrompidos.

A Steam Web API, os dados da Steam e os elementos de marca e links da Valve usados na integração são fornecidos no estado em que se encontram, sujeitos a falhas e conforme disponíveis. Na medida permitida pela legislação aplicável, o usuário assume os riscos relativos à qualidade, ao desempenho, à exatidão e ao esforço necessário para utilizar esses recursos.

Dentro dos mesmos limites legais, a Valve, as publicadoras e desenvolvedoras de jogos da Steam e seus fornecedores não prestam declarações nem oferecem garantias ou condições expressas, implícitas ou previstas em lei sobre esses recursos. A exclusão abrange, entre outros aspectos, comerciabilidade, adequação a uma finalidade específica, qualidade da execução, exatidão, titularidade, fruição pacífica, ausência de ônus ou gravames, não violação de direitos de terceiros, acesso ou uso contínuo ou sem erros e garantias ou condições decorrentes de práticas anteriores entre as partes ou de usos comerciais.

Na medida permitida pela legislação aplicável, a Valve e seus fornecedores não respondem por danos decorrentes dos Termos da Steam Web API ou do uso desses recursos, incluindo danos indiretos, consequenciais, especiais, incidentais e punitivos, ainda que tenham sido informados da possibilidade desses danos. A exclusão aplica-se qualquer que seja o fundamento da reclamação, inclusive descumprimento contratual, violação de garantia ou negligência. Ela tem efeito independente do recurso exclusivo previsto abaixo e continua aplicável, nos limites da lei, se esse recurso deixar de cumprir sua finalidade essencial ou for considerado inexigível.

Se o usuário discordar dos Termos da Steam Web API ou tiver uma reclamação ou controvérsia contra a Valve ou seus fornecedores relativa a esses Termos ou aos serviços abrangidos, seu único recurso contratual, na medida permitida por lei, será deixar de utilizar a Steam Web API, os dados da Steam e os elementos de marca e links da Valve.

O PLATINEXOS é desenvolvido de forma independente, sem afiliação ou endosso da Valve. Esta seção preserva os direitos, as garantias e os recursos assegurados por normas de aplicação obrigatória, assim como as responsabilidades legais próprias do desenvolvedor do PLATINEXOS. Para mais informações, consulte os [Termos oficiais da Steam Web API](https://steamcommunity.com/dev/apiterms).

## 4. Licenças e direitos de terceiros

O PLATINEXOS utiliza componentes de terceiros que permanecem sujeitos às respectivas licenças, condições de uso, direitos autorais e avisos legais.

Os textos integrais das licenças e os avisos aplicáveis acompanham a distribuição do aplicativo e podem ser consultados na documentação fornecida.

Informações adicionais estão disponíveis no documento [Avisos de Direitos Autorais](AVISOS-DE-DIREITOS-AUTORAIS.md).

**Estes Termos de Uso não substituem, modificam nem limitam as licenças e as condições específicas dos componentes de terceiros, inclusive os componentes da Microsoft.**

Os direitos concedidos pelas respectivas licenças e pela legislação aplicável permanecem preservados. As condições próprias de redistribuição e utilização desses componentes devem ser observadas conforme seus instrumentos de licenciamento.

### 4.1. Condições Microsoft incluídas no aceite

Consulte os textos integrais do [Windows App SDK Runtime](Licencas/Microsoft.WindowsAppSDK.Runtime-1.8.251106002/license.txt), do [Windows App SDK WinUI](Licencas/Microsoft.WindowsAppSDK.WinUI-1.8.251105000/license.txt), do [Windows SDK](Licencas/Microsoft.Windows.SDK.NET.Ref-10.0.22621.57/sdk_license.rtf), da [.NET Library License](Licencas/Microsoft.NETCore.App.Runtime.win-x64-10.0.13/Microsoft-NET-Library-License.html) e do [Win2D 1.3.2](Licencas/Microsoft.Graphics.Win2D-1.3.2/Microsoft-Win2D-EULA-historica.html). O [índice de licenças](LICENCAS-DE-TERCEIROS.md) identifica os textos por componente e versão, incluindo os demais componentes do Windows App SDK.

A concordância abrange as condições aplicáveis ao destinatário, inclusive as restrições de uso, a preservação dos avisos, as exclusões de garantia e os limites de responsabilidade previstos nos textos aplicáveis. Para quem redistribuir os componentes, também abrange as condições de redistribuição da licença correspondente. Permanecem preservados os direitos assegurados pela legislação aplicável e pelas demais licenças de terceiros.

## 5. Privacidade e armazenamento de dados

O PLATINEXOS utiliza informações fornecidas pelo usuário e dados disponibilizados pela Steam para executar suas funcionalidades.

Determinados dados são armazenados localmente no perfil Windows utilizado para executar o aplicativo. A chave da Steam Web API poderá ser armazenada no Gerenciador de Credenciais do Windows, conforme a escolha do usuário.

A utilização de recursos de sincronização envolve comunicação com serviços externos da Steam, sujeitos às condições e práticas da Valve Corporation.

As informações sobre armazenamento, sincronização, exclusão de arquivos locais e remoção de credenciais estão detalhadas na [Política de Privacidade](POLITICA-DE-PRIVACIDADE.md).

Para solicitações relacionadas à privacidade, utilize o endereço **platinexos@gmail.com**.

## 6. Suporte e comunicação

Quando o repositório público estiver disponível e com o recurso Issues habilitado, problemas técnicos, sugestões e solicitações de melhorias poderão ser encaminhados pelo [GitHub Issues do PLATINEXOS](https://github.com/Sandr0F/PLATINEXOS/issues).

As informações publicadas nesse canal são públicas.

Antes de enviar capturas de tela, relatórios ou outros arquivos, o usuário deve remover chaves de acesso, informações pessoais, credenciais e quaisquer outros dados sensíveis.

Não devem ser anexados bancos de dados locais, arquivos de preferências ou documentos que contenham informações privadas.

Para assuntos relacionados à privacidade ou comunicações que não devam ser públicas, utilize o e-mail **platinexos@gmail.com**.

## 7. Aceitação dos Termos de Uso

Ao selecionar **Aceitar e continuar**, você concorda com estes Termos de Uso e com as condições Microsoft aplicáveis aos componentes identificados na seção 4, disponíveis integralmente para consulta antes da aceitação. Essa ação não autoriza a sincronização Steam na abertura.

Caso não concorde, poderá selecionar **Recusar e sair**, encerrando a inicialização do aplicativo.

O PLATINEXOS registra localmente a versão dos termos aceitos e a data e hora da aceitação, para evitar solicitações repetidas enquanto a versão vigente permanecer inalterada.

Uma nova aceitação poderá ser solicitada quando os termos forem atualizados.

A aceitação destes Termos de Uso não substitui eventuais condições ou licenças próprias de terceiros que sejam aplicáveis ao uso dos respectivos componentes.
