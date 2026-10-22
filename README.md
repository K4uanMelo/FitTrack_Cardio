# 🏃‍♂️ FitTrack Cardio - Mobile App

> **Cada movimento conta.** Aplicativo móvel para monitoramento de treinos de cardio com armazenamento 100% local, métricas em tempo real e visualização de percurso via GPS.

[![Figma Prototype](https://img.shields.io/badge/Figma-Testar%20Protótipo%20Navegável-F24E1E?style=for-the-badge&logo=figma&logoColor=white)](https://www.figma.com/proto/Sb6uky8iIVB5MkyiSvg1mk/FIT-TRACK-CARDIO?node-id=2-11106&t=f0kxS6Sg30OXxjHp-1&scaling=min-zoom&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=2%3A10801)
[![React Native](https://img.shields.io/badge/React%20Native-0.72+-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://reactnative.dev/)
[![Expo](https://img.shields.io/badge/Expo-Go-000000?style=for-the-badge&logo=expo&logoColor=white)](https://expo.dev/)

---

## 🎨 Protótipo no Figma

Acesse o protótipo interativo e navegável das telas diretamente no Figma:

👉 **[Acessar Protótipo Interativo no Figma](https://www.figma.com/proto/Sb6uky8iIVB5MkyiSvg1mk/FIT-TRACK-CARDIO?node-id=2-10801&t=f0kxS6Sg30OXxjHp-1&scaling=contain&content-scaling=responsive&page-id=0%3A1&starting-point-node-id=2%3A10801)**

---

## 📱 Sobre o Projeto

O **FitTrack Cardio** é uma solução mobile voltada para a prática de atividades físicas ao ar livre (caminhada, corrida e ciclismo). Projetado com foco em simplicidade, privacidade e agilidade, o aplicativo permite que o usuário registre seus treinos e acompanhe seu progresso semanal sem a necessidade de criar contas ou depender de servidores externos.

---

## 🎯 Público-Alvo e Problema Resolvido

* **Público-Alvo:** Praticantes de atividades físicas (iniciantes a intermediários) que buscam monitorar suas métricas de cardio de forma simples e rápida.
* **Problema Resolvido:** Aplicativos de fitness tradicionais costumam exigir cadastros complexos, planos pagos e envio constante de dados para a nuvem. O FitTrack Cardio oferece acompanhamento *local-first*, gravando dados diretamente no dispositivo do usuário.

---

## 🚀 Funcionalidades do MVP

1. **Seleção de Atividade & Configuração:** Escolha da modalidade (Caminhada, Corrida, Ciclismo), data, nome personalizado e observações do percurso.
2. **Cronômetro & Telemetria em Tempo Real:** Registro ao vivo do tempo decorrido, distância percorrida (km) e velocidade média (km/h), com ações de pausa, retomada e finalização.
3. **Mapeamento & Status do GPS:** Exibição da rota no mapa com indicadores de precisão e estado da conexão GPS.
4. **Histórico & Filtros:** Listagem completa de treinos anteriores filtrável por modalidade (*Todos, Caminhada, Corrida, Ciclismo*), com detalhamento e opção de exclusão.
5. **Dashboard & Estatísticas da Semana:** Resumo dos treinos realizados na semana e quilometragem total acumulada.

---
* **Tecnologia Escolhida:** React Native (Expo)
* **Integrantes e RAs:**
  * **Arlyson Silva** — RA: 113627
  * **Kauan Melo** — RA: 113471
  * **Richard Rocha** — RA: 113760
* **Disciplina:** Desenvolvimento de Aplicativos Móveis
## 🗺️ Fluxo de Navegação e Telas

O aplicativo conta com **6 telas centrais** organizadas através de navegação inferior (*Bottom Tab Navigation*) e navegação em pilha (*Stack Navigation*):

| Tela | Descrição / Objetivo |
| :--- | :--- |
| **1. Início (Dashboard)** | Resumo semanal (quantidade de treinos e km acumulados), atalho para "Cadastrar treino" e lista dos últimos treinos. |
| **2. Treinos (Histórico)** | Listagem de treinos com filtros por atividade e busca por registros salvos. |
| **3. Cadastrar Treino** | Formulário para definir nome da sessão, modalidade, data e observações antes de iniciar a gravação. |
| **4. Mapa / Gravação** | Cronômetro ativo, métricas em tempo real, status de precisão do GPS e botões de controle (Pausar/Continuar/Finalizar). |
| **5. Detalhes do Treino** | Visualização completa de uma atividade concluída com modal para confirmação de exclusão do registro. |
| **6. Perfil do Usuário** | Estatísticas consolidadas desde a adesão ao app e informações de privacidade local. |

---

## 🛠️ Arquitetura e Estrutura do Código

Desenvolvido utilizando **React Native** com **Expo**, garantindo performance nativa e portabilidade para iOS e Android.

```text
FitTrack_Cardio/
├── assets/             # Ícones, logo e imagens estáticas
├── src/
│   ├── components/     # Componentes reutilizáveis (Cards, Botões, Badges, Header)
│   ├── screens/        # Telas da aplicação (Home, Workouts, Tracking, Profile, etc.)
│   ├── navigation/     # Configuração de rotas (TabNavigator, StackNavigator)
│   ├── context/        # Gerenciamento de estado global (WorkoutContext)
│   ├── utils/          # Funções utilitárias (Formatação de tempo, velocidade e distância)
│   └── mock/           # Dados simulados para execução do protótipo
├── App.js              # Ponto de entrada da aplicação
├── package.json        # Dependências do projeto
└── README.md           # Documentação do repositório
