# Gestão PPC e Force-Directed Graph

### Projeto: Casa Estoril
Dashboard analítico 3D para monitoramento de performance de equipes de construção civil.

## 🛠️ Tecnologias
- **Engine:** Three.js / 3D-Force-Graph
- **Data Source:** Google Sheets API (CSV)
- **Metodologia:** Lean Construction (PPC)

## 📊 Funcionalidades
- Visualização de interdependências em tempo real.
- Filtros por equipe (Cofragem, Ferros, Elétrica).
- Simulação de impacto de produtividade e retrabalho.

Este repositório contém o sistema PPC Boundless Vision, uma ferramenta de análise 3D para a obra Casa Estoril.
Desenvolvido por Tulio Cunha , Gestor de projetos da Boundless Vision construtora do projeto Casa Estoril.
Pesquida bibliografia de boas práticas de gestão da qualidade em canteiros de obras para elaboração conceital.
Desenvolvido o código html com suporte das ferramnentas de Ai Perplexity e Gemini.
21 versões e aperfeiçoamentos do código html foram realizadas nesta inicialização.

Próximo passo é publicar uma planilha no Google Sheets como CSV e colar os links no código acima.
IMPORTANTE: substituir os links URL_PLANILHA_PROFISSIONAIS e URL_PLANILHA_CONEXOES pelos links CSV gerados no seu Google Sheets (Arquivo > Compartilhar > Publicar na Web > Escolher aba > Formato .csv).

Para que o código funcione perfeitamente, o ideal é que você utilize um único arquivo de planilha (Google Sheets), mas com duas abas (páginas) diferentes dentro dela.
Isso mantém os dados organizados e fáceis de gerenciar.
Aqui estão os campos exatos que você deve criar em cada aba:
Aba 1: Nome da aba= "Profissionais. Esta aba contém as informações de cada pessoa (os "nós" do gráfico)
Coluna                  Descrição                                          Exemplo de Preenchimento 
Coluna 1 ="ID"          Número único para cada pessoa (obrigatório).       Ex: 1, 2, 3...
Coluna 2 = "Nome"       nome do oficial ou ajudante,                       Ex: Francisco, Ibrahim, Samu
COLUNA 3 = "Equipe      ou Grupo de trabalho" (em letras minúsculas),      Ex: cofragem, ferros, eletrica, apoio
Coluna 4 = "Função"     Cargo ocupado.                                     Ex: Oficial, Ajudante, Encarregado
Coluna 5 = "PPC (%)"    Produtividade (0 a 100)".                          Ex: 85
Coluna 6 = "Retrabalho(%)"Taxa de erro (0 a 50).                           Ex= 5
Coluna 7 = "Observação" Notas sobre o desempenho ou incidentes,            Ex: "Evoluindo bem", "Atenção necessária"

Aba 2: Nome da aba: "Conexoes". Esta aba define as linhas que ligam as pessoas (quem responde a quem).
Campo (Cabeçalho)        Descrição                           Exemplo de Preenchimento
Origem (ID)              O ID do superior ou oficial         1 (ID do Encarregado)
Destino (ID)             O ID do subordinado ou ajudante     7 (ID do Samu)
Tipo                     Descrição da relação (opcional)     Supervisão, Ajuda, Comando
