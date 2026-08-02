# MK_ESPECIFICAÇÃO_MÓDULO_EQUIPE

**Código:** M04  
**Nome:** Equipe  
**Categoria:** Núcleo Funcional  
**Versão:** 1.0  
**Status:** Especificação Oficial

---

# 1. Objetivo

O Módulo Equipe constitui o sistema institucional responsável pelo cadastro interno dos integrantes da campanha.

Seu objetivo é registrar, organizar e manter atualizadas as informações pessoais, de contato e de atuação dos membros da equipe, constituindo a fonte oficial de identificação dos integrantes da campanha para utilização pelos demais módulos do MÉTODO KÓLLER.

---

# 2. Escopo

O módulo compreende todos os processos relacionados ao cadastro, atualização e manutenção das informações dos integrantes da equipe da campanha.

Seu escopo restringe-se exclusivamente ao ambiente interno da organização, não contemplando apoiadores, eleitores, fornecedores, parceiros externos ou quaisquer pessoas que não exerçam função institucional na campanha.

---

# 3. Finalidade

O Módulo Equipe tem por finalidade centralizar o cadastro institucional da equipe da campanha, permitindo:

- identificação única dos integrantes;
- armazenamento de informações pessoais;
- armazenamento de informações de contato;
- registro da estrutura organizacional ocupada pelo integrante;
- disponibilização das informações para os demais módulos;
- eliminação de retrabalho por meio do cadastro único;
- fortalecimento da governança das informações.

---

# 4. Conceito

No MÉTODO KÓLLER, Equipe representa o cadastro institucional dos integrantes da campanha.

A entrada padrão das informações ocorre por meio de formulário institucional (Google Forms) de uso interno da campanha.

O módulo não possui finalidade de gestão hierárquica da organização.

Seu papel consiste em manter uma base oficial, íntegra e permanentemente atualizada dos integrantes da campanha, permitindo que outros módulos reutilizem essas informações sempre que necessário.

---

# 5. Natureza do Módulo

O Módulo Equipe constitui um módulo cadastral estruturante do MÉTODO KÓLLER.

Sua função é manter a identificação institucional dos integrantes da campanha e disponibilizar essas informações aos demais módulos do sistema.

O módulo não executa processos operacionais próprios além da manutenção cadastral, atuando como infraestrutura informacional para todo o ecossistema do MÉTODO KÓLLER.

Toda informação referente aos integrantes da equipe deverá possuir origem única, atualização controlada e disponibilidade para reutilização institucional, reduzindo redundâncias e fortalecendo a governança das informações.

---

# 6. Princípios

O módulo deverá observar os seguintes princípios:

- cadastro único;
- uso exclusivamente interno;
- fonte única da verdade;
- integridade das informações;
- rastreabilidade;
- reutilização dos dados;
- integração entre módulos;
- simplicidade operacional;
- escalabilidade;
- governança da informação;
- preservação da memória institucional.

---

# 7. Unidade de Registro

A unidade básica do módulo denomina-se **Integrante da Equipe**.

Considera-se integrante da equipe toda pessoa que exerça função institucional na campanha.

Neste MVP compreendem-se como integrantes:

- Candidato(a);
- Facilitador(a) (coordenação de núcleo);
- Integrante de Núcleo.

Cada integrante deverá possuir apenas um cadastro institucional.

---

# 8. Informações Básicas

Cada integrante deverá permitir, no mínimo, o registro das seguintes informações:

## Identificação

- identificador único;
- data do cadastro;
- nome completo;
- nome social;
- data de nascimento;
- CPF.

## Contato

- WhatsApp;
- telefone;
- e-mail.

## Endereço

- logradouro;
- número;
- complemento;
- bairro;
- município;
- CEP.

## Redes Sociais

- redes sociais do integrante.

## Estrutura Organizacional

- núcleo;
- coordenação;
- cargo;
- função.

As opções de Núcleo, Coordenação, Cargo e Função deverão obedecer ao documento institucional **01 - Manual Operacional**.

Caso determinada função ainda não exista nas opções disponíveis, poderá ser utilizada a opção **Outro**, permitindo seu registro sem comprometer a arquitetura do módulo.

Novos atributos poderão ser incorporados futuramente sem comprometer esta especificação.

---

# 9. Situação do Integrante

Cada integrante deverá possuir situação cadastral.

Situações previstas:

- Ativo;
- Inativo.

A situação Inativo não implica necessariamente desligamento da campanha.

O cadastro deverá permitir ainda o registro de:

- data de ingresso;
- data de desligamento.

---

# 10. Histórico

O módulo deverá preservar o histórico das alterações relevantes do cadastro.

Sempre que aplicável deverão permanecer registrados:

- alterações cadastrais;
- alterações de contatos;
- alterações da estrutura organizacional;
- alterações da situação;
- datas de atualização;
- data de ingresso;
- data de desligamento.

A preservação do histórico constitui mecanismo permanente de memória institucional.

---

# 11. Relacionamentos

O Módulo Equipe poderá integrar-se a qualquer módulo do MÉTODO KÓLLER que necessite identificar integrantes da campanha.

Entre eles, exemplificativamente:

- Agenda;
- Comunicação;
- Mobilização;
- Logística;
- Jurídico;
- Financeiro;
- Inteligência;
- Dashboard.

Os demais módulos deverão reutilizar as informações do Módulo Equipe sempre que possível, evitando duplicidade de cadastros.

---

# 12. Integração

O Módulo Equipe constitui a fonte oficial das informações cadastrais da equipe.

Sempre que possível, os demais módulos deverão consultar este módulo em vez de solicitar novo preenchimento das informações ao usuário.

Essa integração fortalece o princípio do cadastro único e reduz inconsistências.

---

# 13. Automações

O módulo deverá permitir automações destinadas à redução de atividades repetitivas.

Entre elas poderão existir:

- preenchimento automático de documentos;
- preenchimento automático de formulários;
- preenchimento automático de responsáveis em outros módulos;
- sincronização entre bases de dados;
- validações cadastrais;
- atualização compartilhada das informações.

Todas as automações deverão preservar consistência, rastreabilidade e governança das informações.

---

# 14. Indicadores

As informações produzidas pelo módulo deverão permitir a geração automática de indicadores institucionais, incluindo, entre outros:

- quantidade de integrantes cadastrados;
- integrantes ativos;
- integrantes inativos;
- integrantes por núcleo;
- integrantes por função;
- evolução da equipe;
- crescimento da equipe.

Os indicadores deverão ser calculados automaticamente a partir da Base de Dados institucional, sem necessidade de preenchimento manual pelos usuários.

---

# 15. Requisitos Funcionais

O módulo deverá permitir:

- cadastrar integrantes;
- editar cadastros;
- consultar integrantes;
- pesquisar integrantes;
- filtrar registros;
- alterar situação cadastral;
- registrar desligamentos;
- reativar integrantes;
- disponibilizar informações para outros módulos;
- preservar histórico das alterações.

---

# 16. Requisitos Não Funcionais

O módulo deverá observar:

- simplicidade de utilização;
- facilidade de manutenção;
- baixo retrabalho;
- compatibilidade com os demais módulos;
- escalabilidade;
- flexibilidade para evolução;
- preservação da memória institucional.

---

# 17. Premissas

O funcionamento do módulo pressupõe:

- utilização do ecossistema Google como plataforma operacional principal do MÉTODO KÓLLER;
- utilização de Google Forms como entrada oficial dos dados;
- armazenamento institucional das informações;
- compartilhamento controlado com os demais módulos.

---

# 18. Governança

Toda informação registrada deverá permanecer vinculada ao ambiente institucional da campanha.

As informações produzidas pelo módulo constituem patrimônio organizacional e deverão observar os princípios de governança estabelecidos pelo MÉTODO KÓLLER.

Alterações cadastrais deverão ocorrer apenas por usuários autorizados.

---

# 19. Evolução do Módulo

Esta especificação estabelece a arquitetura funcional do Módulo Equipe.

Novas funcionalidades poderão ser incorporadas futuramente desde que preservem:

- os princípios do MÉTODO KÓLLER;
- a compatibilidade com esta especificação;
- a integração com os demais módulos;
- a rastreabilidade das informações;
- a simplicidade operacional.

---

# 20. Considerações Finais

O Módulo Equipe constitui a base institucional oficial de identificação dos integrantes da campanha.

Ao centralizar as informações pessoais, de contato e de atuação da equipe em um único ambiente, elimina redundâncias, fortalece a governança da informação e disponibiliza uma fonte única e confiável de dados para todos os demais módulos do MÉTODO KÓLLER.

Sua arquitetura foi concebida para permanecer simples, escalável, integrada e preparada para acompanhar a evolução do sistema, preservando os princípios fundamentais do método e garantindo que as informações da equipe sejam reutilizadas de forma consistente em todo o ecossistema institucional.