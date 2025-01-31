# CoworkBook

## **Sistema de Gestão de Reservas para Coworking**  

### 🔹 **Objetivo:**  
Criar um sistema onde usuários possam reservar salas de reunião ou espaços de trabalho em um coworking, com gerenciamento de disponibilidade, pagamentos (opcional) e controle administrativo.  

---

### 📌 **Tecnologias:**  
- **Back-end:** PHP (com MySQL para armazenar dados)  
- **Front-end:** TypeScript + Bootstrap  
- **Banco de Dados:** MySQL (ou MariaDB)  
- **Autenticação:** Login com JWT ou PHP Sessions  
- **API:** Criar uma API REST em PHP para gerenciar reservas e usuários  

---

### 🎯 **Funcionalidades Principais:**  

✅ **Usuário Comum:**  
- Cadastro/Login  
- Visualização de horários disponíveis  
- Reserva de espaços (com limite de tempo e capacidade)  
- Histórico de reservas  

✅ **Administrador:**  
- Gerenciamento de usuários  
- Controle de reservas (aprovar, cancelar, bloquear horários)  
- Relatórios de ocupação e receita  

✅ **Extras (Se Quiser Inovar 💡):**  
- Envio de e-mails de confirmação (usando PHPMailer)  
- Integração com um gateway de pagamento (ex: MercadoPago)  
- Dashboard com gráficos de ocupação (usando Chart.js)  
- Notificações em tempo real (com WebSockets)  

Aqui está uma estrutura bem organizada para o **WorkSpace Manager**, usando **PHP, TypeScript e Bootstrap**, separando bem back-end e front-end para facilitar manutenção e escalabilidade.  

---

### 📂 **Estrutura de Diretórios**
```
CoworkBook/
│── backend/                       # Código do back-end em PHP
│   ├── config/                    # Configurações do banco de dados
│   │   ├── database.php           # Conexão com MySQL
│   ├── controllers/               # Lógica da aplicação (CRUD)
│   │   ├── AuthController.php     # Login e autenticação
│   │   ├── BookingController.php  # Gerenciamento de reservas
│   │   ├── UserController.php     # Gerenciamento de usuários
│   ├── models/                    # Modelos representando tabelas do BD
│   │   ├── User.php
│   │   ├── Booking.php
│   ├── routes/                    # Rotas da API REST
│   │   ├── api.php                # Endpoints da aplicação
│   ├── middleware/                # Autenticação e segurança
│   │   ├── AuthMiddleware.php
│   ├── utils/                     # Funções auxiliares
│   │   ├── helpers.php            # Envio de e-mails, logs, etc.
│   ├── public/                    # Arquivos acessíveis pela web
│   │   ├── index.php              # Entrada principal da API
│── frontend/                      # Código do front-end em TypeScript e Bootstrap
│   ├── src/                       # Código principal
│   │   ├── assets/                # Imagens, ícones e fontes
│   │   ├── components/            # Componentes reutilizáveis (NavBar, Cards, etc.)
│   │   ├── pages/                 # Páginas (Home, Login, Reservas, Admin)
│   │   ├── services/              # Comunicação com API
│   │   │   ├── api.ts             # Configuração da API (fetch, axios)
│   │   │   ├── auth.ts            # Funções de autenticação
│   │   │   ├── booking.ts         # Funções de reservas
│   │   ├── styles/                # CSS customizado com Bootstrap
│   ├── index.html                 # Página principal
│   ├── main.ts                    # Entrada do TypeScript
│── database/                      # Scripts SQL
│   ├── schema.sql                 # Estrutura das tabelas
│── .env                           # Variáveis de ambiente (DB, JWT, etc.)
│── package.json                   # Dependências do front-end
│── composer.json                  # Dependências do back-end PHP
│── README.md                      # Documentação do projeto
```

---

Esse projeto é versátil, dá pra usar em escritórios, coworkings, academias, etc. 🚀
