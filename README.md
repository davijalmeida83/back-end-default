# Recuperação de senha

**RF**

- O usuário deve poder recuperar sua senha informando o seu e-mail;
- O usuário deve receber um e-mmail com instruções de recuperação de senha;
- O usuário deve poder resetar a sua senha;

**RNF**

- Utilizar Mailtrap para testar envios em ambiente de dev;
- Utilizar o Amazon SES para envios de e-mail em produção;
- O envio de e-mails devem acontecer em segundo plano(background job);

**RN**

- O link enviado por e-mail para resetar a senha de usuário, deve experiar em 2h;
- O usuário precisa confirmar a nova senha ao resetar sua senha;



# Atualização do perfil

**RF**

- O usuário deve poder atualizar o seu nome, e-mail e senha.

**RNF**

**RN**

- O usuário não pode alterar o seu e-mail para um e-mail já utilizado;
- Para atualizar a sua senha, o usuário deve informar a senha antiga;
- Para atualizar a sua senha, o usuário deve confirmar a nova senha;

# Painel do prestador

**RF**

- O Usuário deve poder listar os seus agendamentos de um dia específico;
- O prestador deve receber uma notificação, sempre que houver um novo agendamento;
- O prestador deve poder visualizar as notificações não lidas;

**RNF**

- Os agendamentos do prestador no dia devem ser armazenados em cache;
- As nofiticações do prestador devem ser armazenadas no Mongo DB;
- As notificações do prestador devem ser enviadas em tempo real utilizando socket.io;

**RN**

- A notificação deve conter um status de Lida ou Não Lida, para que o prestador possa controlar;



# Agendamento de serviços

**RF**

- O usuário deve poder listar todos os prestadores de serviços cadastrados;
- O usuário deve poder listar os dias de um mês com pelo menos 1 horário disponível de um prestador;
- O usuário deve poder listar horários disponiveis de um dia específico de um prestador;
- O usuário deve poder realizar um novo agendamento com um prestador;

**RNF**

- A listagem de prestadores devem ser armazenadas em cache;

**RN**

- Cada agendamento deve durar 1h exatamente;
- Os agendamentos devem estar disponíveis entre 8h às 18h (Primeito horário às 8h, ultimo às 17h);
- O usuário não pode agendar em um horário já ocupado;
- O usuário não pode agendar em um horário que já passou;
- O usuário não pode agendar serviços consigo mesmo;


