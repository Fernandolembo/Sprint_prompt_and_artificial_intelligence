# Sprint_prompt_and_artificial_intelligence

GoodWe SmartCharge Intelligence - EV Challenge 2026.
Membros: Fernando Henrique Lembo - RM: 570228 Guilherme Lopes Muniz - RM: 569521 Gustavo Russo Balizardo - RM: 569283 Ryan Barreto Carlos Dias - RM: 574126
-------------------------------------------------------------------------------------------------------------------------------------------------------------------
Problema:
A GoodWe busca expandir sua atuação no mercado de mobilidade elétrica, migrando de soluções puramente residenciais para o setor Comercial. O desafio central é a falta de um ecossistema integrado que consiga:

Orquestrar Potência: Evitar que a recarga de múltiplos veículos ultrapasse a demanda contratada do estabelecimento.

Faturamento: Registrar e cobrar pelo uso da energia de forma automatizada.

Comunicação: Oferecer uma interface intuitiva para que o gestor tome decisões rápidas.
-------------------------------------------------------------------------------------------------------------------------------------------------------------------
Proposta do chatbot:
Nossa solução é um Chatbot com IA Generativa integrado ao sistema de gestão da GoodWe. Ele atua como um assistente operacional para a persona: Gestor de Facilidades / Operador Comercial.

Por que essa Persona?
No ambiente comercial (shoppings, frotas, empresas), o tempo de resposta é crítico. O gestor não pode navegar por planilhas complexas para saber por que um carregador parou ou quanto foi faturado. O chatbot simplifica dados técnicos em decisões de negócio.

Funcionalidades Principais:
Diagnóstico de Falhas: Tradução de erros de hardware para linguagem humana.

Gestão de Energia: Consultas em tempo real sobre o balanceamento de carga e economia solar.

Suporte ao Faturamento: Resumo de consumo por usuário e status de pagamentos.
-------------------------------------------------------------------------------------------------------------------------------------------------------------------
Tecnologias selecionadas e Justificativa:
LLM (Cérebro): Gemini 1.5 Flash (Google). Escolhido pela alta velocidade de resposta e capacidade de processar grandes volumes de manuais técnicos (Context Window).

Framework: LangChain. Utilizado para a orquestração do sistema, permitindo que a IA consulte documentos (RAG) e execute ferramentas (APIs).

Interface: Streamlit. Para prototipagem rápida de uma interface web amigável.

Base de Conhecimento: Arquivos PDF/Markdown contendo manuais da linha GoodWe EV e protocolos OCPP.
-------------------------------------------------------------------------------------------------------------------------------------------------------------------
Fluxograma de funcionamento:
Entrada (Input): O usuário (Gestor ou Operador) interage com o sistema enviando uma dúvida técnica, uma solicitação de dados de consumo ou relatando um código de erro do carregador.

Triagem e Orquestração (LangChain): O orquestrador analisa a intenção da pergunta. Se a dúvida exigir conhecimento específico (manual ou status real), o sistema ativa os mecanismos de busca. Caso contrário, segue para resposta direta.

Recuperação de Conhecimento (RAG & API): * Dados Estáticos: O sistema realiza uma busca vetorial (RAG) em manuais técnicos da GoodWe para traduzir códigos de erro.

Dados Dinâmicos: Consulta em tempo real via protocolo OCPP/API para verificar a telemetria (potência atual, consumo e status do conector).

Processamento Cognitivo (LLM): O modelo Gemini 1.5 Flash recebe o contexto do System Prompt + os dados recuperados no passo anterior. A IA cruza estas informações para garantir que a resposta seja tecnicamente precisa e livre de alucinações.

Saída (Output): O chatbot entrega uma resposta contextualizada com um "Insight Acionável" (ex: sugerir o reset de um disjuntor ou informar o faturamento exato do período).
