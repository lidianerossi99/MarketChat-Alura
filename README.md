# MarketChat: Seu Assistente de Compras Inteligente 🛍️💬

Bem-vindo ao MarketChat, um chatbot assistente de compras desenvolvido em Python durante a Imersão IA da Alura em parceria com o Google! Este projeto visa facilitar a busca inicial por produtos, direcionando você para os principais e mais seguros marketplaces do Brasil.

## 🎥 Vídeo de Demonstração

Assista ao MarketChat em ação e veja como ele pode simplificar suas buscas por produtos!

https://youtu.be/PYoqQGBh810


Este projeto foi desenvolvido pensando nos seguintes critérios:

*   **Utilidade:** O MarketChat busca simplificar a jornada de compra online. Em vez de abrir inúmeras abas e navegar por diversos sites, o usuário pode rapidamente obter direcionamentos para categorias de produtos nos principais varejistas brasileiros, economizando tempo e esforço na fase inicial de pesquisa.
*   **Criatividade:** A criatividade está na combinação da API de busca programável do Google com uma lógica personalizada em Python para filtrar e apresentar resultados de forma amigável. O uso de um "refinamento" no Mecanismo de Busca Personalizado (CSE) para focar apenas em marketplaces selecionados e a tentativa de apresentar variedade de lojas são diferenciais. A interface, mesmo em linha de comando, foi pensada para ser acolhedora com o uso de emojis.
*   **Eficácia:** O chatbot demonstra eficácia ao conectar-se à API do Google, aplicar o refinamento configurado para `MarketplacesBR`, processar os resultados e apresentar ao usuário até 3 sugestões de marketplaces distintos (quando a API fornece essa variedade para a busca). *Veja o vídeo de demonstração acima para conferir o chatbot em ação!*


## ✨ Funcionalidades Principais

*   **Busca Inteligente:** Digite o produto que deseja e o MarketChat busca por você.
*   **Foco em Marketplaces Brasileiros:** Utiliza um Mecanismo de Busca Personalizado do Google configurado para priorizar os principais e mais seguros e-commerces do Brasil.
*   **Variedade de Opções:** Tenta apresentar até 3 marketplaces diferentes para sua consulta, quando disponíveis nos resultados da API.
*   **Interação Amigável:** Interface de linha de comando com mensagens claras e emojis para uma conversa mais simpática.
*   **Direcionamento Correto:** Fornece links diretos para as páginas de categoria ou busca dos marketplaces, onde o usuário pode explorar produtos, preços e usar os filtros avançados da própria loja.

## 🛠️ Tecnologias Utilizadas

*   **Python 3**
*   **Google Programmable Search Engine (CSE):** Para criar um mecanismo de busca focado nos marketplaces desejados.
*   **Google Custom Search JSON API:** Para interagir com o CSE via código.
*   **Bibliotecas Python:**
    *   `requests`: Para realizar as chamadas HTTP à API do Google.
    *   `python-dotenv`: Para gerenciar as chaves de API de forma segura em ambiente de desenvolvimento local.

## ⚙️ Configuração e Execução Local

Para testar o MarketChat em sua máquina, siga os passos abaixo:

1.  **Pré-requisitos:**
    *   Python 3.7 ou superior instalado.
    *   Git instalado (para clonar o repositório).

2.  **Clone o Repositório:**
    ```bash
    git clone https://github.com/SEU_USUARIO/NOME_DO_SEU_REPO.git
    cd NOME_DO_SEU_REPO
    ```

3.  **Crie e Ative um Ambiente Virtual (Recomendado):**
    ```bash
    python -m venv venv
    # No Windows:
    .\venv\Scripts\activate
    # No macOS/Linux:
    source venv/bin/activate
    ```

4.  **Instale as Dependências:**
    ```bash
    pip install -r requirements.txt
    ```

5.  **Configure suas Chaves API do Google (MUITO IMPORTANTE):**
    *   **Obtenha suas credenciais:**
        1.  Você precisará de uma **API Key** do Google Cloud Platform com a "Custom Search JSON API" habilitada. [Guia para criar API Key](https://cloud.google.com/docs/authentication/api-keys).
        2.  Você precisará criar um **Programmable Search Engine (CSE)** ([cse.google.com](https://cse.google.com/)).
            *   Configure-o para pesquisar nos sites que desejar (ex: `www.mercadolivre.com.br/*`, `www.amazon.com.br/*`, `www.magazineluiza.com.br/*`, etc.).
            *   Crie um **Rótulo de Refinamento** chamado `MarketplacesBR` (ou o nome que desejar, mas ajuste no código) e adicione esses sites a ele, selecionando "Pesquisar em sites com esse refinamento".
            *   Copie o **ID do mecanismo de pesquisa** (CSE ID).
    *   **Crie um arquivo `.env`** na raiz do projeto (na mesma pasta do `market_chat.py`).
    *   Adicione suas chaves ao arquivo `.env` (substitua pelos seus valores reais):
        ```env
        GOOGLE_API_KEY="SUA_GOOGLE_API_KEY_REAL_AQUI"
        GOOGLE_CSE_ID="SEU_CSE_ID_REAL_AQUI"
        ```
 

6.  **Execute o Chatbot:**
    ```bash
    python market_chat.py
    ```

## 💬 Como Usar o Chatbot

Após iniciar o script, o MarketChat te dará as boas-vindas!
1.  Digite o nome do produto que você está procurando (ex: `notebook gamer`, `celular samsung`, `fone de ouvido bluetooth`).
2.  O chatbot buscará nos marketplaces configurados e apresentará até 3 sugestões de lojas diferentes.
3.  Para cada sugestão, você verá o nome/título da página, a loja, alguns detalhes (snippet) e um link para visitar.
4.  Digite `encerrar` a qualquer momento para finalizar a conversa.

## ⚠️ Limitações Conhecidas

*   A qualidade e a variedade dos resultados dependem da API do Google e da configuração do Mecanismo de Busca Personalizado (CSE).
*   A interface atual é via linha de comando.


## ✍️ Autor(a)

*   **lidiane_rossi99**
*   https://www.linkedin.com/in/lidiane-rossi

## 📜 Licença

Este projeto está licenciado sob a Licença MIT. Veja o arquivo `LICENSE` para mais detalhes.

---

Espero que este projeto seja útil e divertido de explorar!