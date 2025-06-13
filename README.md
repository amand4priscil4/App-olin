# App Olin - Sistema de Gestão de Casos Periciais


> Aplicativo móvel completo para gestão de casos periciais, desenvolvido em React Native com integração a API Node.js e MongoDB.

## Sobre o Projeto

O **App Olin** é uma solução mobile completa para profissionais da perícia forense, permitindo o gerenciamento eficiente de casos periciais, evidências, relatórios e informações de vítimas. O aplicativo oferece uma interface intuitiva e funcionalidades avançadas como geolocalização automática, upload de arquivos e integração com IA para geração de relatórios.

### Principais Funcionalidades

- **Gestão de Casos**: Criação, visualização e edição de casos periciais
- **Controle de Evidências**: Upload de fotos e documentos com metadados
- **Cadastro de Vítimas**: Informações detalhadas incluindo dados odontológicos
- **Relatórios Inteligentes**: Geração baseada nos dados do caso
- **Geolocalização**: Captura automática de coordenadas para evidências
- **Autenticação JWT**: Sistema seguro de login e controle de acesso
- **Interface Responsiva**: Design otimizado para dispositivos móveis
- **Sincronização**: Dados sincronizados em tempo real com o backend

## Tecnologias Utilizadas

### Frontend (Mobile)
- **React Native** - Framework para desenvolvimento mobile
- **Expo** - Plataforma de desenvolvimento
- **React Navigation** - Navegação entre telas
- **Axios** - Cliente HTTP para API
- **AsyncStorage** - Armazenamento local
- **Expo Location** - Serviços de geolocalização
- **Expo ImagePicker** - Captura de imagens
- **React Native Screens Swiper** - Componente de tabs

### Backend
- **Node.js** - Runtime JavaScript
- **Express** - Framework web
- **MongoDB Atlas** - Banco de dados NoSQL
- **Mongoose** - ODM para MongoDB
- **JWT** - Autenticação
- **Multer** - Upload de arquivos
- **Bcrypt** - Criptografia de senhas

## Estrutura do Projeto

```
app-olin/
├── components/
│   ├── forms/
│   │   ├── new-case-modal.js
│   │   ├── new-evidence-modal.js
│   │   ├── new-relatorio-modal.js
│   │   └── modal-nova-vitima.js
│   ├── lists/
│   │   ├── list-evidencias.js
│   │   ├── list-relatorios.js
│   │   └── list-vitimas.js
│   └── auth-context.js
├── screens/
│   ├── cases/
│   │   ├── case-list.js
│   │   └── case-details.js
│   ├── auth/
│   │   └── login.js
│   └── dashboard.js
├── constants/
│   └── colors.js
└── app.json
```

## Instalação e Configuração

### Pré-requisitos

- Node.js 18+
- npm ou yarn
- Expo CLI
- Dispositivo móvel ou emulador

### Instalação

1. Clone o repositório:
```bash
git clone https://github.com/amand4priscil4/App-olin.git
cd App-olin
```

2. Instale as dependências:
```bash
npm install
# ou
yarn install
```

3. Configure as variáveis de ambiente:
```bash
# Crie um arquivo .env na raiz do projeto
API_URL=https://case-api-icfc.onrender.com
```

4. Inicie o aplicativo:
```bash
expo start
```

## Como Usar

### 1. Login
- Entre com suas credenciais de perito ou administrador
- O sistema utiliza autenticação JWT para segurança

### 2. Gerenciar Casos
- **Criar Caso**: Toque no botão "+" para adicionar um novo caso
- **Visualizar**: Selecione um caso da lista para ver detalhes
- **Editar**: Modifique informações do caso (conforme permissões)

### 3. Adicionar Evidências
- Acesse a aba "Evidências" dentro de um caso
- Toque em "+" para adicionar nova evidência
- Escolha entre foto (câmera/galeria) ou documento
- A localização é capturada automaticamente

### 4. Cadastrar Vítimas
- Na aba "Vítimas", adicione informações da vítima
- Preencha dados pessoais, documento e observações
- O odontograma é inicializado automaticamente

### 5. Gerar Relatórios
- Acesse "Relatórios" e escolha o tipo:
  - Laudo de Evidência
  - Laudo Odontológico
  - Relatório Final

## Funcionalidades Avançadas

### Geolocalização Automática
- Captura coordenadas GPS para evidências
- Geocoding reverso para endereços
- Integração com mapas

### Upload de Arquivos
- Suporte a imagens (JPEG, PNG)
- Documentos PDF
- Compressão automática
- Validação de tipos

### Relatórios com IA
- Geração automática baseada nos dados do caso
- Análise de evidências e informações das vítimas
- Possibilidade de edição antes do salvamento

## API Endpoints

### Autenticação
- `POST /api/login` - Login de usuário
- `GET /api/protegido` - Verificar token

### Casos
- `GET /api/casos` - Listar casos
- `POST /api/casos` - Criar caso
- `GET /api/casos/:id` - Buscar caso por ID
- `PUT /api/casos/:id` - Atualizar caso

### Evidências
- `GET /api/evidencias` - Listar evidências
- `POST /api/evidencias` - Criar evidência
- `GET /api/evidencias/:id` - Buscar evidência

### Vítimas
- `GET /api/vitimas/caso/:casoId` - Listar vítimas por caso
- `POST /api/vitimas` - Criar vítima
- `GET /api/vitimas/:id` - Buscar vítima

### Relatórios
- `POST /api/laudos` - Criar laudo de evidência
- `POST /api/laudos-odontologicos/:vitimaId` - Criar laudo odontológico
- `POST /api/relatorios/:casoId` - Criar relatório final

## Contribuição

1. Faça o fork do projeto
2. Crie uma branch para sua feature (`git checkout -b feature/nova-feature`)
3. Commit suas mudanças (`git commit -m 'Adiciona nova feature'`)
4. Push para a branch (`git push origin feature/nova-feature`)
5. Abra um Pull Request

## Licença

Este projeto está licenciado sob a Licença MIT - veja o arquivo [LICENSE](LICENSE) para detalhes.

## Contato

**Desenvolvedor**: Amanda Priscila  
**Email**: amandapriscilaa15@gmail.com  
**GitHub**: [@amand4priscil4](https://github.com/amand4priscil4)

---

**App Olin** - Transformando a gestão de casos periciais através da tecnologia
