#  Smart Attendance – Proposta
## 1. O Problema: Ineficiência do Modelo Tradicional

O cenário atual da chamada manual no ambiente universitário apresenta um **gargalo operacional síncrono**, com os seguintes impactos negativos:

* **Desperdício de Tempo:** O professor gasta em média 5 a 10 minutos por sessão realizando a chamada nominal, reduzindo o tempo de exposição de conteúdo.
* **Vulnerabilidade à Fraude:** O sistema é suscetível ao "Buddy Punching" (registro de presença pelo colega) no modelo oral.
* **Interrupção Pedagógica:** A pausa no meio ou início da aula quebra o fluxo cognitivo de alunos e professores.

A tese do projeto é que **reformular o processo manual é ineficaz**; a solução requer a adoção de um processo paralelo e automatizado.

---

## 2. A Solução Proposta 

O Produto Mínimo Viável (MVP) do Smart Attendance para a fase de PI-1 foca na **prova de conceito analítica** e na **simulação do fluxo de uso**.

### 2.1. Arquitetura Conceitual
O sistema utiliza um modelo de **registro distribuído e seguro**, onde o professor abre a chamada, e o aluno a registra em seu dispositivo móvel, em paralelo, utilizando um dos seguintes métodos de validação:

* **QR Code Dinâmico:** Código visual escaneável.
* **Token Alfanumérico Temporal:** Código de 6 dígitos que se atualiza a cada 10/20 segundos, mitigando a fraude por compartilhamento remoto.

### 2.2. Entregáveis Principais do MVP

1.  **Dashboard de Análise de Dados:**
    * **Finalidade:** Comprovar a tese do projeto.
    * **Conteúdo:** Visualização de KPIs que comparam o **Tempo Médio Gasto** e a **Percepção de Fraude** entre o método Manual e o Smart Attendance.

2.  **Protótipo Funcional Básico (Front-end):**
    * **Finalidade:** Simular a experiência de uso.
    * **Fluxo:** Tela inicial com escolha de perfil (Professor/Aluno) → Painel do Professor (Geração de QR Code/Token rotativo simulado) → Painel do Aluno (Interface para leitura do QR Code ou inserção do Token).
  
### 2.3. Pensando em Acessibilidade
| Pilar | Foco Principal | Proposta de Ação |
| :--- | :--- | :--- |
| **1. Acessibilidade Básica** | Mídia e Sentidos | **Sistema SOMENTE de texto:** Sem imagens, vídeos ou áudio para garantir o uso por pessoas com limitações sensoriais. |
| **2. Legibilidade Visual** | Contraste e Leitura | **Alto Contraste Padrão:** Usar cores que garantam fácil legibilidade (ex: preto no branco) para todos os textos. |
| **3. Usabilidade e Fluxo** | Eficiência e Simplicidade | **Fluxo Direto e Curto:** Criar um processo de no máximo 3 etapas para o professor gerar o código e para o aluno registrar a presença, minimizando erros. |
| **4. Acessibilidade Avançada** | Recursos Específicos | **Integração Rybená:** Utilizar o *widget* Rybená (já em uso pelo CEUB) para recursos avançados (Libras, Texto para Fala), evitando o desenvolvimento interno. |
