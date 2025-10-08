# PowerBI Caseiro — Allanis Lima 🎓💚

Projeto educacional: *Power BI caseiro em Python* — dashboard interativo para explorar uma grande nuvem de palavras
(dataset sintético). Ideal para apresentações, seminários e para inspirar quem pensa em entrar na **FATEC**.

---
## O que tem aqui
- `app/generate_bigdata.py` — Gera a base sintética `data/word_bigdata_sample.csv`.
- `app/word_bi.py` — Dashboard Streamlit para consultar, filtrar e visualizar a base.
- `data/word_bigdata_sample.csv` — pequena amostra (já incluida) para testar rapidamente.
- `requirements.txt` — dependências.
- `.gitignore`, `LICENSE`.

---
## Motivação
Mostrar que **dados + Python + criatividade** viram um dashboard interativo: ótimos argumentos para escolher um curso técnico/tecnológico como a FATEC.
Este projeto foi pensado para jovens que querem ver resultados rápidos e aplicar lógica, estatística e visualização com ferramentas reais.

---
## Quickstart (3 passos)
1. Clone o repositório:
   ```bash
   git clone https://github.com/<seu-usuario>/powerbi-caseiro_allanis.git
   cd powerbi-caseiro_allanis
   ```
2. Crie o ambiente e instale:
   ```bash
   python -m venv venv
   source venv/bin/activate  # Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```
3. Rodar o dashboard:
   ```bash
   python app/generate_bigdata.py  # opcional: gera uma base maior
   streamlit run app/word_bi.py
   ```

---
## Consultas e queries interessantes (exemplos)
- Top palavras por categoria: `SELECT norm, SUM(freq) FROM dataset WHERE pos='noun' GROUP BY norm ORDER BY SUM(freq) DESC LIMIT 50`
- Palavras com sentimento positivo e frequência alta: filtro `sentiment=='positivo' & freq>200`
- Busca fuzzy: tokens que contenham 'tech' ou 'data' (substring)
- Detecção de bigrams frequentes: agrupar `is_bigram==1` por `norm`
- Similaridade (TF-IDF) entre tokens para encontrar termos que aparecem em contextos parecidos

---
## Ideias para apresentação
- Comece com a **nuvem de palavras** (visual e imediato).
- Mostre um filtro "tecnologia" vs "meio ambiente" e compare sentimentos.
- Demonstre uma query ao vivo (digite um termo e veja as linhas de contexto aparecerem).
- Mostre o código gerador para explicar como se sintetiza dados e por que isso é útil.

---
## Autor
Allanis Lima — Projeto educativo para incentivar estudos técnicos e escolha pela FATEC.
