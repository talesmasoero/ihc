# TESTE DE ACESSIBILIDADE — SISTEMA DE PRESENÇA POR QR CODE

Avaliação da acessibilidade das telas de Professor (Geração de QR Code / Código) e Aluno (Validação via QR Code ou Código).

---

## 1. Objetivo do Teste

Avaliar a acessibilidade das telas reais do sistema, considerando:

### Legibilidade e contraste
Verificar se textos, botões e códigos são facilmente legíveis, principalmente em condições de baixa visão.

### Tamanho e área de toque
Confirmar se os botões são suficientemente grandes para usuários com limitações motoras.

### Compreensão visual e cognitiva
Identificar se usuários entendem facilmente os botões “Ler QR Code”, “Digitar Código”, “Parar Geração” e “Validar Código”.

### Uso com tecnologias assistivas
Testar zoom, leitor de tela e navegação por teclado/touch.

### Compreensão do fluxo
Verificar se as telas orientam bem o usuário, mesmo sem instruções adicionais.

---

## 2. Tipo de Teste

### Qualitativo
Focado em:
- clareza dos botões
- contraste das cores
- compreensão das ações
- facilidade para localizar QR Code e campo numérico

### Quantitativo
Medições de:
- tempo de execução  
- número de erros  
- necessidade de ajuda  
- taxa de sucesso  

---

## 3. Participantes

| Participante | Idade | Dispositivo | Condição | Experiência |
|--------------|-------|-------------|----------|-------------|
| Marcos       | 29    | Notebook    | Daltonismo (Deuteranopia) | Alta |
| Helena       | 74    | Desktop  | Baixa visão (usa zoom 150%) | Moderada |

---

## 4. Roteiro do Teste

### Tarefa 1 — Professor
1. Acessar a tela "Professor"  
2. Encontrar e clicar no botão “Parar Geração”  
3. Identificar o QR Code  
4. Ler o código numérico exibido abaixo  

### Tarefa 2 — Aluno
1. Acessar a tela “Aluno”  
2. Localizar os botões “Ler QR Code” e “Digitar Código”  
3. Simular leitura ou digitar o código  
4. Confirmar no botão “Validar Código”  

---

## 5. Participantes e Resultados

### 1. Marcos (29 anos, daltonismo — Notebook)

**Observações na tela do Professor**
- O botão “Parar Geração” tem um roxo escuro com texto branco — legível, porém difícil de diferenciar de outros roxos.  
- O QR Code tem bom contraste e é facilmente identificado.  
- O texto “Código: 484936” está nítido.  

**Observações na tela do Aluno**
- Botões roxos “Ler QR Code” e “Digitar Código” são muito semelhantes.  
- O botão amarelo “Validar Código” é claramente perceptível.  
- Falta de ícones prejudica identificação por forma.  

**Tempo:** 2min  
**Erros:** 0  
**Comentário:** “As funções são claras, mas as cores confundem um pouco.”  
**Resultado:** Sucesso total.

---

### 2. Helena (74 anos, visão reduzida — Smartphone)

**Tela do Professor**
- Com zoom de acessibilidade, o QR Code ficou desproporcional.  
- O QR Code perdeu parte da margem, prejudicando a leitura.  
- O texto “Código: 484936” ficou normal.  

**Tela do Aluno**
- Botões roxos ficaram muito compridos horizontalmente, prejudicando hierarquia.  
- A caixa de texto é visível, mas os dígitos são estreitos.  
- O botão “Validar Código” é claro, porém com texto pequeno.  

**Tempo:** 3min 20s  
**Erros:** 2  
**Comentário:** “Quando aumento a tela, o layout do qr code vaza.”  
**Resultado:** Concluiu com dificuldade.

---

## 6. Conclusões do Teste de Acessibilidade

As telas são simples, porém apresentam problemas:

- Cores escuras e semelhantes, prejudicando daltonismo  
- Textos pequenos para baixa visão  
- Botões largos, mas pouco altos para usuários com dificuldade motora  
- Ausência de ícones prejudica compreensão  
- Zoom quebra partes do layout  
- Botão amarelo é o único realmente acessível  

---

## 7. Principais Dificuldades Identificadas

- Contraste insuficiente entre botões roxos  
- Tamanhos de texto pequenos  
- Baixa altura e pouco espaçamento entre botões  
- QR Code sem legenda descritiva  
- Fonte estreita na caixa de digitação  

---

## 8. Pontos Positivos

- QR Code bem centralizado  
- Alternativa de código numérico acessível  
- Layout simples  
- Botão amarelo altamente visível  

---

## 9. Recomendações de Acessibilidade

### Melhorias Visuais
- Aumentar contraste seguindo WCAG AA  
- Diferenciar tons para hierarquia visual  
- Fonte mínima 18px  

### Melhorias de Usabilidade Motora
- Altura dos botões entre 48–56px  
- Espaçamento mínimo de 12–16px  

### Melhorias Cognitivas
- Adicionar ícones (câmera, teclado, check, QR Code)  
- Adicionar micro-instruções  

### Tecnologias Assistivas
- Incluir aria-labels  
- Melhor adaptação ao zoom  

---

## 10. Conclusão Final

As telas possuem boa estrutura, porém não atendem plenamente aos critérios de acessibilidade para usuários com daltonismo, baixa visão e limitações motoras.  
Com ajustes simples — contraste, tamanhos, ícones e melhor comportamento com zoom — o sistema pode alcançar maior usabilidade universal.
