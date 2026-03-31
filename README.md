# 🚀 Aurora-Singer

Projeto de verificação de telemetria para decolagem de nave espacial. Analisa condições operacionais, decide status segurança, calcula autonomia e detecta anomalias via IA.

## 📌 Prints da execução

```text
=== RELATÓRIO DE PRÉ-DECOLAGEM ===
... (output do script)
Resultado final: PRONTO PARA DECOLAR
Nível de risco estimado pela IA: RISCO_BAIXO
IA: nenhuma anomalia detectada.
=== ANÁLISE ENERGÉTICA ===
Energia disponível antes das perdas: 4.186 kWh
Energia útil após perdas: 3.953 kWh
Autonomia estimada após perdas: 27.20 min
```

## 💻 Instruções de execução

1. `pip install -r requirements.txt`
2. `python aurora_singer.py`
3. (opcional) `jupyter notebook` e abrir `relatorio.ipynb`

---

## 📊 Exemplo de Execução Real

### Output do Script `aurora_singer.py`

```
=== RELATÓRIO DE PRÉ-DECOLAGEM ===
...
Resultado final: PRONTO PARA DECOLAR
Nível de risco estimado pela IA: RISCO_BAIXO
IA: nenhuma anomalia detectada.
=== ANÁLISE ENERGÉTICA ===
Energia disponível antes das perdas: 4.186 kWh
Energia útil após perdas: 3.953 kWh
Autonomia estimada após perdas: 27.20 min
```

---

## 💻 Instruções de Execução

### Pré-requisitos
- Python 3.7+
- pip

### Instalação

```bash
pip install -r requirements.txt
```

### Executar

```bash
python aurora_singer.py
```

### Notebook (opcional)

```bash
jupyter notebook
```

---

## 📄 Arquivos

- `README.md`
- `aurora_singer.py`
- `relatorio.ipynb`
- `telemetria_sintetica.csv`

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

**Última Atualização**: Março 31, 2026
