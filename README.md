# Gerador de Certificados

Este é um projeto de gerador de certificados desenvolvido em PHP, JavaScript, HTML e CSS, com o uso do framework Bootstrap para o design da página. Ele permite gerar certificados tanto individualmente quanto em massa para eventos.

## Tecnologias Utilizadas

- PHP 8.2.9
- Servidor XAMPP.
- Composer para PHP.
- Biblioteca mPDF para geração de certificados a partir das informações fornecidas no formulário HTML.
- PHPMailer para envio de certificados por e-mail.
- Banco de dados MySQL para armazenamento dos registros de login e codigos de autenticação unicos dos certificados.


## Funcionalidades

- **Gerador de Certificados Individuais**: Permite gerar certificados personalizados para cada participante do evento.
- **Gerador de Certificados em Massa**: Facilita a geração de certificados para todos os participantes do evento de uma só vez.
- **Envio de Certificados por E-mail**: Possibilita o envio automático de certificados por e-mail aos participantes.
- **Geração de Certificados a partir de Arquivos CSV**: Permite gerar certificados em massa a partir de informações contidas em arquivos CSV.
- - **Armazenamento em Banco de Dados**: Registra os dados dos participantes em um banco de dados MySQL.
- **Design Responsivo**: Utiliza o framework Bootstrap para garantir um design responsivo e amigável para dispositivos móveis.

## Pré-requisitos

Antes de começar, certifique-se de ter os seguintes requisitos instalados em sua máquina:

- PHP 8.2.9
- Servidor XAMPP ou similar
- Composer para PHP
- Navegador Web moderno
- Banco de dados MySQL



## Instalação

1. Clone este repositório para o seu ambiente local:https://github.com/bruno-alves15/GERADORCERTIFICADOPHP
2. Navegue até o diretório do projeto:
3. Instale o PHPMailer via Composer: composer require mpdf/mpdf
4. Instale o PHPMailer via Composer: composer require phpmailer/phpmailer
5. Crie um banco de dados para o nome de registros de login no sistema com a seguinte instrução:

    CREATE DATABASE sislogin; após
   
    CREATE TABLE usuarios com a seguinte estrutura:
   
| Campo   | Tipo         | Restrições       |
|---------|--------------|------------------|
| id      | INT(10)      | UNSIGNED, NOT NULL, AUTO_INCREMENT |
| nome    | VARCHAR(255) | COLLATE utf8mb4_general_ci, NOT NULL |
| usuario | VARCHAR(255) | COLLATE utf8mb4_general_ci, NOT NULL |
| email   | VARCHAR(255) | COLLATE utf8mb4_general_ci, NOT NULL |
| senha   | VARCHAR(45)  | COLLATE utf8mb4_general_ci, NOT NULL |
| tipo    | INT(11)      | NOT NULL         |
| data    | DATE         | NOT NULL         |

6. Crie tambem o banco de dados para a parte de codigos de  autenticação unicos dos certificados com a seguinte instrução:


      CREATE DATABASE codigo_autenticacao; após
   
    CREATE TABLE codigos_autenticacao com a seguinte estrutura:

| Campo   | Tipo         | Restrições       |
|---------|--------------|------------------|
| id      | INT(11)      | PRIMARY KEY, NOT NULL, AUTO_INCREMENT |
| codigo  | VARCHAR(255) | COLLATE utf8mb4_general_ci, NOT NULL |
| usado   | TINYINT(1)   | NOT NULL, DEFAULT 0 |

7. Certifique-se de ter o servidor XAMPP ou similar iniciado e o banco de dados MySQL configurado.
8. Abra o navegador web e acesse : http://localhost/GERADORCERTIFICADOPHP/PROJETO_CERTIFICADOPHP/index.php

   ## Uso

1. Na página inicial, você terá a opção de "Gerar Certificado Individual" ou "Gerar Certificados em Lote".
2. Selecione a opção desejada e siga as instruções na tela para fornecer as informações necessárias.
3. Após preencher os dados, clique no botão "Gerar Certificado" para obter o certificado.



   







   






