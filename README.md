# 📰 IA NewsLetter Generator

Um projeto pessoal que utiliza **Inteligência Artificial** para coletar e resumir automaticamente **notícias de sites preferidos pelos usuários**, gerando uma **newsLetter personalizada** por e-mail ou por meio de uma interface web.

---

## 🚀 Objetivo

Facilitar o consumo de notícias através de um sistema que permite:

- O usuário informar seus sites favoritos.
- IA ler, interpretar e resumir as notícias mais recentes.
- Envio automático de newsletters por e-mail.
- Armazenamento temporário das notícias para performance e escalabilidade.

---

## 🛠️ Tecnologias Utilizadas

- **Backend**: Django + Django Rest Framework
- **Banco de dados**: PostgreSQL
- **Frontend**: Django Templates (HTML, CSS, JS)
- **IA Generativa**: Gemini API (resumos automáticos)
- **Scraping**: Gemini interpretando o conteúdo da URL
- **Deploy**: Render (gratuito)
- **Envio de e-mail**: SMTP, Mailgun ou SendGrid
- **Fallback de imagens**: `onerror` em `<img>` HTML

---

## 👤 Funcionalidades

- [x] Cadastro e login de usuários
- [x] Usuário pode informar os sites de notícias que gosta
- [x] IA resume automaticamente as notícias mais recentes
- [x] Página personalizada com as notícias resumidas
- [x] Usuário pode marcar até 50 notícias como favoritas
- [x] Notícias expiram após 24h (exceto favoritas)
- [x] Newsletter enviada por e-mail com 1 a 5 notícias
- [x] Imagem padrão exibida caso a original falhe

---

## 📬 Exemplo de Newsletter

### Título: Crise na Política Brasileira  
**Resumo:** A crise entre os poderes continua a se agravar após as declarações do Congresso. Especialistas indicam que os próximos dias serão decisivos.  
📅 19/05/2025 – 🌐 Fonte: G1

[Ler mais](https://g1.globo.com/...)

---

## ⚙️ Como rodar localmente

```bash
# Clone o repositório
git clone https://github.com/seu-usuario/ia-newsletter.git
cd ia-newsletter

# Crie um ambiente virtual
python -m venv venv
source venv/bin/activate  # Linux/macOS
venv\Scripts\activate     # Windows

# Instale as dependências
pip install -r requirements.txt

# Configure o .env (veja .env.example)
cp .env.example .env

# Rode as migrações
python manage.py migrate

# Inicie o servidor
python manage.py runserver
