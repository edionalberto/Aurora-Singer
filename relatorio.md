# 🚀 Aurora-Singer: Sistema de Telemetria e Verificação de Decolagem

**Projeto Integrador FIAP** | Curso de Ciência da Computação Aplicada  
**Autor**: Edion  
**Data**: Março de 2026  
**Repositório**: https://github.com/edionalberto/Aurora-Singer

---

## 📋 Descrição do Projeto

**Aurora-Singer** é um sistema completo de telemetria e verificação de segurança para um veículo espacial hipotético. O projeto implementa:

1. **Monitoramento de Telemetria**: Captura e organização de 6 parâmetros críticos de uma nave espacial
2. **Algoritmo de Verificação de Decolagem**: Sistema automático que decide se é seguro decolar com base em faixas predefinidas
3. **Análise de Autonomia Energética**: Cálculo de tempo de voo baseado em capacidade de bateria e consumo
4. **Detecção de Anomalias com IA**: Classificação inteligente de dados e identificação de riscos
5. **Reflexão Crítica**: Discussão sobre ética, responsabilidade social e sustentabilidade da exploração espacial

### Parâmetros Monitorados

| Parâmetro | Unidade | Faixa Segura | Status |
|-----------|---------|--------------|--------|
| Temperatura Interna | °C | 15-35 | ⚠️ Crítica |
| Temperatura Externa | °C | -50 a 50 | ⚠️ Crítica |
| Integridade Estrutural | (0/1) | 1 (Íntegro) | 🔴 Crítica |
| Nível de Energia | % | ≥ 85 | 🔴 Crítica |
| Pressão dos Tanques | psi | 1800-2200 | ⚠️ Alta |
| Status dos Módulos | Status | OPERACIONAL | 🔴 Crítica |

---

## 📂 Estrutura do Projeto

Arquivos principais:

- `README.md` - documentação resumida e instruções de execução
- `relatorio.md` - relatório de avaliação com análise crítica
- `relatorio.ipynb` - notebook completo com código e resultados
- `aurora_singer.py` - script executável de simulação de decolagem
- `telemetria_sintetica.csv` - dados de telemetria sintéticos de teste
- `requirements.txt` - dependências Python
- `relatorio.html` - versão gerada em HTML do notebook
- `.gitignore` - itens ignorados no versionamento


---

## 🛠️ Pré-requisitos

**Sistema Operacional**: Windows, macOS ou Linux  
**Python**: 3.7 ou superior  
**Gerenciador de Pacotes**: pip ou conda

### Dependências Python

```
pandas >= 1.0.0
numpy >= 1.18.0
jupyter >= 1.0.0
scikit-learn >= 0.24.0
```

---

## 💻 Instruções de Execução

### Opção 1: Usando Jupyter Notebook (Recomendado)

#### Passo 0: Preparar Ambiente Virtual (Windows)

Abra o PowerShell na pasta do projeto:

```bash
# Criar ambiente virtual
python -m venv venv

# Ativar ambiente virtual
.\venv\Scripts\Activate
```

#### Passo 1: Instalar Dependências

Com o ambiente virtual ativado, execute:

```bash
pip install --upgrade pip
pip install jupyter pandas numpy scikit-learn
```

**Ou usando requirements.txt (recomendado para reprodutibilidade):**

```bash
pip install -r requirements.txt
```

#### Passo 2: Iniciar Jupyter

Com o ambiente virtual ativado, execute:

```bash
jupyter notebook
```

Isso abrirá uma nova aba no seu navegador padrão.

#### Passo 3: Abrir o Arquivo

Navegue até a pasta do projeto e clique em `relatorio.ipynb`

#### Passo 4: Executar as Células

- Clique em uma célula
- Pressione `Shift + Enter` para executar
- Ou use o botão **▶ Run** na barra superior
- Para executar todas as células: **Cell > Run All**

### Opção 2: Usando VS Code com Extensão Python

1. Abra VS Code
2. Instale a extensão "Jupyter" de Microsoft
3. Abra `relatorio.ipynb`
4. Clique em **"Run All"** para executar todas as células
5. Ou execute célula por célula pressionando ▶

### Opção 3: Script Direto em Python

Para executar apenas o script `aurora_singer.py`:

```bash
# Com ambiente virtual ativado
python aurora_singer.py
```

Isso executará uma simulação completa sem precisar de Jupyter.

### Opção 4: Usar Google Colab (Online, sem instalação)

1. Vá para https://colab.research.google.com
2. Selecione **Upload** e envie `relatorio.ipynb`
3. Execute as células normalmente
4. ⚠️ **Nota**: Pode ser necessário instalar scikit-learn se não estiver disponível

---

## 📊 Exemplo de Execução Real

### Output do Script `aurora_singer.py` (31/03/2026)

```
=== RELATÓRIO DE PRÉ-DECOLAGEM ===
timestamp: 2026-03-18T00:25:00
temperatura_interna: 27.93
temperatura_externa: 12.6
tensao_bateria: 51.12
corrente_bateria: 35.74
nivel_energia: 98.43
capacidade_bateria_ah: 83.2
energia_disponivel_kwh: 4.186
carga_kw: 8.72
perdas_energeticas: 5.57
pressao_tanques: 128.76
integridade_estrutural: 1
status_modulos_criticos: 1
status_link_telemetria: 1
autonomia_estimada_dataset_min: 45
decisao_dataset: READY

Resultado final: PRONTO PARA DECOLAR
Nível de risco estimado pela IA: RISCO_BAIXO
IA: nenhuma anomalia detectada.

=== ANÁLISE ENERGÉTICA ===
Energia disponível antes das perdas: 4.186 kWh
Energia útil após perdas: 3.953 kWh
Consumo estimado da decolagem (1 min): 0.145 kWh
Energia restante após decolagem: 3.808 kWh
Autonomia estimada após perdas: 27.20 min
Autonomia registrada no dataset: 45 min
```

### Análise do Output:

✅ **Sistema STATUS: OPERACIONAL**
- Decisão: PRONTO PARA DECOLAR
- Risco IA: BAIXO
- Anomalias: NENHUMA

📊 **Parâmetros Validados:**
- Temperatura interna: 27.93°C (faixa 20-32°C) ✅
- Temperatura externa: 12.6°C (faixa 0-28°C) ✅
- Tensão bateria: 51.12V (faixa 47-51.5V) ✅
- Corrente: 35.74A (faixa 25-100A) ✅
- Energia: 98.43% (≥70%) ✅
- Pressão: 128.76 bar (faixa 100-140 bar) ✅
- Integridade: OK ✅
- Módulos críticos: OK ✅
- Link telemetria: OK ✅
- Perdas: 5.57% (≤7%) ✅

⚡ **Análise Energética:**
- Energia útil: 3.953 kWh (após 5.57% perdas)
- Autonomia: 27.20 minutos
- Energia pós-decolagem: 3.808 kWh

---

## 🤖 Análise de IA

O sistema de análise inteligente fornece:

- **Classificação de Parâmetros**: NORMAL, PRECAUÇÃO ou CRÍTICO
- **Detecção de Anomalias**: Identificação automática de comportamentos anormais
- **Análise de Risco**: Score de 0-10 indicando nível de risco geral
- **Recomendações**: Sugestões acionáveis baseadas no estado do sistema

**Exemplo de Saída:**

```
📊 CLASSIFICAÇÃO DE PARÂMETROS:
   ✅ Temperatura Interna: NORMAL
   ✅ Energia: NORMAL
   ✅ Pressao: NORMAL
   ✅ Modulos: NORMAL

🔍 ANOMALIAS DETECTADAS:
   ✅ Nenhuma anomalia detectada

📈 ANÁLISE DE RISCO:
   Nível de Risco Total: 1/10 ✅ (Baixo)

💡 RECOMENDAÇÕES:
   ✅ Sistema totalmente operacional. Pronto para missão.
```

---

## 📈 Estatísticas do Projeto

| Métrica | Valor |
|---------|-------|
| Linhas de Código | ~400 |
| Classes Implementadas | 3 |
| Cenários de Teste | 5 |
| Parâmetros Monitorados | 6 |
| Pontos de Verificação | 6 |

---

## 🔍 Estrutura do Notebook

| Seção | Descrição |
|-------|-----------|
| **1.1** | Organização e descrição da telemetria |
| **1.2** | Algoritmo de verificação (pseudocódigo + fluxograma) |
| **1.3** | Implementação em Python com 3 cenários de teste |
| **1.4** | Análise energética com 2 simulações |
| **1.5** | Análise de IA com 2 cenários (normal e anômalo) |
| **1.6** | Reflexão crítica: ética, impacto social e sustentabilidade |

---

## 💡 Conceitos Implementados

### Algoritmo de Decisão (Verificação de Decolagem)

O sistema implementa uma série de verificações em cascata:

```
1. ✓ Integridade Estrutural
   └─→ 2. ✓ Módulos Críticos
       └─→ 3. ✓ Nível de Energia
           └─→ 4. ✓ Temperatura Interna
               └─→ 5. ✓ Temperatura Externa
                   └─→ 6. ✓ Pressão dos Tanques
                       └─→ ✅ PRONTO PARA DECOLAR ou 🔴 ABORTADA
```

### Análise de Autonomia

Calcula tempo de voo considerando:
- Capacidade total das baterias (kWh)
- Carga atual (%)
- Consumo instantâneo na decolagem (kW)
- Perdas energéticas por eficiência (5%)

### Detecção Inteligente de Anomalias

Utliza rangos históricos de operação normal para identificar:
- Temperaturas extremas
- Mudanças rápidas de temperatura
- Pressão instável
- Falhas de integridade estrutural

---

### Desativar Ambiente Virtual

Quando terminar, desative o ambiente virtual:

```bash
# Windows
deactivate

# macOS/Linux
deactivate
```

---

## ⚠️ Limitações Conhecidas

1. **Dados Simulados**: O projeto usa dados fictícios para demonstração
2. **Consumo Constante**: Assume consumo linear de energia (real seria variável)
3. **Sem Persistência**: Dados não são salvos entre execuções
4. **Análise Simplificada**: IA usa heurísticas, não machine learning

---

## 🚀 Melhorias Futuras

- [ ] Integração com banco de dados real
- [ ] Gráficos visualizando tendências de parâmetros
- [ ] Exportação de relatórios em PDF
- [ ] Dashboard interativo com streamlit
- [ ] Machine learning para predição de falhas
- [ ] API REST para integração com outros sistemas

---

## 📚 Reflexão Crítica - Pontos-Chave

### Ética e Responsabilidade
A exploração espacial exige rigor técnico absoluto. Falhas em sistemas como Aurora-Singer têm consequências: perda de vidas humanas e recursos.

- Verificação de segurança deve ser transparente. O projeto fortalece a cultura de "segurança em primeiro lugar" testando regras claras de pré-decolagem e atribuindo responsabilidade técnica.
- Em contextos reais, o uso de IA para decisões de risco precisa de explicabilidade (XAI) para engenheiros e mission control entenderem por que uma recomendação é adotada ou rejeitada.
- Atomicidade de decisões: cada leitura deve ser registrada e auditável. Logs de telemetria com carimbo de tempo são fundamentais para análises pós-evento e responsabilização.
- Robustez contra falsos positivos/negativos: um falso negativo (aceitar decolagem insegura) é ameaça de vida; um falso positivo (negar decolagem segura) impacta custo e cronograma. Balancear sensibilidade e especificidade é requisito ético.
- Inclusão de testes de falha e redundância: sistemas críticos precisam simular falhas de sensores e degradação em tempo real, não só condições ideais, para evitar vieses de validação.

### Impacto Social
Enquanto a exploração espacial oferece benefícios (tecnologia, conhecimento), também gera riscos (custo de oportunidade, poluição, militarização).

### Sustentabilidade
É imperativo que a exploração espacial futura seja feita de forma sustentável, com foco em combustíveis limpos, remoção de lixo espacial e responsabilidade ambiental.

---

## 📄 Licença

Este projeto é fornecido como trabalho acadêmico para FIAP.

---

## 👤 Autor

**Edion**  
FIAP - Curso de Ciência da Computação Aplicada  
Março de 2026

---

## 📞 Suporte

Para dúvidas sobre o projeto:
- Verifique a documentação no notebook
- Consulte os comentários no código
- Reexecute as células de teste

**Última Atualização**: Março 31, 2026