# 📦 MeGuia Admin Panel - Guia de Instalação

## 🎉 Parabéns! Você baixou o Painel Admin MeGuia completo!

Este arquivo contém todo o código do painel administrativo que criamos, incluindo:

### ✅ **O que está incluído:**
- **Dashboard completo** com estatísticas em tempo real
- **Gerenciamento de Cidades** (CRUD completo)
- **Gerenciamento de Parques** com sistema de cupons
- **Gerenciamento de Passeios** 
- **Gerenciamento de Usuários**
- **Gerenciamento de Itinerários**
- **Sistema de autenticação** (Firebase + Demo)
- **Design moderno** com TailwindCSS + shadcn/ui
- **Dados de demonstração** para testes

---

## 🚀 **Como instalar:**

### **1. Extrair o arquivo:**
```bash
tar -xzf meguia-admin-panel.tar.gz
cd meguia-admin-panel
```

### **2. Instalar dependências:**
```bash
npm install
```

### **3. Executar o projeto:**
```bash
npm run dev
```

### **4. Acessar o painel:**
- URL: `http://localhost:8000`
- **Login automático** (modo demonstração ativo)

---

## 🔧 **Integração com seu projeto existente:**

### **Opção A: Usar como projeto separado**
- Execute como está para ter um painel admin independente
- Configure Firebase com suas credenciais reais

### **Opção B: Integrar no seu projeto MeGuia**
Copie estas pastas para seu projeto:

```
📁 Copiar para seu projeto:
├── src/app/admin/          # Todas as páginas do admin
├── src/components/layout/  # Layout do admin
├── src/components/auth/    # Sistema de autenticação
├── src/components/dashboard/ # Componentes do dashboard
├── src/contexts/           # Contextos (Auth)
├── src/services/           # Serviços Firebase + Demo
├── src/types/              # Tipos TypeScript
└── .env.local.example      # Exemplo de configuração
```

---

## ⚙️ **Configuração do Firebase:**

### **1. Criar arquivo `.env.local`:**
```env
NEXT_PUBLIC_FIREBASE_API_KEY=sua-api-key
NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=seu-projeto.firebaseapp.com
NEXT_PUBLIC_FIREBASE_PROJECT_ID=seu-project-id
NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=seu-projeto.appspot.com
NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=123456789
NEXT_PUBLIC_FIREBASE_APP_ID=seu-app-id
```

### **2. Configurar Firestore:**
Crie estas coleções no Firebase:
- `usuarios`
- `cidades` 
- `parques`
- `passeios`
- `itinerarios`

### **3. Ativar Firebase Auth:**
- Vá para Authentication > Sign-in method
- Ative "Email/Password"
- Crie um usuário administrador

---

## 🔄 **Alternar entre modo Demo e Produção:**

### **Modo Demo (atual):**
- Arquivo: `src/app/layout.tsx`
- Linha: `import { AuthProvider } from '@/contexts/DemoAuthContext';`

### **Modo Produção:**
- Altere para: `import { AuthProvider } from '@/contexts/AuthContext';`
- Configure Firebase conforme acima

---

## 📱 **Funcionalidades principais:**

### **Dashboard:**
- ✅ Estatísticas em tempo real
- ✅ Cards coloridos com métricas
- ✅ Atividades recentes
- ✅ Ações rápidas

### **Cidades:**
- ✅ CRUD completo
- ✅ Upload de imagens
- ✅ Busca e filtros

### **Parques:**
- ✅ CRUD completo
- ✅ **Sistema de cupons integrado**
- ✅ Configuração de horários
- ✅ Dias da semana disponíveis
- ✅ Público-alvo e transporte
- ✅ Badge "Cupom disponível"

### **Passeios:**
- ✅ CRUD completo
- ✅ Configuração de duração
- ✅ Tipos de passeio
- ✅ Requisitos

### **Usuários:**
- ✅ Lista de usuários
- ✅ Histórico de itinerários
- ✅ Estatísticas

### **Itinerários:**
- ✅ Lista completa
- ✅ Filtros avançados
- ✅ Visualização detalhada
- ✅ **Exportação em JSON**

---

## 🎨 **Design System:**
- **Cores:** Preto e branco (conforme solicitado)
- **Sidebar:** Escura com navegação moderna
- **Cards:** Coloridos com indicadores
- **Tabelas:** Responsivas com ações
- **Modais:** Elegantes para formulários
- **Mobile:** Totalmente responsivo

---

## 🆘 **Suporte:**

### **Problemas comuns:**
1. **Erro de dependências:** Execute `npm install --legacy-peer-deps`
2. **Porta ocupada:** Use `fuser -k 8000/tcp` e reinicie
3. **Firebase não conecta:** Verifique as credenciais no `.env.local`

### **Estrutura de arquivos:**
```
src/
├── app/
│   ├── admin/              # Páginas do painel
│   ├── layout.tsx          # Layout principal
│   └── page.tsx           # Página inicial
├── components/
│   ├── auth/              # Autenticação
│   ├── dashboard/         # Dashboard
│   ├── layout/            # Layout admin
│   └── ui/                # Componentes shadcn
├── contexts/              # Contextos React
├── services/              # Serviços Firebase
└── types/                 # Tipos TypeScript
```

---

## 🎯 **Próximos passos:**

1. **Teste o painel** no modo demo
2. **Configure Firebase** com suas credenciais
3. **Integre com seu app** MeGuia existente
4. **Customize** conforme necessário
5. **Deploy** em produção

---

**🎉 Painel Admin MeGuia - Pronto para uso!**

*Desenvolvido com ❤️ usando Next.js, TypeScript, TailwindCSS e Firebase*
