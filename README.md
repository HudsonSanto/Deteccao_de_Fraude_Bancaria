<h1>💳 Detecção de Fraudes em Transações Financeiras</h1>

<p>Este projeto tem como objetivo construir um sistema de <strong>detecção de fraudes</strong> em transações financeiras usando <strong>técnicas de machine learning</strong>, com foco em interpretar e prever transações suspeitas.</p>

<h2>🧠 Modelos Utilizados</h2>

<p>Foram treinados e avaliados diversos algoritmos supervisionados, com foco em problemas de <strong>classificação binária desbalanceada</strong>:</p>

<ul>
  <li>Regressão Logística</li>
  <li>Support Vector Machines (SVM)</li>
  <li>K-Nearest Neighbors (KNN)</li>
  <li>Random Forest</li>
  <li>LightGBM</li>
  <li>XGBoost</li>
</ul>

<h2>📊 Métricas de Avaliação</h2>

<p>Dado o forte desbalanceamento da base (baixa incidência de fraudes), foram utilizadas as seguintes métricas para uma avaliação mais justa:</p>

<ul>
  <li><strong>Acurácia Balanceada</strong></li>
  <li><strong>Precisão</strong></li>
  <li><strong>Revocação (Recall)</strong></li>
  <li><strong>F1-Score</strong></li>
  <li><strong>Coeficiente Kappa</strong></li>
</ul>

<p>O modelo com melhor desempenho foi o <strong>XGBoost</strong>, com destaque para sua revocação (0.858) e F1-Score (0.909), embora o <strong>Random Forest</strong> também tenha apresentado resultados competitivos.</p>

<h2>🔍 Análise Exploratória de Dados</h2>

<p>Foi realizada uma análise exploratória completa com:</p>

<ul>
  <li>Estatísticas descritivas das variáveis numéricas e categóricas</li>
  <li>Verificação de <strong>valores ausentes</strong></li>
  <li>Estudo de <strong>distribuição</strong>, <strong>assimetria</strong>, <strong>curtose</strong> e <strong>coeficiente de variação</strong></li>
  <li>Visualizações com <strong>Plotly</strong>, <strong>Matplotlib</strong> e <strong>Seaborn</strong></li>
</ul>

<h2>🛠️ Engenharia de Atributos</h2>

<p>Foram criadas novas variáveis para enriquecer o modelo:</p>

<ul>
  <li>Conversão de tempo (<code>step</code>) para <strong>dias</strong> e <strong>semanas</strong></li>
  <li>Diferença entre os saldos antes e depois da transação</li>
  <li>Extração do primeiro caractere dos identificadores de origem/destino</li>
</ul>

<h2>🧪 Treinamento e Validação</h2>

<p>Utilizei o <strong>Stratified K-Fold Cross Validation</strong> com balanceamento de classes e ajuste de hiperparâmetros via <strong>GridSearchCV</strong>, além da normalização dos dados com <strong>MinMaxScaler</strong>.</p>

<h2>📁 Dataset</h2>

<p>O dataset utilizado está disponível publicamente e foi carregado a partir do meu Google Drive. Contém mais de 6 milhões de registros simulados de transações bancárias.</p>

<h2>🚀 Como Executar</h2>

<ol>
  <li>Clone este repositório:
    <pre><code>git clone https://github.com/seu-usuario/seu-repo.git</code></pre>
  </li>
  <li>Instale as dependências:
    <pre><code>pip install -r requirements.txt</code></pre>
  </li>
  <li>Rode o notebook:
    <pre><code>jupyter notebook Detecao_de_Fraude.ipynb</code></pre>
  </li>
</ol>

<h2>📌 Observações</h2>

<ul>
  <li>As classes estão fortemente desbalanceadas (menos de 0,2% de fraudes)</li>
  <li>A maioria das transações fraudulentas ocorre nas operações de tipo <strong>TRANSFER</strong> e <strong>CASH_OUT</strong></li>
  <li>Alguns modelos, como SVM e Regressão Logística, não se mostraram adequados sem técnicas adicionais de balanceamento</li>
</ul>

