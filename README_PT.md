# EcommerceScraperHub

Uma solução abrangente para scraping de dados de produtos de plataformas de e-commerce como Kabum e Pichau, armazenando-os eficientemente e exibindo-os através de uma interface web moderna e responsiva construída com Ant Design.

## Funcionalidades

- **Extração de Dados**: Raspagem automatizada de detalhes de produtos da Kabum e Pichau.
- **Armazenamento de Dados**: Armazena os dados extraídos em formato JSON estruturado.
- **Gerenciamento de Imagens**: Baixa imagens de produtos e fornece assets de fallback para imagens ausentes.
- **Interface Web Moderna**: Uma UI responsiva e interativa construída com Ant Design.
- **Filtragem Avançada**: Filtre produtos por categoria, faixa de preço e fonte.
- **Funcionalidade de Busca**: Busca em texto completo em todos os atributos do produto.
- **Detalhes do Produto**: Visual dedicado para especificações e detalhes de cada produto.
- **Melhorias de UX**: Animações suaves, efeitos de hover e layout responsivo para todos os dispositivos.

## Tecnologias Utilizadas

- **Backend**: Python 3.x (Requests, BeautifulSoup, Faker)
- **Frontend**: HTML5, CSS3, JavaScript (React via CDN do Ant Design)
- **Armazenamento**: Arquivo JSON (`db.json`)

## Pré-requisitos

- Python 3.6+
- Navegador Web Moderno (Chrome, Firefox, Edge)

## Instalação e Configuração

### 1. Clone o Repositório
bash
git clone https://github.com/seu-username/ecommerce-scraper-hub.git
cd ecommerce-scraper-hub


### 2. Instale as Dependências Python
bash
pip install -r requirements.txt


### 3. Execute os Scripts de Coleta de Dados

**Passo 3a: Coletar Dados dos Produtos**
Execute o scraper principal para buscar produtos dos sites configurados.
bash
python scraper.py


**Passo 3b: Gerar Imagens de Fallback**
Crie imagens de placeholder para produtos que não possuem imagem disponível.
bash
python gerar_imagem_fallback.py


*Nota: Isso irá gerar um arquivo `db.json` e um diretório `images/` contendo os assets dos produtos.*

### 4. Inicie a Interface Web

Simplesmente abra o arquivo `index.html` em seu navegador ou sirva-o via um servidor web local (recomendado para políticas de CORS).
bash
# Usando o servidor HTTP embutido do Python
python -m http.server 8000
# Acesse http://localhost:8000


## Estrutura do Projeto


ecommerce-scraper-hub/
├── scraper.py              # Script principal para extração de dados
├── gerar_imagem_fallback.py # Script para gerar imagens de placeholder
├── requirements.txt        # Dependências Python
├── db.json                # Banco de dados JSON com dados dos produtos
├── index.html             # Ponto de entrada principal da aplicação web
├── screenshots/           # Comparações visuais das versões da UI
├── images/                # Imagens de produtos baixadas
└── README.md              # Documentação do projeto


## Como Funciona

1.  **Scraping**: O script `scraper.py` usa bibliotecas Python para enviar requisições HTTP aos sites de e-commerce, analisar as respostas HTML e extrair informações relevantes de produtos (nome, preço, categoria, fonte, URL da imagem).
2.  **Processamento de Dados**: Os dados extraídos são padronizados e salvos em `db.json`. Simultaneamente, as imagens são baixadas e salvas localmente.
3.  **Imagens de Fallback**: Se um produto não possuir imagem, `gerar_imagem_fallback.py` garante que um placeholder exista.
4.  **Renderização do Frontend**: O arquivo `index.html` carrega os dados de `db.json`. Ele usa a biblioteca Ant Design (via CDN) para renderizar uma grade dinâmica e filtrável de produtos.

## Contribuindo

Contribuições são bem-vindas! Fique à vontade para enviar um Pull Request.

1.  Fork o Projeto
2.  Crie sua Branch de Feature (`git checkout -b feature/FeatureIncrivel`)
3.  Commit suas Alterações (`git commit -m 'Adiciona FeatureIncrivel'`)
4.  Push para a Branch (`git push origin feature/FeatureIncrivel`)
5.  Abra um Pull Request