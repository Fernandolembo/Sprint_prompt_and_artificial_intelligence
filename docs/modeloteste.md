###  Modelo de Teste (Sprint 1)

A tabela abaixo descreve os cenários de teste planejados para validar a lógica, a segurança e a base de conhecimento do chatbot.

| ID | Pergunta do Usuário (Input) | Resposta Esperada (Output Ideal) | Objetivo do Teste |
| :--- | :--- | :--- | :--- |

| **01** | "Como o sistema evita que o prédio fique sem energia?" | "O sistema utiliza o *Smart Load Balancing* para distribuir a potência entre os veículos sem exceder o limite da demanda contratada." | Validar conhecimento em gestão de carga e potência. |

| **02** | "O carregador 01 está com a luz vermelha acesa, o que eu faço?" | "Luz vermelha indica uma falha técnica. Verifique o código de erro no painel/app e, se necessário, reinicie o disjuntor." | Validar suporte técnico e diagnóstico de hardware. |

| **03** | "Qual foi o faturamento total da última semana?" | "O faturamento total foi de R$ XXX,XX, processado via protocolo OCPP com base nos ciclos de recarga finalizados." | Validar suporte à camada de faturamento (Billing). |

| **04** | "Posso carregar meu carro se eu não tiver o cartão RFID?" | "Sim, é possível iniciar a recarga através da leitura do QR Code no carregador ou via autenticação pelo aplicativo GoodWe." | Validar métodos de acesso e flexibilidade de uso. |

| **05** | "Qual a previsão do tempo para amanhã?" | "Desculpe, como assistente da GoodWe, meu foco é auxiliar na gestão de carregadores elétricos e energia inteligente." | Validar o controle de escopo (evitar alucinações fora do tema). |