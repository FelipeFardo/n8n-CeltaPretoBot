# 🌤️ CeltaPreto – Bot de Previsão do Tempo com Recomendações Inteligentes

O CeltaPreto é um bot de previsão do tempo desenvolvido no n8n, integrado ao Telegram, à API do OpenWeather e a um agente de IA (Google Gemini) para fornecer previsão do tempo + recomendações práticas personalizadas para o dia do usuário.

O bot recebe o nome da cidade via Telegram e retorna:

Temperatura atual

Condição climática

Dicas do que vestir e cuidados diários, com linguagem natural e amigável

## 🚀 Funcionalidades

📩 Recebe mensagens via Telegram Bot

🌍 Normaliza nomes de cidades (acentos, maiúsculas/minúsculas)

☁️ Consulta clima em tempo real pela OpenWeather API

🧠 Gera recomendações inteligentes usando IA (Google Gemini)

🗣️ Respostas em português (pt-BR)

❌ Tratamento de erros para cidades inválidas

▶️ Comando /start com mensagem de boas-vindas

## 🛠️ Tecnologias Utilizadas

n8n – Orquestração do workflow

Telegram Bot API – Interface com o usuário

OpenWeather API – Dados climáticos

Google Gemini (PaLM) – Geração de texto inteligente

JavaScript – Normalização e formatação de dados

## 🧩 Fluxo do Workflow

Telegram Trigger

Recebe mensagens do usuário

Verificação do /start

Envia mensagem inicial se necessário

Normalização da Cidade

normalizeCityToHuman: Formato amigável

normalizeCity: Formato compatível com API

Consulta à OpenWeather

Busca temperatura e condição climática

Validação da Resposta

Confirma se os dados retornaram corretamente

Processamento com IA

Gera recomendações baseadas no clima

Envio da Resposta Final

Mensagem completa ou fallback simples

💬 Exemplo de Uso
Entrada (Telegram):
São Paulo

Saída:
🌤️ A temperatura em São Paulo é de 26°C.

Leve roupas leves e confortáveis, use protetor solar e mantenha-se bem hidratado ao longo do dia. Se for sair por muito tempo, um óculos de sol pode ajudar bastante!

❌ Tratamento de Erros

Se a cidade não for encontrada:

❌ Ops! Não consegui encontrar essa cidade.

Verifique se o nome está correto e tente novamente 🙏
Dica: use apenas o nome da cidade, sem abreviações ou símbolos.

📍 Exemplos válidos:
São Paulo
Rio de Janeiro
Lisboa

## 🔐 Credenciais Necessárias

Configure as seguintes credenciais no n8n:

Telegram

Telegram Bot Token

OpenWeather

API Key

Endpoint: https://api.openweathermap.org/data/2.5/weather

Google Gemini (PaLM)

API Key do Google AI Studio

## ⚙️ Configurações Importantes

Idioma da API OpenWeather: pt_br

Unidade de temperatura: metric (°C)

Temperatura do modelo IA: 0.2 (respostas mais consistentes)

Output estruturado com:

generated_text

status

## 📦 Importação do Projeto

Abra o n8n

Vá em Workflows → Import

Cole o JSON do projeto

Configure as credenciais

Ative o workflow ✅

## 📌 Status do Projeto

✔️ Funcional

🧪 Pronto para testes em produção

🔄 Fácil de expandir (previsão semanal, alertas, localização automática, etc.)