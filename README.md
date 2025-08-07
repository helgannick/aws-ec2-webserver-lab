# 🖥️ Laboratório AWS EC2: Instalação de Servidor Web Apache

Este projeto foi desenvolvido durante o curso preparatório da certificação AWS Developer pela [Escola da Nuvem](https://escoladanuvem.org/), com o objetivo de aplicar na prática o uso do Amazon EC2 para deploy de servidores web e gestão de instâncias na nuvem.

## 🚀 Objetivos do laboratório

- Criar e configurar instância EC2 via AWS Console
- Instalar automaticamente o Apache HTTP Server usando User Data
- Liberar acesso HTTP via grupo de segurança
- Criar uma segunda instância via AWS CLI no CloudShell
- Encerrar e gerenciar instâncias manualmente

## 🛠️ Tecnologias e Ferramentas

- **AWS EC2**
- **AWS Console**
- **CloudShell + AWS CLI**
- **Amazon Linux 2**
- **Apache HTTP Server**

## 📸 Screenshots

### Página Web hospedada na instância EC2:
![apache online](./images/apache-test-page.jpeg)

### CloudShell com criação via CLI:
![cloudshell ec2](./images/ec2-cli-cloudshell.jpeg)

## 📦 User Data Script usado

```bash
#!/bin/bash
yum update -y
yum install -y httpd
systemctl start httpd
systemctl enable httpd
echo "<h1>Testando o Apache!</h1><p>Servidor funcionando corretamente!</p>" > /var/www/html/index.html

Esse script automatiza a instalação e inicialização do Apache ao criar a instância.
```

### 🧠 Aprendizados
Como iniciar instâncias EC2 com scripts automatizados (User Data)

Importância do controle de segurança via grupos de segurança

Gerenciamento prático de instâncias via interface e CLI

Diferença entre provisionamento manual e automatizado

### 📌 Conclusão
Esse laboratório reforça como a combinação entre a interface gráfica e linha de comando (CLI) na AWS permite agilidade e controle sobre a infraestrutura em nuvem.

### 📚 Créditos
Projeto realizado como parte do programa AWS Developer - Escola da Nuvem.
