# NexusBot - Assistente Virtual WhatsApp IA

![NexusBot](https://img.shields.io/badge/NexusBot-Assistente%20Virtual-blue)
![Flask](https://img.shields.io/badge/Flask-2.0.1-green)
![AI21](https://img.shields.io/badge/AI21-API-orange)
![WhatsApp](https://img.shields.io/badge/WhatsApp-API-brightgreen)

## 📋 Sobre

NexusBot é um assistente virtual integrado ao WhatsApp, desenvolvido com Flask e alimentado por modelos avançados de linguagem da AI. O nome "NexusBot" deriva de "nexus" (conexão), refletindo seu propósito de conectar usuários a respostas rápidas e precisas.

Criado por Jacinto Sérgio Robate, estudante de Tecnologias de Informação na Universidade Católica de Moçambique, o NexusBot oferece uma gama de funcionalidades úteis através de uma interface familiar e acessível - o WhatsApp.

## ✨ Funcionalidades

- **🤔 Perguntas e Respostas**: Responde perguntas sobre diversos assuntos utilizando o modelo Jamba-1.5-large da AI21
- **📝 Geração de Trabalhos Acadêmicos**: Cria documentos DOCX completos e formatados a partir de um tema fornecido
- **🖼️ Geração de Imagens**: Gera imagens baseadas em descrições textuais usando o modelo FLUX.1-dev da Hugging Face
- **💼 Vagas de Emprego**: Conexão com portais de vagas de emprego nacionais e internacionais
- **📊 Sistema de Feedback**: Canal direto para reclamações e sugestões
- **📱 Menu Interativo**: Interface intuitiva com botões e listas no WhatsApp

## 🛠️ Tecnologias Utilizadas

- **Flask**: Framework web para Python
- **AI API**: Modelos avançados de linguagem para geração de texto
- **WhatsApp Cloud API**: Para integração com o WhatsApp
- **Hugging Face API**: Para geração de imagens
- **python-docx**: Para criação e formatação de documentos DOCX
- **python-dotenv**: Para gerenciamento de variáveis de ambiente

## 📦 Pré-requisitos

- Python 3.7+
- Conta no WhatsApp Business API
- Chaves de API para AI21 e Hugging Face
- Token de acesso WhatsApp Cloud API

## 🚀 Instalação

1. Clone o repositório:

```bash
git clone hhttps://github.com/Jacinto-robate/Bot_WhatsApp.git
cd Bot_WhatsApp
```

2. Instale as dependências:

```bash
pip install -r requirements.txt
```

3. Configure as variáveis de ambiente:
   Crie um arquivo `.env` na raiz do projeto com as seguintes variáveis:

```
AI21_API_KEY=sua_chave_api_ai21
AI21_API_KEY_TRABALHO=sua_chave_api_ai21_trabalho
WHATSAPP_ACCESS_TOKEN=seu_token_whatsapp
HUGGINGFACE_API_KEY=sua_chave_api_huggingface
```

4. Inicie o servidor:

```bash
python app.py
```

## 📝 Uso

Uma vez configurado e em execução, os usuários podem interagir com o NexusBot enviando mensagens para o número de WhatsApp associado. O bot responderá com um menu interativo, permitindo acesso às seguintes funcionalidades:

1. **Fazer uma pergunta**: O usuário envia uma pergunta, e o NexusBot responde usando o modelo da AI
2. **Sobre o criador**: Informações sobre o criador do bot
3. **Gerar trabalho**: O bot solicita um tema e gera um trabalho acadêmico completo em formato DOCX
4. **Reclamações**: Canal para envio de feedback ao administrador
5. **Vagas de emprego**: Links para portais de emprego nacionais e internacionais
6. **Gerar imagens**: Cria imagens com base em descrições textuais

## 🔧 Configuração do Webhook

Para receber mensagens do WhatsApp, você precisa configurar um webhook:

1. Disponibilize seu servidor publicamente (usando ngrok, por exemplo)
2. Configure a URL de callback no WhatsApp Business API:
   - URL: `https://seu-dominio.com/webhook`
   - Token de verificação: seu WHATSAPP_ACCESS_TOKEN

## 📁 Estrutura do Projeto

```
nexusbot/
├── app.py             # Aplicação principal Flask
├── .env               # Variáveis de ambiente (não incluído no repositório)
├── requirements.txt   # Dependências do projeto
├── README.md          # Este arquivo
└── /tmp/              # Diretório temporário para arquivos gerados
```

## ⚙️ Arquitetura

O NexusBot segue uma arquitetura baseada em eventos:

1. O usuário envia uma mensagem para o número do WhatsApp
2. O WhatsApp encaminha a mensagem para o webhook configurado
3. A aplicação Flask processa a mensagem e determina a ação apropriada
4. O bot gera uma resposta (texto, documento ou imagem) usando as APIs apropriadas
5. A resposta é enviada de volta ao usuário via WhatsApp

## 🧩 Exemplos de Uso

### Geração de Trabalhos Acadêmicos

```
Usuário: *Seleciona "Gerar trabalho"*
Bot: "Que incrível! Me diga, sobre qual tema você gostaria que eu escrevesse o seu trabalho?"
Usuário: "Inteligência Artificial na medicina"
Bot: *Gera e envia um documento DOCX formatado sobre o tema*
```

### Geração de Imagens

```
Usuário: *Seleciona "Gerar imagens"*
Bot: "Envie a descrição da imagem que deseja gerar:"
Usuário: "Um gato com óculos de sol lendo um livro em uma praia"
Bot: *Gera e envia até 3 imagens baseadas na descrição*
```

## 🔒 Segurança

- Filtragem de conteúdo impróprio para geração de imagens
- Proteção contra solicitações de geração de trabalhos em massa
- Encaminhamento de feedback apenas para administradores autorizados

## 👨‍💻 Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para enviar pull requests ou abrir issues com sugestões e melhorias.

## 📄 Licença

Este projeto está licenciado sob a [MIT License](LICENSE).

## 📞 Contato

- **LinkedIn**: [Jacinto Robate](https://www.linkedin.com/in/jacinto-robate-942a62267/)

---

<p align="center">
  Desenvolvido com ❤️ por Jacinto Sérgio Robate
</p>
