# Progresso Técnico

## 1. Visão Geral da Implementação
Para a disciplina de IHC, a equipe desenvolveu um **Protótipo de Alta Fidelidade Funcional**. O objetivo técnico desta etapa foi traduzir os wireframes e fluxos de navegação desenhados no **Figma** para uma interface web interativa.

A implementação atual permite a **visualização do fluxo principal** do sistema (presença em sala de aula), materializando as decisões de design e permitindo testes de usabilidade com usuários finais.

Optou-se por uma arquitetura *Client-Side* (sem backend ativo no momento), utilizando recursos nativos do navegador para simular a persistência de dados e validar as regras de negócio propostas.

## 2. Stack Tecnológica
As ferramentas e tecnologias utilizadas para a construção do protótipo foram:

* **Design & Prototipação:** Figma (Wireframes).
* **Estrutura:** HTML5 (com foco na semântica).
* **Estilização:** CSS3 puro.
    * Uso de Flexbox para layouts.
    * Design Responsivo adaptável via Media Queries.
* **Interatividade:** JavaScript (ES6+).
* **Bibliotecas Externas:**
    * `qrcode.js`: Para geração de QR Codes na interface do professor.
    * `jsQR`: Para decodificação de QR Codes via câmera na interface do aluno.

## 3. Arquitetura do Projeto
A organização dos arquivos no repositório foi estruturada para separar claramente os contextos de cada usuário (Aluno vs. Professor), compartilhando apenas os recursos de estilo e utilitários globais:

```text
prototipo/
    ├── index.html          # Tela de seleção de perfil (Home)
    ├── style.css           # Estilos globais e variáveis de design
    ├── mobile-toggle.js    # Utilitário para simulação de visualização mobile
    ├── aluno/
    │   ├── aluno.html      # Interface de input e leitura de câmera
    │   └── aluno.js        # Lógica de validação do aluno
    └── professor/
        ├── professor.html  # Interface de geração de códigos
        └── professor.js    # Lógica de geração do professor
```

## 4. Funcionalidades Implementadas (Status Atual)

O desenvolvimento técnico focou na viabilização do "Caminho Feliz" (*Happy Path*), utilizando a técnica de **Mocking** (simulação) para substituir o banco de dados.

**A. Fluxo do Professor**
* **Geração de Identificador:** Implementação de algoritmo para gerar códigos aleatórios de 6 dígitos via JavaScript.
* **Feedback Visual:** Conversão imediata do código numérico em um QR Code visualizável na tela.
* **Persistência Simulada:** Uso do `localStorage` (`setItem`) para salvar o código gerado no navegador, permitindo que a "sessão" do aluno consiga validar esse dado posteriormente.

**B. Fluxo do Aluno**
* **Validação de Dados:** O sistema recupera o código salvo pelo professor no `localStorage` e compara com o input do aluno, retornando mensagens de sucesso (Verde) ou erro (Vermelho) em tempo real.
* **Leitura de Câmera:** Integração com a API `navigator.mediaDevices` para acessar a câmera do dispositivo e realizar a leitura do QR Code.

**C. Recursos de IHC e Usabilidade**
* **Simulador Mobile:** Desenvolvimento de um script (`mobile-toggle.js`) que permite alternar a visualização da página para um formato de "smartphone" dentro do desktop, facilitando a validação da interface responsiva durante o desenvolvimento.
* **Feedback de Sistema:** Implementação de feedbacks visuais claros para ações de sucesso (código válido) e erro (código incorreto ou falha na câmera).

## 5. Desafios Técnicos Superados

* **Sincronização de Dados sem Backend:** O principal desafio foi permitir a comunicação entre a tela do Professor e a do Aluno. A solução técnica foi o uso criativo do `localStorage` para compartilhar o estado da aplicação entre as páginas HTML.
* **Acesso ao Hardware:** A implementação da leitura de QR Code exigiu o tratamento de permissões de câmera do navegador e o uso de `requestAnimationFrame` para processar o vídeo frame a frame.