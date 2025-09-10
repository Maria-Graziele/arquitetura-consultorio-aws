# 🦷 Arquitetura AWS – Consultório Odontológico

## 📌 Descrição
Este projeto representa uma arquitetura em nuvem utilizando *Amazon Web Services (AWS)* para simular o ambiente de um *consultório odontológico*.  
O objetivo é integrar diferentes serviços da AWS (*S3, EC2 e Lambda*) para hospedar aplicações, armazenar imagens de pacientes (como radiografias e fotos) e automatizar tarefas comuns no consultório.

---

## 🏗 Arquitetura

A arquitetura é composta pelos seguintes componentes:

### ☁ Amazon S3
- Utilizado para *armazenamento de imagens* dos pacientes (radiografias, fotos etc.).  
- Hospeda um *site estático* com informações acessíveis.  
- Possibilidade de aplicar *marca d’água* para segurança das imagens.  

### 🖥 Amazon EC2
- Instância EC2 responsável pelo *backend principal da aplicação* do consultório.  
- Conecta-se com a *rede interna do consultório*, permitindo que funcionários acessem o sistema.  
- Faz a integração dos dados vindos do S3 e do Lambda.  

### ⚡ AWS Lambda
- Responsável por *tarefas automatizadas*, como:  
  - Processamento de imagens (redimensionamento, compressão).  
  - Envio de notificações automáticas, como *e-mails de lembrete de consultas*.  
- Funciona em modo *serverless*, reduzindo custos, já que só executa quando necessário.  

### 🏢 Rede Interna do Consultório
- Permite que a equipe interna (dentistas, recepcionistas e assistentes) acesse o sistema e os dados dos pacientes de forma segura.  

---

## 🔄 Fluxo de Funcionamento
1. O paciente realiza upload de imagens ou cadastro de informações.  
2. Os dados são armazenados no *Amazon S3*.  
3. O *AWS Lambda* é acionado para processar imagens ou enviar notificações de agendamento.  
4. O *Amazon EC2* centraliza o backend e disponibiliza os dados para a *rede interna* do consultório.  
5. A equipe do consultório acessa o sistema internamente para gerenciar consultas, pacientes e imagens.  

---

## 🎯 Benefícios da Arquitetura
- *Escalabilidade:* adapta-se ao crescimento da clínica.  
- *Automação:* tarefas repetitivas são realizadas de forma automática.  
- *Segurança:* armazenamento confiável e redundante no S3.  
- *Flexibilidade:* integração entre serviços e acesso interno e público.  

---

## 📊 Diagrama da Arquitetura
![Diagrama AWS](./images/arquitetura.png)

---

## 👩‍💻 Autor
Projeto desenvolvido como parte de prática no *Bootcamp AWS*, para consolidar conhecimentos em:  
- *Amazon S3*  
- *Amazon EC2*  
- *AWS Lambda*  
- *Documentação no GitHub*
