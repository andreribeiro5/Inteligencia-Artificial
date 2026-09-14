# Planeamento de Rotas de Entrega — Inteligência Artificial

> Resolução de um problema de **entrega de mantimentos** modelado como um **grafo de municípios**, resolvido com vários **algoritmos de procura** (informada e não informada). Desenvolvido no âmbito da unidade curricular de **Inteligência Artificial** da Licenciatura em Engenharia Informática da Universidade do Minho.

---

## 📋 Sobre o projeto

O sistema modela a distribuição de mantimentos a partir de um ponto central (**"Centro"**) para um conjunto de municípios do distrito de Braga, cada um com atributos próprios (prioridade, acessibilidade, condições climatéricas, necessidade de alimentos, tempo-de-vida/TTL e coordenadas geográficas).

O objetivo é encontrar rotas de entrega, dando prioridade aos locais com maior necessidade, tendo em conta diferentes **meios de transporte** e as suas restrições. São aplicados e **comparados vários algoritmos de procura** quanto ao caminho encontrado, custo e tempo.

> **Projeto académico de grupo.** Ver a secção [Contribuição](#-contribuição) para o detalhe do trabalho individual.

## ✨ Abordagem

- Modelação do problema como um **grafo** de municípios com atributos dinâmicos (prioridade, acessibilidade, clima, TTL, coordenadas).
- **Meios de transporte** com características distintas — **Carro, Mota, Helicóptero e Drone** — cada um com capacidade, velocidade, autonomia e reabastecimento próprios.
- Seleção do transporte em função da acessibilidade e das condições de cada local.
- Ordenação dos destinos por **prioridade** de necessidade.
- Registo dos resultados de cada algoritmo em ficheiros `Resultados_<algoritmo>.txt` (caminho, custo e tempo).

## 🔎 Algoritmos de procura

- **Não informada:** BFS, DFS e Custo Uniforme
- **Informada:** Greedy e **A\*** (com heurística baseada na distância entre coordenadas)

## 🛠️ Stack técnica

- **Python**
- Estruturas de dados para grafos
- Algoritmos de procura em espaço de estados

## 📁 Estrutura do repositório

```
.
├── main.py           # ponto de entrada: constrói o grafo e corre os algoritmos
├── grafo.py          # estrutura do grafo e algoritmos de procura
├── transporte.py     # meios de transporte (Carro, Mota, Helicóptero, Drone)
└── README.md
```

## 🚀 Como executar

Pré-requisito: **Python 3**.

```bash
python main.py
```

Os resultados de cada algoritmo são gravados em ficheiros `Resultados_<algoritmo>.txt` na raiz do projeto (caminho, custo total e tempo estimado).

## 👥 Contribuição

Este é um trabalho académico realizado em grupo. A minha contribuição centrou-se em:

- Modelação do grafo e dos atributos dos municípios
- Implementação de alguns dos algoritmos de procura 
- Meios de transporte e respetivas restrições (capacidade, autonomia, reabastecimento)
- Análise e comparação dos resultados dos algoritmos
