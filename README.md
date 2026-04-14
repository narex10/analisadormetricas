# 📊 Meta Ads Analyzer - Premium SaaS

Análise avançada e em tempo real de métricas da Meta Ads (Facebook/Instagram) com suporte para múltiplas contas, cálculos de ROAS, ROI e análise de landing pages com IA.

## ✨ Características Principais

### 🎯 Hero KPI
- **ROAS em tempo real** com cor-coding de performance
- Status dinâmico (Alta performance / Estável / Crítico)
- Insights instantâneos com base em dados Meta

### 👥 Multi-Account Support
- Conecte até 2 contas Meta simultâneamente
- Agregação automática de dados sem cross-linking
- Identificação de conta em cada campanha/adset/anúncio

### 📈 Dashboards Completos
- **Visão Geral**: Hero KPI, KPIs principais, métricas do funil
- **Campanhas**: Tabela com status, gasto, impressões, CTR, CPM
- **Conjuntos**: Performance de Ad Sets com insights
- **Criativos**: Score de performance de anúncios baseado em CTR
- **Funil**: Visualização em cascata de Impressões → Cliques → Leads → Clientes
- **Página**: Análise de CRO de landing pages com Anthropic Claude
- **Calculadora**: Simulador de ROAS/CAC/Ticket médio
- **Conversões**: Métricas de funil e diagnóstico automático

### 🔐 Segurança
- Credenciais armazenadas localmente (localStorage)
- Sem backend - processamento 100% client-side
- Suporte para CORS proxy para APIs externas

## 🚀 Início Rápido

### Opção 1: Servidor Local
```bash
# Instalar Python (já incluído no Windows 11+)
python -m http.server 8080

# Abrir em navegador
http://localhost:8080/analisador_meta_ads.html
```

### Opção 2: Arquivo Direto
```bash
# Simplesmente abra o arquivo no navegador
file:///c:/Users/user/Desktop/Claude/analisador_meta_ads.html
```

## 🔑 Configuração Necessária

### Meta Ads API
1. Vá para [Meta for Developers](https://developers.facebook.com)
2. Crie um app ou use um existente
3. Gere um token de acesso longo prazo
4. Copie sua Account ID (sem "act_")

### Anthropic Claude API (opcional)
- Para análise de landing pages com IA
- Obtenha em [console.anthropic.com](https://console.anthropic.com)

## 📱 Funcionalidades

### Período Selecionável
- Hoje
- Ontem
- Últimos 7 dias
- Últimos 30 dias
- Últimos 90 dias
- Mês passado
- Últimos 3 meses

### Cálculos Automáticos
- **ROAS** = Receita Total / Investimento
- **CAC** = Investimento / Clientes Adquiridos
- **CPL** = Investimento / Leads
- **CTR** = (Cliques / Impressões) × 100
- **CPM** = (Investimento / Impressões) × 1000

### Diagnósticos Inteligentes
- Análise automática de CPL vs benchmarks
- Taxa de conversão realista
- Relação CAC/LTV
- Recomendações baseadas em performance

## 🛠️ Stack Técnico

- **Frontend**: HTML5, CSS3, JavaScript ES6+
- **Gráficos**: Chart.js 4.4.1
- **API**: Meta Ads Graph API v19.0
- **IA**: Anthropic Claude API
- **Fonts**: Google Fonts (Inter)
- **Storage**: localStorage para credenciais

## 📝 Estrutura do Projeto

```
analisadormetricas/
├── analisador_meta_ads.html  # App principal (single-file)
├── .gitignore
├── README.md
└── .vscode/
    └── launch.json          # Config para debug no VS Code
```

## 🐛 Debugging

Abra o DevTools (F12) e acesse a aba **Console** para:
- Ver logs de inicialização com 🚀/✅/❌/ℹ️
- Monitorar chamadas à API da Meta
- Verificar erros de execução com stack traces

## 🔄 Git & GitHub

```bash
# Clonar repositório
git clone https://github.com/narex10/analisadormetricas.git

# Configurar identidade
git config user.email "seu-email@exemplo.com"
git config user.name "Seu Nome"

# Push de mudanças
git add .
git commit -m "sua mensagem"
git push origin main
```

## 📊 Exemplo de Uso

1. **Configurar**: Insira tokens Meta e Anthropic no painel Config
2. **Conectar**: Clique em "Conectar e carregar dados"
3. **Analisar**: Explore as abas de dashboards
4. **Calcular**: Use a Calculadora para simular cenários
5. **Exportar**: Screenshots ou dados direto do navegador

## ⚙️ Variáveis Importantes

- `accountSets`: Array de contas conectadas `[{token, account, label, name}]`
- `dadosGlobais`: Cache de dados agregados para renderização
- `TOKEN`, `ACCOUNT`: Primeira conta Meta
- `TOKEN2`, `ACCOUNT2`: Segunda conta Meta (opcional)
- `ANTHROPIC_KEY`: Chave da API Claude (opcional)

## 🎨 Customização

Edite o arquivo HTML para:
- Mudar cores (CSS variables no `:root`)
- Adicionar novos KPIs
- Modificar periodicidades
- Integrar com outros sistemas

## 📞 Suporte

- GitHub Issues: https://github.com/narex10/analisadormetricas/issues
- Email: arcanodigital.com.br@gmail.com

## 📄 Licença

MIT - Sinta-se livre para usar, modificar e distribuir

---

**Versão**: 1.0.0  
**Última atualização**: Abril 2026
