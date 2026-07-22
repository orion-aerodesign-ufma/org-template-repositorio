# Política de Segurança

Este documento define as regras mínimas de segurança para os repositórios da Orion AeroDesign.

## 1. Informações que nunca devem ser versionadas

É proibido adicionar ao repositório:

- senhas;
- tokens de acesso;
- chaves de API;
- chaves privadas;
- credenciais de bancos de dados;
- arquivos `.env` contendo informações sensíveis;
- dados pessoais sem autorização;
- informações confidenciais de patrocinadores ou parceiros;
- informações restritas relacionadas à competição.

Antes de realizar um commit, o colaborador deve verificar se nenhum dado sensível foi incluído.

## 2. Variáveis de ambiente

Quando um projeto utilizar variáveis de ambiente, arquivos contendo valores reais não devem ser versionados.

Exemplo:

```text
.env
```

Quando necessário, pode ser disponibilizado um arquivo de exemplo sem dados sensíveis:

```text
.env.example
```

Exemplo:

```text
DATABASE_URL=
API_TOKEN=
SECRET_KEY=
```

## 3. GitHub Secrets

Credenciais necessárias para workflows e automações devem ser armazenadas utilizando mecanismos seguros, como **GitHub Secrets**, e nunca diretamente no código.

Os Secrets devem possuir apenas as permissões necessárias para sua finalidade.

## 4. Tokens e credenciais

Tokens devem:

- possuir o menor nível de permissão possível;
- ser utilizados somente para a finalidade prevista;
- não ser compartilhados entre membros;
- ser revogados quando não forem mais necessários;
- ser substituídos imediatamente em caso de exposição.

## 5. Exposição acidental de credenciais

Caso uma senha, token ou chave seja enviada ao repositório por engano:

1. considerar a credencial comprometida;
2. revogar ou desativar a credencial imediatamente;
3. gerar uma nova credencial;
4. informar um Owner da organização;
5. verificar onde a credencial foi utilizada;
6. corrigir a origem do problema para evitar nova exposição.

Apenas remover a credencial de um commit posterior não é suficiente, pois ela pode continuar presente no histórico do Git.

## 6. Controle de acesso

O acesso aos repositórios deve seguir o princípio do menor privilégio.

Cada membro deve receber somente as permissões necessárias para executar suas atividades.

Os acessos temporários serão controlados manualmente pelos Owners e deverão ser removidos quando:

- a atividade for concluída;
- o membro deixar o projeto;
- ocorrer mudança de setor;
- houver desligamento da equipe;
- a liderança determinar a revogação.

## 7. Contas e autenticação

Cada integrante deve utilizar sua própria conta do GitHub.

É proibido compartilhar contas, senhas ou tokens pessoais.

Recomenda-se o uso de autenticação em dois fatores (2FA) em todas as contas com acesso à organização.

## 8. Repositórios públicos

Os repositórios devem ser privados por padrão.

Antes de tornar qualquer repositório público, deve ser verificado se o conteúdo possui:

- informações sensíveis;
- dados pessoais;
- segredos ou credenciais;
- código ou arquivos de terceiros sem autorização;
- informações estratégicas da competição;
- materiais restritos de patrocinadores ou parceiros.

A mudança de visibilidade deverá ser autorizada pela liderança.

## 9. Comunicação de problemas de segurança

Problemas de segurança identificados não devem ser divulgados publicamente antes de serem avaliados.

O membro deve comunicar o ocorrido a um Owner da organização para que sejam tomadas as medidas necessárias.

## 10. Responsabilidade

Todos os membros e colaboradores são responsáveis por proteger as credenciais, dados e informações aos quais possuem acesso.

Situações não previstas neste documento devem ser comunicadas aos Owners antes da realização de alterações que possam afetar a segurança da organização.
