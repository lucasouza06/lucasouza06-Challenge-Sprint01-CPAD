# 🌿 VegTrack
### Gestão Ecológica e Inteligente da Vegetação em Rodovias — do dado de campo à Ordem de Serviço em segundos.

---

## 👥 Integrantes do Grupo — Turma 2CCPW · FIAP

| Nome | GitHub |
|---|---|
| Luis Otavio Santini Feitosa | — |
| Rogério Deligi | — |
| Maria Fernanda Garavelli | — |
| Vitor Barbosa de Paiva | — |
| Arthur Traldi Felix | — |
| Lucas Andrade de Souza | — |

> **Challenge CCR Motiva · Sprint 1 · 2025**

---

## 🚨 O Problema: Regulatório e Operacional

Concessionárias de rodovias brasileiras como a **CCR Motiva** operam sob rigoroso controle de agências reguladoras — principalmente a **ARTESP** (SP) e a **ANTT** (federal). O **Caderno de Encargos** dessas entidades define prazos, padrões e critérios técnicos de manutenção que, se descumpridos, resultam em **não conformidades, multas contratuais e impacto direto no orçamento da concessão**.

O crescimento da vegetação na faixa de domínio é um dos indicadores fiscalizados com maior frequência. Quando a altura supera **30 cm** (classificado como **Nível 3** pela ARTESP), a situação é considerada crítica: há risco de encobrimento de sinalização viária, redução de visibilidade e passivo regulatório imediato.

### Os três vetores do problema

**1. Vistorias visuais falhas e reativas**
O modelo tradicional depende de inspeções humanas amostrais ao longo de centenas de quilômetros de rodovia. Quando uma equipe detecta que a vegetação atingiu o Nível 3, frequentemente o fiscal da ARTESP já registrou a não conformidade antes de qualquer intervenção.

**2. Risco constante de penalidades financeiras**
A fiscalização é contínua e não avisa hora. Uma multa por sinalização encoberta ou vegetação fora do padrão drena o orçamento da concessão e compromete os índices contratuais de desempenho (IDs).

**3. Conflito entre urgência operacional e compliance ambiental**
A ausência de comunicação em tempo real sobre restrições ecológicas leva equipes de campo a usarem roçadeiras mecanizadas pesadas em períodos e áreas de nidificação de fauna protegida — como o **Sabiá-laranjeira** (*Turdus rufiventris*) entre agosto e dezembro, ou épocas de acasalamento de Jararacas. O resultado são **passivos ecológicos, autos de infração ambiental (CETESB/IBAMA) e multas graves** que se somam ao já pressionado orçamento operacional.

---

## 🧑‍💼 A Persona Principal: Carlos "Cadú" Rocha

**Carlos Eduardo Rocha**, conhecido como **Cadú**, é Supervisor de Conservação e Operações de Campo na Concessionária Motiva. Tem 38 anos e formação em Engenharia Civil (ou Agronômica) com especialização em Infraestrutura Rodoviária.

Cadú é um profissional prático e orientado a resultados. Divide seu tempo entre o escritório — coordenando equipes terceirizadas de manutenção — e a cabine de sua caminhonete, vistoriando trechos críticos da rodovia. Confia em planilhas, mas sabe que a operação no asfalto é dinâmica demais para cronogramas fixos de 30 dias.

### 😤 Suas dores operacionais

- **Cegueira territorial:** Precisa rodar a rodovia inteira para saber onde a vegetação está crítica, sem qualquer sistema de priorização por dados. Cada quilômetro que não vistoriou é um risco.
- **Estresse regulatório permanente:** Vive sob pressão constante dos critérios do Caderno de Encargos da ARTESP. Uma não conformidade registrada pelo fiscal antes da sua equipe agir significa multa e relatório de justificativa.
- **Decisões no escuro sobre fauna:** Não tem como saber, em campo, se aquele trecho com mato alto está ou não em período de reprodução de espécie protegida. Qualquer erro vira passivo ambiental.
- **Falta de rastreabilidade:** Relatórios em papel e planilhas isoladas não constroem o histórico digital que a ARTESP exige para comprovar conformidade.

### 🎯 O que Cadú precisa do VegTrack

- Saber **exatamente em quais KMs** o crescimento da vegetação atingiu estado crítico, sem precisar percorrer toda a rodovia diariamente.
- Receber **recomendações automatizadas** e baseadas em dados sobre o método ideal de intervenção: roçada mecanizada ou manual seletiva.
- Garantir **segurança jurídica e regulatória** perante a ARTESP e órgãos ambientais, com histórico digital rastreável de cada manutenção realizada.

---

## 💡 A Proposta de Solução: Ecossistema VegTrack

O **VegTrack** é um ecossistema de inteligência ecológica e operacional para a conservação de rodovias, composto por dois componentes integrados:

- **App Mobile (React Native + Expo):** Interface de campo para supervisores e técnicos, com mapa de calor em tempo real, registro de levantamentos, alertas ambientais e gestão de Ordens de Serviço.
- **Motor Analítico (FastAPI — Python):** Backend assíncrono que processa dados de vegetação, cruza com ocorrências de biodiversidade via GBIF e gera as recomendações inteligentes de intervenção.

A solução substitui o modelo tradicional de manutenção reativa por um **Modelo de Intervenção Direcionada por Dados**, organizado em três pilares:

### 🗺️ Pilar A — Digitalização e Mapa de Calor de Trechos

O sistema extingue relatórios estáticos em papel. O backend processa dados de campo mapeando a severidade da vegetação por faixas (Canteiro Central Externo, Interno, Marginal etc.) divididas a cada 500 metros. O supervisor visualiza um **mapa de calor em tempo real** com os trechos que violam diretamente os parâmetros da ARTESP — sem precisar percorrer a rodovia.

### 🦜 Pilar B — Motor de Restrição Ambiental Integrado

O grande diferencial da solução é o **cruzamento dos dados operacionais com a biodiversidade local**. Através do consumo da base global GBIF (*Global Biodiversity Information Facility*) e de um calendário nativo de regras de preservação — com mapeamento automatizado de espécies nativas das rodovias do estado de São Paulo —, o VegTrack atua como um **validador de conformidade ecológica em tempo real**.

### 📋 Pilar C — Geração Inteligente de Ordens de Serviço (OS)

Em vez de ordens de roçada genéricas, o sistema gera recomendações customizadas que conciliam urgência operacional com impacto ambiental:

| Cenário | Ação do VegTrack |
|---|---|
| Trecho crítico + sem restrição de fauna | Recomenda **roçada mecanizada** com prazo urgente de 48h |
| Trecho crítico + período reprodutivo de espécie protegida | Emite **Alerta Ambiental Crítico**, bloqueia tratores e exige **roçada manual seletiva** |

---

## 📋 Requisitos do Sistema

### ✅ Requisitos Funcionais (RF)

#### Pilar A — Levantamento e Mapa de Calor

- **RF001 — Visualizar mapa de trechos críticos:** Exibir mapa interativo com heatmap dos KMs da rodovia, colorido por nível de severidade da vegetação (Níveis 1–3 da ARTESP). Segmentos de 500m coloridos em verde (ok), amarelo (atenção) ou vermelho (Nível 3/crítico).

- **RF002 — Registrar levantamento de vegetação em campo:** Permitir que o técnico cadastre altura da vegetação por trecho com foto e geolocalização automática, funcionando offline. Formulário inclui KM inicial/final, faixa, altura estimada, status e foto opcional.

- **RF003 — Consultar histórico de levantamentos por trecho:** Exibir linha do tempo dos registros históricos de um segmento, com gráfico de tendência de crescimento, data do último levantamento e dias desde a última roçada.

#### Pilar B — Motor de Restrição Ambiental

- **RF004 — Exibir alertas de restrição ambiental por trecho:** Mostrar avisos visuais de alerta crítico quando um trecho estiver em período de reprodução de fauna protegida. Impossibilita criação de OS mecanizada nesse estado.

- **RF005 — Consultar calendário de restrições de fauna:** Disponibilizar tela com calendário anual das espécies protegidas mapeadas na rodovia, seus períodos de restrição, tipo de limitação e KMs afetados.

- **RF006 — Receber notificações push de entrada em período restrito:** Enviar notificação automática ao supervisor quando uma espécie protegida entrar em período de restrição nos trechos sob sua gestão, mesmo com app em background.

#### Pilar C — Ordens de Serviço Inteligentes

- **RF007 — Gerar Ordem de Serviço automatizada por trecho:** Criar OS com método de intervenção recomendado (mecanizada vs. manual seletiva) gerado pelo backend. Bloqueia método mecanizado se flag de restrição ambiental estiver ativa.

- **RF008 — Listar e gerenciar ordens de serviço abertas:** Dashboard com lista de todas as OS ativas, filtrável por status (pendente, em execução, concluída), método e urgência. Permite confirmar execução, registrar conclusão com foto e escalar urgência.

- **RF009 — Registrar conclusão de OS com evidência fotográfica:** Finalizar OS com foto geotaggeada obrigatória e timestamp imutável, gerando rastreabilidade digital perante a ARTESP. Comprovante exportável em PDF.

#### Autenticação e Configuração

- **RF010 — Autenticar usuário com perfil de acesso:** Login com e-mail/senha ou SSO corporativo. Perfis de acesso: Supervisor, Técnico de Campo e Gestor (read-only). JWT em SecureStore com refresh token de 7 dias.

- **RF011 — Configurar trecho de rodovia gerenciado:** Permitir que o supervisor defina o trecho (KM inicial/final) que gerencia, filtrando todas as telas para esse contexto.

- **RF012 — Exportar relatório de conformidade em PDF:** Gerar relatório com histórico de OS concluídas, evidências fotográficas e indicadores de conformidade do período, para envio à ARTESP.

---

### ⚙️ Requisitos Não Funcionais (RNF)

- **RNF001 — Operação offline com sincronização automática:** O app deve operar completamente sem internet para levantamento e consulta de OS. Sincronização automática ao recuperar conexão, via fila com estratégia last-write-wins. Tiles de mapa em cache para o trecho configurado.

- **RNF002 — Precisão de geolocalização mínima de 10 metros:** Captura de coordenadas GPS com `accuracy: Location.Accuracy.High`. Se precisão > 25m, exibe aviso ao usuário. Precisão registrada no payload para fins de rastreabilidade regulatória.

- **RNF003 — Tempo de resposta da API inferior a 2 segundos:** Endpoints críticos devem responder em até 2s em rede 4G. Backend implementa cache Redis para dados do GBIF (TTL 24h) e paginação máxima de 50 itens por página.

- **RNF004 — Segurança: dados sensíveis criptografados em repouso e em trânsito:** JWT em `expo-secure-store`. Comunicações via HTTPS/TLS 1.3. Banco SQLite local criptografado. Dados de localização nunca logados em texto plano. Conformidade com LGPD.

- **RNF005 — Compatibilidade com Android 10+ e iOS 14+:** Target SDK Android 34. iOS deployment target 14.0. Expo SDK 51+. Testes obrigatórios em dispositivo físico Android para validar GPS e câmera.

- **RNF006 — Usabilidade adaptada para uso em campo:** Área de toque mínima de 48×48dp. Contraste mínimo WCAG AA. Fonte mínima 16sp. Botões primários com altura mínima 56dp. Feedback háptico em ações críticas. Tema claro obrigatório (uso ao sol).

- **RNF007 — Tamanho do bundle final inferior a 50MB:** APK/IPA de produção com no máximo 50MB. Hermes engine habilitado. Code splitting por rota. Tiles de mapa carregados on-demand. Bundle size monitorado no CI como gate de build.

- **RNF008 — Rastreabilidade de auditoria com log imutável de ações:** Toda ação crítica gera evento de auditoria com timestamp, usuário e dados anteriores/posteriores. Log imutável com retenção mínima de 5 anos, conforme exigências do PER.

---

### 🔒 Restrições Técnicas (RT)

- **RT001 — Framework obrigatório: React Native com Expo SDK:** Todo o frontend mobile desenvolvido exclusivamente em React Native com Expo Managed Workflow (sem ejeção nesta sprint). TypeScript estrito. Distribuição via EAS Build.

- **RT002 — Backend exclusivamente em FastAPI (Python):** Nenhuma lógica de negócio replicada no frontend. O app é apenas camada de apresentação e coleta. Contrato de API documentado com OpenAPI 3.0. Versionamento: `/api/v1/`.

- **RT003 — Integração GBIF via backend (nunca direta do app):** O app não realiza chamadas diretas à API do GBIF. Toda consulta de biodiversidade passa pelo backend, que aplica cache e regras de negócio. API key do GBIF nunca exposta no bundle.

- **RT004 — Autenticação via JWT stateless:** Backend sem estado de sessão. JWT com expiração de 1h e refresh token de 7 dias. Algoritmo HS256 ou RS256. Proibido armazenar JWT em AsyncStorage não criptografado.

- **RT005 — Mapas com provedores de licença corporativa compatível:** Uso de Mapbox GL ou OpenStreetMap via tiles self-hosted. Google Maps API permitido apenas em protótipo — avaliar custos para produção.

- **RT006 — Conformidade com LGPD para dados de geolocalização:** Coleta de localização GPS requer consentimento explícito com finalidade declarada. Usuário pode revogar em Configurações. Dados de localização associados ao técnico retidos por no máximo 2 anos.

- **RT007 — Escopo da Sprint 1: rodovias do estado de São Paulo:** Motor de restrição ambiental calibrado para fauna e flora nativas do estado de SP. Consultas GBIF filtradas pelo bbox de SP. Calendário de restrições validado com base em espécies catalogadas pela CETESB e SMA-SP.

---

## 🛠️ Stack Tecnológica e Justificativa de Engenharia

Para o ecossistema **VegTrack**, foi selecionada uma arquitetura desacoplada e moderna (Client-Server), garantindo alta performance em campo, escalabilidade e conformidade com as diretrizes de Edge Computing e desenvolvimento sustentável (ESG).

### 1. Frontend Mobile: React Native + Expo Ecosystem

* **Aderência ao Contexto Operacional:** O Supervisor de Campo (Cadú) opera em ambientes de rodovia onde a conectividade de rede celular é frequentemente intermitente ou inexistente. O React Native permite a compilação nativa para Android e iOS, possibilitando a criação de mecanismos de cache e persistência de dados local (via *AsyncStorage* ou *SQLite*).

* **Agilidade e Sensores (Expo):** O uso do Expo acelera o ciclo de feedback e testes operacionais. Utilizaremos os módulos nativos `expo-location` para capturar as coordenadas exatas (latitude/longitude) do veículo de vistoria em tempo real, cruzando com os KMs do Rodoanel, e `expo-camera` para registrar evidências fotográficas das condições da vegetação (Nível 3) exigidas para comprovação regulatória junto à ARTESP.

* **Interface e Mapas:** A biblioteca `react-native-maps` será utilizada para renderizar de forma fluida os polígonos representativos das faixas de domínio e os marcadores dinâmicos dos trechos críticos (KMs com mato alto).

### 2. Backend: FastAPI (Python 3.13+)

* **Alta Performance Assíncrona:** O backend foi construído utilizando o **FastAPI**, aproveitando sua natureza assíncrona (baseada em *Starlette* e *Pydantic*). Isso garante que múltiplos supervisores de campo e fiscais possam consultar endpoints simultaneamente com latência mínima, essencial para sistemas operacionais de missão crítica.

* **Processamento Analítico de Planilhas (Pandas & OpenPyXL):** O core da nossa inteligência operacional lê e processa as planilhas unifilares da concessionária (arquivos `.xlsx` e `.csv` de medição da CCR Rodoanel). O motor Python extrai os percentuais de severidade (Níveis 1, 2 e 3) mapeados a cada 500 metros, transformando dados brutos e estáticos em um JSON estruturado para o aplicativo.

* **Validação de Dados e Tipagem:** O *Pydantic v2* valida rigorosamente os payloads de entrada e saída das Ordens de Serviço (`/ordens`), garantindo segurança jurídica contra corrupção de dados operacionais.

### 3. Integração com APIs Globais de Biodiversidade: GBIF API

* **Fator Diferencial de Sustentabilidade (ESG):** Através do cliente HTTP assíncrono `httpx`, o backend do VegTrack consome em tempo real os dados georreferenciados da **GBIF** (*Global Biodiversity Information Facility*). O sistema realiza requisições assíncronas baseadas em caixas envolventes (*bounding boxes*) ao redor do Rodoanel Mário Covas para mapear se espécies vulneráveis (como o *Didelphis albiventris* ou *Turdus rufiventris*) possuem registros de ocorrência no raio de 15km da rodovia.

* **Automação de Alertas Biológicos:** Esses dados biológicos externos são cruzados com as regras nativas de reprodução (mapeadas no módulo `fauna_flora.py`). Se um trecho necessita de roçada urgente, mas o algoritmo detecta que a janela temporal atual coincide com o pico reprodutivo da fauna local, a API automaticamente rebaixa o método de roçada mecanizada para manual, eliminando acidentes ecológicos e multas de órgãos ambientais.

---

## 🎨 Protótipo Navegável (Figma)

> 🔗 **[Acessar Protótipo Navegável — VegTrack](https://www.figma.com/proto/5oamsogahmd7Se6ZgcjV5S/VegTrack-%E2%80%94-Prot%C3%B3tipo?node-id=2-3&p=f&t=val4P4Xv3d7pBuVz-1&scaling=scale-down&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=2%3A3)**
>
> _Protótipo navegável com 5 telas: Login, Mapa de Calor, Detalhe do Trecho + Alerta Ambiental, Gestão de Ordens de Serviço e Registro de Conclusão com Evidência Fotográfica._

---

## 📁 Estrutura do Repositório

```
vegtrack/
├── mobile/                  # App React Native + Expo
│   ├── src/
│   │   ├── screens/         # Telas do app
│   │   ├── components/      # Componentes reutilizáveis
│   │   ├── services/        # Chamadas à API FastAPI
│   │   ├── store/           # Estado global (Zustand/Context)
│   │   └── utils/           # Helpers e constantes
│   ├── app.json
│   └── package.json
│
├── backend/                 # Motor analítico FastAPI
│   ├── routers/             # Endpoints REST (/trechos, /ordens, /restricoes-fauna)
│   ├── services/            # Lógica de negócio e integração GBIF
│   ├── models/              # Schemas Pydantic v2
│   ├── fauna_flora.py       # Calendário de restrições nativas SP
│   └── main.py
│
└── README.md
```

---

## 🚀 Como Executar o Projeto

### Pré-requisitos

- Node.js 18+
- Python 3.13+
- Expo CLI (`npm install -g expo-cli`)
- EAS CLI (`npm install -g eas-cli`)

### Backend (FastAPI)

```bash
cd backend
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
uvicorn main:app --reload
```

A documentação interativa estará disponível em `http://localhost:8000/docs`.

### Mobile (React Native + Expo)

```bash
cd mobile
npm install
npx expo start
```

Escaneie o QR Code com o app **Expo Go** (Android/iOS) ou pressione `a` para abrir no emulador Android.

---

<div align="center">

**VegTrack** · Challenge CCR Motiva · FIAP 2025 · Turma 2CCPW

_Transformando dados de campo em conformidade regulatória — quilômetro a quilômetro._

</div>
