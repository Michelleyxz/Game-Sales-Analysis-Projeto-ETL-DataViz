# Game Market ETL — Pipeline de Análise do Mercado de Games

> Projeto ETL (Extract — Transform — Load) simples e didático para análise de vendas de jogos.  
> Feito para o desafio da DIO / Santander Codegirls — pensado para rodar no Google Colab.


Visão geral
Este projeto demonstra um pipeline ETL com:
- Extração: dataset de vendas de jogos (CSV ou dataset embutido no notebook).
- Transformação: limpeza, padronização e criação de features.
- Load / Visualização: gráficos, top 10 jogos e arquivos processados.

O objetivo é ser um projeto de portfólio — fácil de executar e explicar em entrevistas.

---

Como rodar (Google Colab — recomendado)
1. Abra o Google Colab (https://colab.research.google.com).  
2. Clique em File → Upload notebook e envie `01_Extracao.ipynb` (ou abra direto do GitHub).  
3. Rode as células na ordem: `01_Extracao` → `02_Transformacao` → `03_Load_Visualizacao`.

 Executando sem enviar arquivo
- Os notebooks têm uma célula inicial que permite:
  - Fazer upload do `vgsales.csv` (se tiver), ou
  - Usar um dataset de exemplo interno (se preferir não subir arquivo).
- Se usar dataset externo: carregue via `files.upload()` no Colab.


Scripts / Notebooks principais
- 01_Extracao.ipynb — carrega dados e inspeciona (head, info, nulos).
- 02_Transformacao.ipynb — limpeza, padronização de colunas, tratamento de anos, criação de `global_hit`.
- 03_Load_Visualizacao.ipynb — gera gráficos (vendas por gênero, top10, vendas por plataforma) e salva `games_clean.csv`.

 Requisitos (local)
Se quiser rodar localmente:
```bash
python3 -m venv venv
source venv/bin/activate   # mac/linux
# venv\Scripts\activate     # windows
pip install -r requirements.txt
jupyter lab

git init
git add .
git commit -m "feat: projeto ETL Game Market"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/NOME_DO_REPO.git
git push -u origin main


Qual prefere agora? Quer que eu gere os notebooks automaticamente aqui para você baixar?

