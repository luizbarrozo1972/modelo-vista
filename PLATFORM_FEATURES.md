# PLATFORM FEATURES - MEU VISTA
## Documentação Completa de Funcionalidades da Plataforma

---

## 1. VISÃO GERAL DA PLATAFORMA

### 1.1 Arquitetura Multi-Plataforma

**Componentes do Sistema:**
- **Vista Planejador (Web):** Interface principal para planejadores financeiros
- **Vista Gestor (Web):** Sistema de gestão para escritórios com múltiplos planejadores
- **Meu Vista App (Mobile):** Aplicativo para clientes finais (iOS e Android)
- **Vista Finance (Web):** Plataforma de produtos financeiros integrada

### 1.2 Modelo de Acesso

**Para Planejadores:**
- Login via app.meuvista.com/v1/auth/login
- Acesso baseado em plano contratado (Ignição, Business, Escalada)
- Multi-sessão permitida (web + mobile)

**Para Clientes Finais:**
- App mobile Meu Vista (disponível nas stores)
- Credenciais fornecidas pelo planejador
- Acesso read-only a informações pessoais

---

## 2. MÓDULO: DASHBOARD E HOME

### 2.1 Dashboard do Planejador

**Funcionalidades Principais:**
- **Visão Geral de Clientes:**
  - Lista de clientes ativos
  - Status de cada cliente (ativo, inativo, prospect)
  - Última interação registrada
  - Alertas e pendências

- **Métricas de Desempenho:**
  - Número de clientes ativos
  - Receita recorrente mensal estimada
  - Taxa de conclusão de planos
  - Tarefas pendentes

- **Atalhos Rápidos:**
  - Criar novo cliente
  - Gerar diagnóstico
  - Acessar último cliente visualizado
  - Agendar reunião

- **Notificações:**
  - Atualizações de contas conectadas
  - Alertas de orçamento dos clientes
  - Vencimentos de dívidas
  - Marcos de sonhos atingidos

### 2.2 Home do Cliente (App Mobile)

**Interface Intuitiva Incluindo:**
- **Resumo Financeiro:**
  - Saldo total consolidado
  - Patrimônio líquido
  - Resultado do mês (receitas - despesas)

- **Progresso de Sonhos:**
  - Cards visuais para cada sonho/meta
  - Barra de progresso (% alcançado)
  - Valor faltante e prazo estimado

- **Próximas Ações:**
  - Contas a pagar próximas
  - Investimentos a vencer
  - Reuniões agendadas com planejador

- **Acesso Rápido:**
  - Adicionar despesa
  - Ver extrato completo
  - Consultar investimentos
  - Mensagens com planejador

---

## 3. MÓDULO: GESTÃO DE CLIENTES

### 3.1 Cadastro de Clientes

**Informações Coletadas:**
- **Dados Pessoais:**
  - Nome completo
  - CPF
  - Data de nascimento
  - Estado civil
  - Dependentes
  - Endereço
  - Contatos (email, telefone, WhatsApp)

- **Perfil Financeiro:**
  - Ocupação profissional
  - Renda mensal estimada
  - Nível de educação financeira (autoavaliação)
  - Perfil de risco (conservador, moderado, arrojado)

- **Configurações de Acesso:**
  - Gerar credenciais para app mobile
  - Permissões de visualização
  - Frequência de relatórios automáticos

### 3.2 Relacionamento e CRM

**Histórico de Interações:**
- Timeline de todas as interações
- Registro de reuniões (datas, pautas, decisões)
- Anotações privadas do planejador
- Documentos anexados

**Atas de Reunião:**
- Template estruturado para documentação
- Campos:
  - Data e hora
  - Assuntos tratados
  - Decisões tomadas
  - Ações definidas (quem, o quê, quando)
  - Próxima reunião agendada
- Compartilhamento com cliente via app

**Gestão de Tarefas:**
- To-dos vinculados a cada cliente
- Prazos e lembretes
- Status (pendente, em andamento, concluído)
- Integração com calendário

**Comunicação:**
- Sistema de mensagens interno (cliente-planejador)
- Notificações push via app
- Email automático para comunicações importantes

### 3.3 Gestão Multi-Cliente (Vista Gestor)

**Recursos para Escritórios:**
- **Visão Consolidada:**
  - Dashboard com todos os clientes da empresa
  - Métricas agregadas por planejador
  - Performance da equipe

- **Distribuição de Clientes:**
  - Atribuição de clientes a planejadores específicos
  - Transferência de carteira
  - Clientes compartilhados (co-planejamento)

- **Permissões e Hierarquia:**
  - Administrador (acesso total)
  - Planejador sênior (supervisão)
  - Planejador júnior (clientes atribuídos)
  - Assistente (read-only)

- **White Label:**
  - Personalização de logo e cores
  - Domínio customizado (opcional)
  - Nome da empresa em relatórios

---

## 4. MÓDULO: CONEXÃO DE CONTAS E OPEN FINANCE

### 4.1 Integração Open Finance

**Funcionalidades:**
- **Conexão com Instituições Financeiras:**
  - Bancos (conta corrente, poupança)
  - Corretoras de valores
  - Cooperativas de crédito
  - Fintechs

- **Dados Sincronizados:**
  - Saldos em tempo real
  - Extratos de transações
  - Investimentos
  - Cartões de crédito (faturas e limites)
  - Empréstimos e financiamentos

- **Processo de Conexão:**
  1. Cliente seleciona instituição na interface
  2. Autenticação via Open Finance (redirect para banco)
  3. Autorização de compartilhamento de dados
  4. Sincronização inicial completa
  5. Atualizações automáticas periódicas (diárias)

- **Gestão de Consentimentos:**
  - Visualização de contas conectadas
  - Status de cada conexão (ativa, expirada, erro)
  - Renovação de consentimento (validade típica: 90 dias)
  - Revogação de acesso

### 4.2 Integração Kinvo API

**Consolidação de Investimentos:**
- **Ativos Suportados:**
  - Ações (B3)
  - Fundos de investimento
  - Tesouro Direto
  - CDBs, LCIs, LCAs
  - Debêntures
  - Fundos imobiliários (FIIs)
  - ETFs e BDRs
  - Criptomoedas (via exchanges integradas)

- **Dados Importados:**
  - Posição atualizada de cada ativo
  - Cotação em tempo real
  - Rentabilidade histórica
  - Distribuição de proventos
  - Custos e taxas

- **Sincronização:**
  - Automática noturna
  - Manual sob demanda (botão "Sincronizar")
  - Notificação de inconsistências

### 4.3 Importação Manual

**Métodos Alternativos:**
- **Upload de Planilhas:**
  - Excel/CSV com template padronizado
  - Mapeamento automático de colunas
  - Validação de dados

- **Entrada Manual:**
  - Formulários para cada tipo de ativo/conta
  - Campos obrigatórios e opcionais
  - Sugestões baseadas em histórico

- **Importação de Extratos:**
  - PDF parsing (OCR básico)
  - Categorização manual assistida

### 4.4 Gerenciamento de Erros

**Tratamento de Problemas:**
- Indicador visual de contas com erro de sincronização
- Mensagens claras sobre o problema (senha alterada, consentimento expirado, banco offline)
- Passo a passo para resolução
- Suporte via chat/email

---

## 5. MÓDULO: ORÇAMENTO E FLUXO DE CAIXA

### 5.1 Criação de Orçamento

**Estrutura Personalizável:**
- **Categorias de Receita:**
  - Salário
  - Renda variável (comissões, bônus)
  - Renda passiva (aluguéis, dividendos)
  - Outras receitas
  - Subcategorias customizáveis

- **Categorias de Despesa:**
  - Moradia (aluguel, condomínio, IPTU, luz, água, gás, internet)
  - Transporte (combustível, estacionamento, transporte público, manutenção)
  - Alimentação (supermercado, restaurantes, delivery)
  - Saúde (plano de saúde, consultas, medicamentos)
  - Educação (mensalidades, cursos, livros)
  - Lazer e entretenimento
  - Vestuário
  - Seguros
  - Impostos
  - Dívidas
  - Investimentos (poupança forçada)
  - Subcategorias customizáveis

**Flexibilidade:**
- Planejador pode criar, editar ou excluir categorias
- Templates prontos por perfil de cliente
- Estrutura hierárquica (categoria > subcategoria)

### 5.2 Planejamento vs. Realizado

**Funcionalidades:**
- **Orçamento Planejado:**
  - Valores estimados por categoria
  - Frequência (mensal, anual, eventual)
  - Sazonalidade (ex: IPTU anual)

- **Realizado:**
  - Transações reais categorizadas
  - Importadas via Open Finance ou manuais
  - Associação automática a categorias (machine learning)

- **Comparação:**
  - Dashboard visual (planejado vs. realizado)
  - % de aderência ao orçamento
  - Alertas de estouro de categoria
  - Gráficos de tendência mensal

### 5.3 Extrato Consolidado

**Visualização de Transações:**
- **Filtros:**
  - Por período (último mês, trimestre, ano, customizado)
  - Por conta (todas ou específica)
  - Por categoria
  - Por tipo (receita, despesa)
  - Por status (efetivado, agendado)

- **Informações Exibidas:**
  - Data
  - Descrição original
  - Categoria atribuída
  - Valor
  - Conta de origem
  - Botão de edição (recategorizar, dividir transação)

- **Ações:**
  - Recategorização em massa
  - Exclusão de transações (ex: transferências entre contas próprias)
  - Adição de notas/observações
  - Marcar como recorrente

### 5.4 Projeção de Fluxo de Caixa

**Visão Futura:**
- **Receitas Futuras:**
  - Baseadas em padrão histórico
  - Receitas agendadas (salário, aluguéis)
  - Entrada de investimentos programados

- **Despesas Futuras:**
  - Contas fixas recorrentes
  - Cartões de crédito (próximas faturas)
  - Parcelamentos em andamento
  - Despesas sazonais previstas

- **Gráfico de Projeção:**
  - Eixo X: Meses futuros (6-12 meses)
  - Eixo Y: Saldo acumulado
  - Linhas: Receitas, Despesas, Saldo líquido
  - Alertas de meses com saldo negativo

### 5.5 Gestão de Despesas via App Mobile

**Funcionalidades Cliente:**
- **Adição Rápida:**
  - Botão flutuante "+" na home
  - Formulário simples: valor, categoria, descrição
  - Foto de nota fiscal (opcional)
  - Geolocalização automática (opcional)

- **Categorização Inteligente:**
  - Sugestões baseadas em histórico
  - Aprendizado de padrões (ex: "Posto XYZ" = Transporte)

- **Alertas de Orçamento:**
  - Notificação ao atingir 80% do orçamento de categoria
  - Alerta de estouro
  - Resumo semanal de gastos

---

## 6. MÓDULO: PATRIMÔNIO E INVESTIMENTOS

### 6.1 Consolidação de Patrimônio

**Visão 360° de Ativos:**
- **Patrimônio Financeiro:**
  - Contas correntes e poupança
  - Investimentos de renda fixa
  - Investimentos de renda variável
  - Previdência privada (PGBL, VGBL)
  - Criptomoedas
  - Outros ativos financeiros

- **Patrimônio Não-Financeiro:**
  - Imóveis (residencial, comercial, terrenos)
  - Veículos (carros, motos, embarcações)
  - Participações em empresas
  - Bens de valor (obras de arte, joias)
  - Outros bens tangíveis

**Registro de Ativos Não-Financeiros:**
- Formulário detalhado:
  - Tipo de bem
  - Descrição
  - Valor estimado atual
  - Data de aquisição
  - Valor de aquisição
  - Forma de aquisição (compra à vista, financiado, herança, doação)
  - Se financiado: saldo devedor, prestações restantes
  - Fotos e documentos anexados
  - Notas/observações

**Atualização de Valores:**
- Automática para ativos financeiros (via APIs)
- Manual para não-financeiros (revisão periódica sugerida)
- Histórico de valorização/desvalorização

### 6.2 Análise de Investimentos

**Dashboard de Investimentos:**
- **Visão Consolidada:**
  - Valor total investido
  - Rentabilidade global (% e R$)
  - Comparação com benchmarks (CDI, IPCA, Ibovespa)

- **Distribuição de Alocação:**
  - Por classe de ativo (renda fixa, variável, previdência)
  - Por instituição financeira
  - Por risco (conservador, moderado, arrojado)
  - Por liquidez (imediata, curto prazo, longo prazo)
  - Por sonho/objetivo (se vinculado)

- **Gráficos e Visualizações:**
  - Pizza (distribuição percentual)
  - Barras (evolução temporal)
  - Linha (rentabilidade acumulada)

**Análise Detalhada por Ativo:**
- Nome e código (ticker)
- Instituição custodiante
- Quantidade/cotas
- Valor aplicado
- Valor atual
- Rentabilidade (% e R$)
- Prazo de vencimento (se aplicável)
- Taxa de administração
- Come-cotas (fundos)
- Tributação aplicável

**Recomendações Automáticas:**
- Rebalanceamento de carteira
- Ativos com baixa performance
- Concentração excessiva
- Desenquadramento do perfil de risco

### 6.3 Gestão de Dívidas

**Cadastro de Dívidas:**
- **Informações Coletadas:**
  - Tipo (cartão de crédito, empréstimo pessoal, financiamento imobiliário, veículo, outros)
  - Instituição credora
  - Saldo devedor total
  - Taxa de juros (% a.m. ou a.a.)
  - Valor da prestação
  - Data de vencimento
  - Número de parcelas restantes
  - Garantias (se houver)

- **Importação Automática:**
  - Via Open Finance (empréstimos e financiamentos)
  - Cartões de crédito (faturas e parcelamentos)

**Estratégias de Quitação:**
- **Simulações:**
  - Método bola de neve (menor saldo primeiro)
  - Método avalanche (maior taxa de juros primeiro)
  - Amortização extraordinária (quanto economizar pagando antecipado)

- **Visualização:**
  - Timeline de quitação de todas as dívidas
  - Juros totais pagos vs. economizados
  - Data estimada de liberdade das dívidas

**Alertas:**
- Vencimento de parcelas
- Atraso de pagamento
- Oportunidades de portabilidade (taxas menores)

---

## 7. MÓDULO: SONHOS E METAS

### 7.1 Cadastro de Sonhos

**Definição de Objetivos:**
- **Informações do Sonho:**
  - Nome/descrição (ex: "Casa própria", "Viagem para Europa", "Aposentadoria")
  - Valor necessário (R$)
  - Prazo desejado (meses/anos)
  - Prioridade (alta, média, baixa)
  - Categoria (educação, moradia, lazer, independência financeira)

- **Contexto Adicional:**
  - Motivação (por que esse sonho é importante)
  - Imagem representativa (foto ou ícone)
  - Notas descritivas

**Múltiplos Sonhos:**
- Cliente pode ter dezenas de sonhos cadastrados
- Hierarquização por prioridade
- Sonhos de curto (< 1 ano), médio (1-5 anos) e longo prazo (> 5 anos)

### 7.2 Transformação de Sonhos em Planos

**Planejamento Estruturado:**
- **Cálculo Automático:**
  - Valor necessário: R$
  - Prazo: X meses
  - Valor já acumulado: R$ Y
  - Faltam: R$ Z
  - Aporte mensal necessário: R$ W (considerando rentabilidade estimada)

- **Simulação Interativa:**
  - Alterar prazo → recalcula aporte necessário
  - Alterar aporte → recalcula prazo
  - Definir rentabilidade esperada (conservador, moderado, arrojado)

- **Viabilidade:**
  - Análise de capacidade de poupança (baseado em orçamento)
  - Sugestões de ajustes (reduzir gastos em categoria X para viabilizar sonho)

### 7.3 Vinculação de Investimentos a Sonhos

**Alocação Direcionada:**
- **Conexão Ativo → Sonho:**
  - Cada investimento pode ser vinculado a um ou mais sonhos
  - Proporção de alocação definível (ex: 50% deste CDB para "Casa", 50% para "Aposentadoria")

- **Visualização:**
  - Card de cada sonho mostra quais investimentos estão financiando
  - Dashboard de investimentos mostra a qual sonho cada ativo está vinculado

**Benefícios Psicológicos:**
- Cliente vê claramente que investimentos têm propósito
- Reduz tentação de resgates impulsivos
- Aumenta engajamento e satisfação

### 7.4 Acompanhamento de Progresso

**Dashboard de Sonhos:**
- **Para Cada Sonho:**
  - Barra de progresso visual (% alcançado)
  - Valor atual vs. valor meta
  - Tempo decorrido vs. tempo restante
  - Status: no prazo, atrasado, antecipado

- **Gamificação:**
  - Marcos celebratórios (25%, 50%, 75%, 100%)
  - Notificações de conquista
  - Histórico de evolução (gráfico linha do tempo)

**Reavaliação Periódica:**
- Revisões programadas (trimestral, semestral, anual)
- Ajuste de valores, prazos ou prioridades
- Arquivamento de sonhos conquistados ou abandonados

### 7.5 Planejamento de Aposentadoria

**Módulo Especializado:**
- **Dados de Entrada:**
  - Idade atual
  - Idade desejada de aposentadoria
  - Expectativa de vida
  - Padrão de vida desejado na aposentadoria (% da renda atual)
  - Fontes de renda previstas (INSS, previdência privada, aluguéis)

- **Cálculos:**
  - Gap de renda (diferença entre necessário e previsto)
  - Patrimônio necessário para preencher gap
  - Aporte mensal necessário até a aposentadoria
  - Simulações de diferentes cenários

- **Visualização:**
  - Timeline até aposentadoria
  - Projeção de renda passiva
  - Sustentabilidade do patrimônio (renda perpétua vs. esgotamento)

---

## 8. MÓDULO: DIAGNÓSTICO FINANCEIRO

### 8.1 Geração Automática de Diagnóstico

**Processo:**
1. Planejador seleciona cliente
2. Clica em "Gerar Diagnóstico"
3. Sistema consolida todos os dados (orçamento, patrimônio, dívidas, sonhos)
4. Algoritmo analisa e produz relatório estruturado
5. PDF gerado em segundos

**Seções do Diagnóstico:**
- **Resumo Executivo:**
  - Situação financeira atual (saudável, atenção, crítico)
  - Principais achados
  - Recomendações prioritárias

- **Análise de Orçamento:**
  - Receitas e despesas do período
  - Comparação com médias de mercado (benchmarks)
  - Categorias com gastos excessivos
  - Taxa de poupança (% da renda)

- **Análise de Patrimônio:**
  - Evolução patrimonial (gráfico temporal)
  - Distribuição de ativos
  - Liquidez patrimonial
  - Qualidade dos investimentos

- **Análise de Endividamento:**
  - Índice de endividamento (dívidas / patrimônio)
  - Comprometimento de renda (parcelas / receita)
  - Custo médio de dívidas
  - Priorização de quitação

- **Análise de Proteção:**
  - Reserva de emergência (suficiente, insuficiente)
  - Seguros contratados
  - Exposição a riscos não cobertos

- **Análise de Sonhos:**
  - Viabilidade de cada sonho
  - Conflitos de priorização (recursos insuficientes para todos)
  - Sugestões de ajuste

**Design Visual:**
- Gráficos coloridos e intuitivos
- Ícones e indicadores visuais (verde, amarelo, vermelho)
- Layout profissional e limpo
- Marca do planejador (se white label)

### 8.2 Personalização do Diagnóstico

**Ajustes Possíveis:**
- Incluir/excluir seções específicas
- Adicionar textos customizados
- Inserir recomendações manuais
- Anexar documentos complementares

**Versionamento:**
- Histórico de diagnósticos gerados
- Comparação entre versões (evolução do cliente)

### 8.3 Apresentação ao Cliente

**Formatos de Entrega:**
- **PDF Download:**
  - Profissional e completo
  - Enviável por email
  - Imprimível

- **Visualização no App:**
  - Cliente acessa via app mobile
  - Versão interativa (clica em gráficos para detalhes)

- **Reunião Virtual:**
  - Apresentação em tela compartilhada
  - Modo apresentação (full screen)

### 8.4 Resumo Vista (Anual)

**Relatório de Fim de Ano:**
- **Visão Consolidada do Ano:**
  - Evolução patrimonial anual
  - Total de receitas e despesas
  - Principais conquistas (sonhos atingidos, dívidas quitadas)
  - Desafios enfrentados

- **Projeção para Próximo Ano:**
  - Metas estabelecidas
  - Ajustes planejados
  - Expectativas de crescimento

**Uso:**
- Reunião de revisão anual
- Ferramenta de retenção de cliente
- Demonstração de valor do serviço de planejamento

---

## 9. MÓDULO: RELATÓRIOS E ANÁLISES

### 9.1 Tipos de Relatórios

**Relatórios Padrão:**
1. **Relatório de Orçamento:**
   - Receitas e despesas detalhadas
   - Comparativo planejado vs. realizado
   - Análise de variações

2. **Relatório de Patrimônio:**
   - Posição consolidada de ativos
   - Distribuição e alocação
   - Rentabilidade por ativo e global

3. **Relatório de Dívidas:**
   - Saldo devedor total
   - Cronograma de pagamentos
   - Custo total (juros pagos)

4. **Relatório de Progresso de Sonhos:**
   - Status de cada objetivo
   - Aderência ao planejamento
   - Projeção de alcance

5. **Relatório Consolidado:**
   - Todos os módulos em um documento
   - Visão holística

**Relatórios Customizados:**
- Planejador pode criar templates próprios
- Seleção de campos e seções
- Salvamento de modelos para reuso

### 9.2 Periodicidade de Relatórios

**Automação:**
- **Mensal:** Envio automático ao cliente no início do mês (resumo do mês anterior)
- **Trimestral:** Análise de tendências de 3 meses
- **Anual:** Resumo Vista completo

**Configuração:**
- Planejador define frequência por cliente
- Cliente pode solicitar relatório sob demanda via app

### 9.3 Análises Comparativas

**Benchmarking:**
- **Comparação com Médias de Mercado:**
  - Gastos por categoria vs. média nacional
  - Taxa de poupança vs. recomendado
  - Alocação de investimentos vs. perfil de risco

- **Comparação Temporal:**
  - Este mês vs. mês anterior
  - Este ano vs. ano anterior
  - Tendências de longo prazo

**Análises Preditivas (Futuro):**
- Machine learning para prever despesas futuras
- Identificação de padrões sazonais
- Alertas proativos de riscos

---

## 10. MÓDULO: VISTA FINANCE

### 10.1 Marketplace de Produtos Financeiros

**Produtos Disponíveis:**
1. **Consórcios:**
   - Imóveis
   - Veículos
   - Serviços
   - Múltiplas administradoras parceiras

2. **Home Equity:**
   - Crédito com garantia de imóvel
   - Taxas reduzidas
   - Prazos longos (até 20 anos)

3. **Financiamento Imobiliário:**
   - Compra de imóveis novos e usados
   - Portabilidade de financiamento
   - Simulações com múltiplos bancos

4. **Financiamento de Veículos:**
   - Carros novos e usados
   - Motos
   - Caminhões
   - Taxas competitivas

5. **Empréstimos Consignados:**
   - Para aposentados e funcionários públicos
   - Taxas reduzidas
   - Desconto em folha

### 10.2 Fluxo de Trabalho

**Para Planejador:**
1. **Identificação de Necessidade:**
   - Durante planejamento, identifica necessidade de crédito do cliente

2. **Acesso ao Vista Finance:**
   - Login integrado (mesmas credenciais)
   - Seleção do tipo de produto

3. **Simulação:**
   - Preenchimento de dados do cliente
   - Valor desejado, prazo, garantias
   - Sistema consulta múltiplas instituições
   - Comparativo de propostas (taxa, prazo, valor parcela)

4. **Proposta:**
   - Seleção da melhor opção
   - Envio de documentação do cliente
   - Acompanhamento de análise

5. **Aprovação e Contratação:**
   - Instituição aprova crédito
   - Cliente assina contrato
   - Liberação de recursos

6. **Comissão:**
   - Planejador recebe comissão sobre valor contratado
   - Pagamento direto pela instituição parceira
   - Tabela de comissões transparente (varia por produto e instituição)

**Para Cliente:**
- Recebe proposta via app ou email
- Acessa documentação necessária
- Assina digitalmente
- Acompanha status da análise

### 10.3 Integração com Planejamento

**Visão Holística:**
- Produtos de crédito são avaliados no contexto do planejamento financeiro global
- Não é venda isolada, mas solução integrada
- Análise de impacto no orçamento e capacidade de pagamento

**Exemplo de Uso:**
- Cliente quer comprar imóvel (sonho cadastrado)
- Planejador simula financiamento via Vista Finance
- Parcela é incorporada ao orçamento
- Impacto em outros sonhos é analisado
- Decisão informada

### 10.4 Compliance e Regulação

**Certificações Recomendadas:**
- CPA-10, CPA-20, CEA (investimentos)
- SUSEP (seguros)
- CFP®, PCA-10 (planejamento financeiro)

**Observação:** Não é obrigatório, mas fortemente recomendado para credibilidade e compliance

**Materiais de Apoio:**
- Instituições parceiras fornecem materiais de compliance
- Treinamentos sobre produtos
- Suporte comercial

---

## 11. MÓDULO: COLABORAÇÃO E COMUNICAÇÃO

### 11.1 Sistema de Mensagens

**Cliente ↔ Planejador:**
- **Chat Interno:**
  - Mensagens de texto
  - Compartilhamento de arquivos (fotos, PDFs)
  - Notificações push

- **Casos de Uso:**
  - Cliente tira dúvidas rápidas
  - Planejador solicita documentos
  - Lembretes de tarefas pendentes

### 11.2 Reuniões e Agendamento

**Agendamento Integrado:**
- Calendário do planejador
- Cliente pode visualizar horários disponíveis
- Agendamento via app
- Confirmação e lembretes automáticos

**Atas de Reunião:**
- Template estruturado preenchido durante ou após reunião
- Compartilhamento com cliente (transparência)
- Histórico acessível

### 11.3 Compartilhamento de Conteúdo

**Educação Financeira:**
- Planejador pode compartilhar artigos, vídeos, materiais educativos
- Biblioteca de conteúdo curado pelo Meu Vista
- Personalização por perfil de cliente

---

## 12. MÓDULO: VISTA GESTOR (MULTI-PLANEJADOR)

### 12.1 Gestão de Equipe

**Recursos para Escritórios:**
- **Dashboard Consolidado:**
  - Todos os clientes do escritório
  - Planejadores ativos
  - Métricas agregadas

- **Distribuição de Trabalho:**
  - Atribuir clientes a planejadores
  - Balanceamento de carga
  - Especialização (ex: planejador focado em alta renda)

### 12.2 Permissões e Controle

**Hierarquia de Acesso:**
- **Administrador:**
  - Acesso total
  - Gestão de planos e pagamentos
  - Configurações de white label
  - Contratação/remoção de planejadores

- **Supervisor:**
  - Visualização de todos os clientes
  - Auditorias de trabalho de planejadores
  - Relatórios gerenciais

- **Planejador:**
  - Acesso aos próprios clientes atribuídos
  - Funcionalidades plenas de planejamento

- **Assistente:**
  - Read-only ou permissões específicas
  - Suporte administrativo

### 12.3 Relatórios Gerenciais

**Métricas de Performance:**
- Clientes ativos por planejador
- Taxa de retenção
- Receita gerada (honorários + Vista Finance)
- NPS por planejador
- Tempo médio de atendimento

**Uso:**
- Avaliação de desempenho
- Identificação de treinamento necessário
- Estratégia de crescimento

### 12.4 White Label

**Personalização Corporativa:**
- **Branding:**
  - Logo do escritório em toda interface
  - Cores corporativas
  - Nome da empresa

- **Domínio:**
  - Opcional: app.nomeescritorio.com.br

- **Relatórios:**
  - Marca do escritório em diagnósticos e relatórios
  - Remoção de menções ao Meu Vista (opcional)

**Posicionamento Premium:**
- Escritório apresenta solução como própria
- Fortalecimento de marca
- Diferenciação competitiva

---

## 13. FUNCIONALIDADES MOBILE (APP CLIENTE)

### 13.1 Interface Mobile-First

**Design Responsivo:**
- Otimizado para smartphones
- UX intuitiva para não-especialistas
- Navegação por abas/menu inferior

### 13.2 Funcionalidades Core

**Home:**
- Resumo financeiro (saldo, patrimônio)
- Progresso de sonhos (cards visuais)
- Notificações e alertas

**Despesas:**
- Adicionar despesa rapidamente
- Foto de nota fiscal
- Categorização
- Histórico de gastos

**Extratos:**
- Todas as transações
- Filtros por período e categoria
- Busca

**Investimentos:**
- Visualização de carteira
- Rentabilidade
- Distribuição

**Sonhos:**
- Acompanhamento de progresso
- Detalhes de cada meta

**Perfil:**
- Dados pessoais
- Configurações de notificação
- Ajuda e suporte

**Mensagens:**
- Chat com planejador
- Histórico de conversas

**Documentos:**
- Acesso a diagnósticos
- Atas de reunião
- Relatórios compartilhados

### 13.3 Notificações Push

**Tipos:**
- Vencimento de contas
- Alerta de estouro de orçamento
- Progresso de sonho (marcos atingidos)
- Mensagem do planejador
- Atualização de investimentos
- Lembrete de reunião agendada

**Configuração:**
- Cliente pode ativar/desativar por tipo
- Frequência personalizável

### 13.4 Gamificação

**Elementos:**
- Badges de conquista (ex: "Primeiro mês no orçamento", "Reserva de emergência completa")
- Streaks (dias consecutivos registrando despesas)
- Progresso visual (barras, níveis)

**Objetivo:**
- Engajamento do cliente
- Reforço de comportamentos positivos
- Diversão no processo de organização financeira

---

## 14. INTEGRAÇÕES TÉCNICAS

### 14.1 APIs e Serviços Integrados

**Open Finance (via Pluggy):**
- Bancos e corretoras brasileiras
- Contas, cartões, investimentos, empréstimos
- Sincronização automática

**Kinvo API:**
- Consolidação de investimentos
- Cotações em tempo real
- Proventos e rendimentos

**CEI (B3):**
- Posição de ações e fundos imobiliários
- Custódia de ativos de renda variável

**Instituições Específicas (Beta/Parcial):**
- XP Investimentos
- Órama
- BTG Pactual
- Outros em expansão

**Criptomoedas:**
- Mercado Bitcoin
- Foxbit
- Bitcoin Trade

### 14.2 Exportação de Dados

**Formatos Disponíveis:**
- **Excel/CSV:**
  - Extratos de transações
  - Posição de investimentos
  - Orçamento planejado vs. realizado

- **PDF:**
  - Todos os relatórios
  - Diagnóstico financeiro
  - Atas de reunião

- **API (Futuro):**
  - Integração com sistemas de terceiros
  - Desenvolvimento de extensões

### 14.3 Segurança de Integrações

**Protocolos:**
- OAuth 2.0 para autenticação Open Finance
- SSL/TLS para todas as comunicações
- Criptografia de dados em repouso
- Tokenização de credenciais

**Gestão de Consentimentos:**
- Usuário tem controle total
- Renovação periódica obrigatória (90 dias típico)
- Revogação instantânea

---

## 15. AUTOMAÇÕES E INTELIGÊNCIA

### 15.1 Categorização Automática

**Machine Learning:**
- Algoritmo aprende padrões de categorização do usuário
- Sugestões automáticas para novas transações
- Acurácia melhora com uso

**Exemplos:**
- "Posto ABC" → sempre categoriza como Transporte
- "Supermercado XYZ" → Alimentação
- "Netflix" → Entretenimento

### 15.2 Alertas Inteligentes

**Tipos:**
- **Orçamento:**
  - Aproximação de limite de categoria
  - Gasto atípico detectado

- **Investimentos:**
  - Oportunidade de rebalanceamento
  - Ativo com performance muito abaixo do esperado
  - Vencimento próximo

- **Dívidas:**
  - Oportunidade de portabilidade (taxa menor disponível)
  - Risco de atraso

- **Sonhos:**
  - Meta em risco de não ser atingida no prazo
  - Oportunidade de antecipação

### 15.3 Recomendações Automáticas

**Engine de Sugestões:**
- Baseado em dados do cliente e benchmarks
- Sugestões de ajuste de orçamento
- Recomendações de investimento (genéricas, não específicas)
- Priorização de objetivos

**Exemplo:**
- Sistema identifica gasto alto em categoria "Restaurantes"
- Calcula economia potencial reduzindo 30%
- Mostra impacto: "Economizando R$ 300/mês, você antecipa sua viagem em 4 meses"

### 15.4 Análise Preditiva (Futuro/Em Desenvolvimento)

**Funcionalidades Potenciais:**
- Previsão de despesas futuras com alta precisão
- Identificação de riscos financeiros antes de ocorrerem
- Simulações de cenários (e se perder emprego, e se ter filho, etc.)
- Otimização automática de carteira de investimentos

---

## 16. EDUCAÇÃO E CONTEÚDO

### 16.1 Jornada do Planejador (Treinamento)

**Incluído nos Planos:**
- Ignição: Acesso ao curso Jornada do Planejador
- Business: Idem + treinamentos avançados

**Conteúdo:**
- Metodologia de atendimento
- Uso da plataforma (tutoriais)
- Técnicas de vendas e retenção
- Educação financeira avançada
- Compliance e regulação

**Formato:**
- Vídeo-aulas
- Materiais de apoio (PDFs, planilhas)
- Exercícios práticos
- Certificado de conclusão

### 16.2 Clube Meu Vista (Comunidade)

**Acesso:**
- Incluído em planos Ignição e Business
- Ou assinatura standalone

**Recursos:**
- Fórum de discussão
- Grupos de WhatsApp/Telegram
- Eventos online (webinars, lives)
- Eventos presenciais (encontros regionais)
- Networking entre planejadores

**Benefícios:**
- Troca de experiências
- Resolução colaborativa de problemas
- Parcerias comerciais
- Suporte peer-to-peer
- Atualizações de mercado

### 16.3 Materiais Educativos para Clientes

**Biblioteca de Conteúdo:**
- Artigos sobre educação financeira
- Vídeos explicativos
- Infográficos
- E-books

**Personalização:**
- Planejador pode compartilhar conteúdos relevantes com clientes específicos
- Recomendações baseadas em perfil (iniciante, intermediário, avançado)

**Temas:**
- Orçamento doméstico
- Como investir
- Planejamento de aposentadoria
- Educação financeira para filhos
- Finanças comportamentais

---

## 17. SUPORTE E ATENDIMENTO

### 17.1 Canais de Suporte

**Para Planejadores:**
- **Email:** suporte@meuvista.com
- **Chat:** Integrado na plataforma web
- **WhatsApp:** Suporte comercial e técnico
- **Base de Conhecimento:** FAQs, tutoriais, videos

**Horário:**
- Segunda a sexta, 9h-12h e 14h-18h (horário comercial)
- Resposta em até 48 horas

**Para Clientes Finais:**
- Suporte via planejador (primeiro nível)
- Ajuda direta em caso de problemas técnicos com app

### 17.2 Onboarding

**Para Plano Ignição:**
- Onboarding automático (self-service)
- Tutoriais em vídeo
- Checklist de configuração
- Suporte via chat/email

**Para Plano Business:**
- Onboarding personalizado
- Sessão de 1-2 horas com especialista
- Configuração assistida
- Treinamento customizado

**Para Plano Escalada:**
- Onboarding completo enterprise
- Integração com sistemas existentes (se aplicável)
- Treinamento de equipe
- Suporte dedicado durante implementação

### 17.3 Atualizações e Roadmap

**Transparência:**
- Changelog público de atualizações
- Anúncios de novas funcionalidades
- Roadmap compartilhado (próximos desenvolvimentos)

**Feedback:**
- Canal para sugestões de melhoria
- Votação de features mais desejadas
- Co-criação com comunidade

---

## 18. COMPLIANCE E SEGURANÇA

### 18.1 Adequação Regulatória

**CVM Instrução 593:**
- Planejadores devem seguir normas de planejamento financeiro
- Plataforma não substitui responsabilidade do profissional
- Materiais de apoio para compliance

**ANBIMA:**
- Código de regulação e melhores práticas
- Recomendações de conduta

**LGPD (Lei Geral de Proteção de Dados):**
- Consentimento explícito para coleta de dados
- Direito de acesso, correção e exclusão
- Portabilidade de dados
- Privacidade by design

**GDPR (para usuários EU):**
- Conformidade para brasileiros residentes na Europa

### 18.2 Segurança de Dados

**Medidas Implementadas:**
- **Criptografia:**
  - SSL/TLS para transmissão
  - Dados identificáveis armazenados criptografados

- **Infraestrutura:**
  - Servidores certificados de alta segurança
  - Backup redundante
  - Disaster recovery plan

- **Acesso:**
  - Autenticação forte (senha + 2FA opcional)
  - Controle de permissões granular
  - Logs de auditoria

- **Monitoramento:**
  - Detecção de anomalias
  - Resposta a incidentes
  - Testes de penetração periódicos

### 18.3 Responsabilidade Legal

**Disclaimer:**
- Plataforma é ferramenta de gestão, não presta aconselhamento
- Planejador é responsável por análises e recomendações
- Meu Vista não se responsabiliza por resultados financeiros dos clientes finais

**Termos de Uso:**
- Aceite obrigatório no cadastro
- Definição clara de responsabilidades
- Limitações de garantia e responsabilidade

---

## 19. PERFORMANCE E ESCALABILIDADE

### 19.1 Performance da Plataforma

**Métricas:**
- Tempo de carregamento de dashboard: < 2 segundos
- Geração de diagnóstico: < 10 segundos
- Sincronização de contas: executada em background (não bloqueia uso)

**Otimizações:**
- Lazy loading de dados
- Cache inteligente
- CDN para assets estáticos
- Consultas otimizadas ao banco de dados

### 19.2 Escalabilidade

**Arquitetura:**
- Cloud-based (escalabilidade horizontal)
- Microserviços (componentes independentes)
- Balanceamento de carga
- Auto-scaling baseado em demanda

**Capacidade:**
- Suporte a milhares de planejadores simultâneos
- Dezenas de milhares de clientes finais
- Milhões de transações processadas

### 19.3 Disponibilidade

**SLA (Não Formal, Mas Objetivo):**
- Uptime: > 99% (menos de 7 horas de downtime por mês)
- Janelas de manutenção programadas (notificação prévia)

**Resiliência:**
- Redundância de servidores
- Failover automático
- Backup contínuo

---

## 20. ROADMAP E FUTURO

### 20.1 Funcionalidades em Desenvolvimento (Inferidas)

**Inteligência Artificial Avançada:**
- Chatbot para clientes (FAQs automatizadas)
- Assistente virtual para planejadores (sugestões em tempo real)
- Análise preditiva de riscos

**Expansão de Integrações:**
- Mais bancos e corretoras
- Integração com marketplaces (Mercado Livre, Amazon - rastreamento de gastos)
- Pagamentos via PIX (iniciação de pagamento)

**Novas Verticais:**
- Planejamento sucessório e herança
- Planejamento tributário (otimização de IR)
- Seguros (marketplace)

**Internacionalização:**
- Adaptação para outros países da América Latina
- Suporte a múltiplas moedas
- Idiomas (inglês, espanhol)

**API Pública:**
- Desenvolvedores externos criando extensões
- Ecossistema de apps integrados
- Marketplace de plugins

### 20.2 Melhorias Contínuas

**UX/UI:**
- Redesign periódico baseado em feedback
- Testes A/B de interfaces
- Accessibility (acessibilidade para PCD)

**Performance:**
- Otimizações contínuas
- Novos algoritmos de processamento
- Edge computing

**Conteúdo:**
- Biblioteca educativa expandida
- Cursos avançados
- Certificações especializadas

---

## 21. COMPARATIVO DE FUNCIONALIDADES POR PLANO

| Funcionalidade | Ignição | Business | Escalada |
|---------------|---------|----------|----------|
| **Plataforma Web** | ✅ | ✅ | ✅ |
| **App Mobile Cliente** | ✅ | ✅ | ✅ |
| **Open Finance** | ✅ | ✅ | ✅ |
| **Consolidação Investimentos (Kinvo)** | ✅ | ✅ | ✅ |
| **Orçamento e Fluxo de Caixa** | ✅ | ✅ | ✅ |
| **Gestão de Patrimônio** | ✅ | ✅ | ✅ |
| **Sonhos e Metas** | ✅ | ✅ | ✅ |
| **Gestão de Dívidas** | ✅ | ✅ | ✅ |
| **Diagnóstico Financeiro (1 clique)** | ✅ | ✅ | ✅ |
| **Relatórios Automatizados** | ✅ | ✅ | ✅ |
| **Vista Finance (Acesso)** | ✅ Grátis | ✅ Grátis | ✅ Grátis |
| **Jornada do Planejador (Curso)** | ✅ Incluído | ✅ Incluído | ✅ Incluído |
| **Clube Meu Vista (Comunidade)** | ✅ | ✅ | ✅ |
| **Suporte Técnico** | Chat/Email | Chat/Email | Dedicado |
| **Onboarding** | Self-service | Personalizado | Enterprise |
| **Número de Clientes** | Até 10 | Ilimitado | Ilimitado |
| **Cobrança Adicional** | Não | R$ 59,90/cliente > 10 | Customizado |
| **Vista Gestores (Multi-planejador)** | ❌ | ✅ | ✅ |
| **White Label** | ❌ | ✅ (Opcional) | ✅ Incluído |
| **Permissões Granulares** | ❌ | ✅ | ✅ |
| **Relatórios Gerenciais** | ❌ | Básico | Avançado |
| **API Acesso (Futuro)** | ❌ | Limitado | Completo |
| **SLA Garantido** | ❌ | ❌ | ✅ |
| **Treinamento In-company** | ❌ | ❌ | ✅ Opcional |

---

## 22. CASOS DE USO PRÁTICOS

### 22.1 Caso 1: Planejador Iniciante

**Persona:** João, 28 anos, ex-gerente de banco, quer ser planejador independente

**Jornada na Plataforma:**
1. Compra curso Origem 2.0 (R$ 49)
2. Aprende fundamentos
3. Contrata Plano Ignição (R$ 229/mês)
4. Faz curso Jornada do Planejador (incluído)
5. Cadastra primeiro cliente (amigo/familiar)
6. Conecta contas via Open Finance
7. Cria orçamento básico
8. Gera primeiro diagnóstico financeiro
9. Apresenta para cliente (impressionado com profissionalismo)
10. Cliente contrata serviço
11. João adiciona mais clientes (até 10)
12. Usa Vista Finance para gerar comissões adicionais
13. Participa do Clube Meu Vista para networking
14. Cresce para 15 clientes em 6 meses
15. Upgrade para Plano Business

**Valor Gerado:**
- Receita com honorários: 10 clientes x R$ 200/mês = R$ 2.000/mês
- Comissões Vista Finance: ~R$ 500/mês
- Total: R$ 2.500/mês
- Custo Meu Vista: R$ 229/mês
- Lucro líquido: R$ 2.271/mês (10x o investimento)

### 22.2 Caso 2: Escritório de Contabilidade Expandindo Serviços

**Persona:** Escritório Contábil ABC, 50 clientes B2B, quer adicionar planejamento financeiro pessoal

**Jornada na Plataforma:**
1. Contrata Programa FPBP (integração para escritórios)
2. Treina 2 contadores no método Vista
3. Contrata Plano Escalada
4. Configura white label com marca do escritório
5. Oferece planejamento financeiro como serviço adicional aos clientes
6. 30% dos clientes aderem (15 famílias)
7. Usa Vista Gestor para distribuir clientes entre os 2 planejadores
8. Gera receita adicional mantendo clientes atuais
9. Diferenciação competitiva no mercado contábil

**Valor Gerado:**
- Receita adicional: 15 famílias x R$ 300/mês = R$ 4.500/mês
- Custo Meu Vista Escalada: ~R$ 1.500-2.000/mês (estimado)
- Lucro adicional: ~R$ 2.500-3.000/mês
- Bonus: Retenção de clientes contábeis aumenta

### 22.3 Caso 3: Cliente Final Usando App

**Persona:** Maria, 35 anos, publicitária, cliente de planejador

**Jornada no App:**
1. Recebe credenciais do planejador via email
2. Baixa app Meu Vista
3. Faz login
4. Vê dashboard com resumo financeiro (dados já importados pelo planejador na reunião)
5. Explora seus 3 sonhos cadastrados:
   - Viagem Europa (2 anos): 45% concluído
   - Entrada apartamento (5 anos): 20% concluído
   - Aposentadoria (30 anos): 8% concluído
6. Adiciona despesa do almoço: R$ 45 em "Restaurantes"
7. App alerta: "Você já gastou 78% do orçamento de Restaurantes este mês"
8. Maria se conscientiza e decide cozinhar mais
9. Fim do mês: Recebe notificação "Parabéns! Você economizou R$ 200 este mês"
10. Visualiza que economizar R$ 200/mês antecipa viagem para Europa em 3 meses
11. Motivada, mantém disciplina
12. Próxima reunião com planejador: Discute realocação de investimentos baseada em relatório do app

**Valor Percebido:**
- Consciência financeira aumentada
- Motivação visual (sonhos com progresso)
- Autonomia (não depende só de reuniões com planejador)
- Resultados tangíveis (economias reais)

---

## 23. DIFERENCIAIS COMPETITIVOS (FEATURES)

### 23.1 Único no Mercado

1. **Ecossistema Completo:**
   - Nenhum concorrente oferece tech + educação + comunidade + suporte no mesmo pacote

2. **Open Finance Nativo:**
   - Integração profunda com Open Finance brasileiro desde o início

3. **Modelo de Precificação Alinhado:**
   - Cobrança por cliente ativo (não por usuário ou flat fee)
   - Planejador só paga quando tem clientes

4. **App Mobile para Cliente Final:**
   - Maioria dos concorrentes B2B não oferece interface para end-user

5. **Vinculação Investimentos → Sonhos:**
   - Feature psicologicamente poderosa, rara no mercado

### 23.2 Melhor que Concorrentes

1. **Diagnóstico em 1 Clique:**
   - Geração instantânea vs. horas de trabalho manual

2. **Sincronização Automática:**
   - Reduz trabalho manual de atualização de dados

3. **Visual e Intuitivo:**
   - Design profissional vs. interfaces antigas e complexas

4. **Comunidade Ativa:**
   - Network de 1.000+ planejadores vs. isolamento

5. **Vista Finance Integrado:**
   - Monetização adicional built-in

---

## 24. LIMITAÇÕES E GAPS (OPORTUNIDADES)

### 24.1 Limitações Identificadas

1. **Sem Planejamento Tributário Avançado:**
   - Não há módulo específico para otimização de IR pessoa física/jurídica

2. **Sem Planejamento Sucessório:**
   - Herança, inventário, holding familiar não são cobertos

3. **Seguros Básicos:**
   - Gestão de seguros é mencionada mas não parece robusta

4. **Integrações Internacionais:**
   - Focado apenas em Brasil, sem suporte a ativos offshore

5. **Análise de Crédito:**
   - Não há score de crédito ou análise de elegibilidade

6. **Automação de Rebalanceamento:**
   - Sugestões sim, execução automática não

### 24.2 Oportunidades de Melhoria

1. **Marketplace de Serviços:**
   - Conectar clientes com advogados, contadores, corretores especializados

2. **Gamificação Mais Profunda:**
   - Desafios, leaderboards, recompensas

3. **Social Features:**
   - Comunidade de clientes (não só planejadores)
   - Grupos de objetivos similares (ex: "Comprando primeiro imóvel em 2025")

4. **Análise Comportamental:**
   - Insights psicológicos sobre padrões de gasto

5. **Integração com Contabilidade:**
   - Para empreendedores, unir PF e PJ

---

## 25. CONCLUSÃO

### 25.1 Resumo Executivo de Features

A plataforma Meu Vista oferece um conjunto completo e integrado de funcionalidades que cobrem todo o ciclo de vida do planejamento financeiro pessoal:

- **Consolidação de Dados:** Open Finance, Kinvo, múltiplas fontes
- **Análise:** Orçamento, patrimônio, dívidas, investimentos
- **Planejamento:** Sonhos, metas, aposentadoria
- **Execução:** Vista Finance, gestão de clientes, relatórios
- **Colaboração:** App cliente, comunicação, educação
- **Gestão:** Vista Gestor, white label, multi-planejador

### 25.2 Proposta de Valor em Features

**Para Planejadores:**
"Tudo o que você precisa para atender clientes com excelência, em uma única plataforma"

**Para Clientes:**
"Sua vida financeira completa, clara e na palma da mão"

### 25.3 Próximos Passos para Análise

Este documento deve ser complementado com:
1. **Análise técnica profunda** (arquitetura de dados, APIs, stack)
2. **Análise de UX detalhada** (fluxos de tela a tela)
3. **Benchmarking competitivo** (feature-by-feature vs. concorrentes)

---

**Documento compilado em:** 04/11/2025
**Versão:** 1.0
**Base:** Análise do website Meu Vista e inferências técnicas
