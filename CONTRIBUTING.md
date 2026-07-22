# Guia de Contribuição

Este documento define o fluxo padrão para contribuições aos repositórios da Orion AeroDesign.

Todos os membros e colaboradores devem seguir estas orientações antes de enviar alterações.

## 1. Fluxo de trabalho

A Orion AeroDesign adota o **GitHub Flow**.

O fluxo básico é:

1. Atualizar a branch `main`.
2. Criar uma nova branch para a atividade.
3. Realizar as alterações necessárias.
4. Fazer commits claros e objetivos.
5. Enviar a branch para o GitHub.
6. Abrir um Pull Request.
7. Aguardar revisão e execução da CI.
8. Corrigir eventuais problemas apontados.
9. Após aprovação, realizar o merge na `main`.

Alterações não devem ser feitas diretamente na branch `main`.

---

## 2. Nome das branches

As branches devem seguir o padrão:

```text
<tipo>/<id-da-ficha>-<descricao-curta>
```

Exemplos:

```text
feat/RQS-ATV-GECO-REP-261001-adicionar-funcionalidade
fix/RQS-ATV-GECO-REP-261001-corrigir-validacao
docs/RQS-ATV-GECO-REP-261001-atualizar-documentacao
ci/RQS-ATV-GECO-REP-261001-configurar-actions
chore/RQS-ATV-GECO-REP-261001-atualizar-configuracao
```

Quando a atividade ainda não possuir uma Ficha de Requisição oficial, deve ser utilizado o identificador definido pela liderança para aquela atividade.

### Tipos permitidos

- `feat`: nova funcionalidade;
- `fix`: correção de erro;
- `docs`: alteração de documentação;
- `test`: criação ou alteração de testes;
- `refactor`: reorganização de código sem mudança de funcionalidade;
- `chore`: manutenção, configuração ou dependências;
- `ci`: alteração relacionada à Integração Contínua.

---

## 3. Commits

Os commits devem ser pequenos, coerentes e representar uma alteração compreensível.

Formato recomendado:

```text
<tipo>: <descricao>
```

Exemplos:

```text
feat: adiciona leitura do sensor de pressao
fix: corrige processamento da telemetria
docs: atualiza instrucoes de instalacao
test: adiciona testes da rotina de calculo
ci: adiciona verificacao automatica no pull request
chore: atualiza configuracao do ambiente
```

Evite mensagens genéricas como:

```text
mudancas
teste
arrumei
novo
final
atualizacao
```

---

## 4. Pull Requests

Toda alteração destinada à `main` deve ser submetida por Pull Request.

O Pull Request deve informar, quando aplicável:

- ID da Ficha de Requisição;
- Issue relacionada;
- objetivo da alteração;
- resumo do que foi modificado;
- forma de testar;
- evidências ou logs;
- riscos ou limitações conhecidos.

O preenchimento será orientado pelo template padrão de Pull Request disponibilizado no repositório.

O autor deve verificar o próprio código antes de solicitar revisão.

---

## 5. Revisão

Durante a fase inicial da estrutura GitHub da Orion AeroDesign, ainda não existem mantenedores formalmente designados.

Por isso, os Pull Requests deverão ser revisados e aprovados por pelo menos um **Owner autorizado da organização** antes do merge na `main`.

Essa política poderá ser atualizada futuramente quando mantenedores ou líderes responsáveis pela revisão técnica forem formalmente definidos.

O autor do Pull Request **não** deve ser o único responsável pela aprovação da própria alteração.

---

## 6. Integração Contínua

Quando houver uma rotina de Integração Contínua configurada, as verificações obrigatórias deverão ser concluídas com sucesso antes do merge.

Dependendo da tecnologia do projeto, a CI poderá executar:

- build;
- lint;
- testes automatizados;
- verificações de estrutura;
- outras validações definidas para o repositório.

Um Pull Request com verificação obrigatória em falha não deve ser integrado à `main`.

---

## 7. Merge

O método padrão recomendado é **Squash Merge**.

Dessa forma, os diferentes commits realizados durante o desenvolvimento de uma branch são consolidados em um único commit ao entrar na `main`, mantendo o histórico principal mais organizado.

Após o merge, a branch utilizada deverá ser removida quando não houver necessidade de mantê-la.

---

## 8. Segurança

Nunca devem ser versionados:

- senhas;
- tokens;
- chaves de API;
- chaves privadas;
- credenciais;
- arquivos `.env` contendo informações sensíveis;
- dados pessoais não autorizados;
- informações confidenciais de patrocinadores, parceiros ou da competição.

Quando necessárias em automações, credenciais devem ser armazenadas utilizando mecanismos seguros, como **GitHub Secrets**.

Qualquer credencial exposta acidentalmente deve ser revogada e substituída imediatamente.

---

## 9. Visibilidade dos repositórios

Os repositórios da Orion AeroDesign devem ser **privados por padrão**.

A mudança de um repositório para público deverá ocorrer somente mediante autorização da liderança e após verificação de:

- propriedade intelectual;
- regulamentos da competição;
- licenças de terceiros;
- informações confidenciais;
- dados pessoais;
- credenciais e segredos.

Os repositórios públicos aprovados utilizarão, por padrão, a licença MIT.

---

## 10. Padrão de nomenclatura dos repositórios

Os repositórios de setores devem seguir:

```text
<setor>-<especialidade>-<categoria>-<nome>
```

Exemplos:

```text
gercon-gcon-docs-estatuto
eltc-ttc-fw-telemetria
estint-aero-sim-estabilidade
```

Prefixos de setor:

```text
estint  = Estrutura e Integração
eltc    = Eletrônica e TT&C
gercon  = Gerência e Comunicação
```

Repositórios institucionais e transversais podem utilizar o prefixo:

```text
org-
```

Exemplo:

```text
org-template-repositorio
org-docs-governanca
```

Nos metadados, o escopo institucional transversal é identificado como:

```text
orion
```

---

## 11. Dúvidas e exceções

Situações não previstas neste documento devem ser encaminhadas aos Owners da organização antes da alteração ser integrada à `main`.

Mudanças nas regras de contribuição devem ser documentadas e aprovadas pela governança responsável da Orion AeroDesign.
