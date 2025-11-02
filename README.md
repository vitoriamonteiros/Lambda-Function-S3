# Projeto AWS: Lambda Function e S3 Automatizados

Neste projeto, apliquei conceitos de automação de infraestrutura na AWS utilizando CloudFormation, Lambda Functions e Amazon S3. O objetivo foi criar e gerenciar recursos em nuvem de forma automatizada, simulando um fluxo real de processamento de arquivos enviados a um bucket S3.

## Recursos Criados
- **Bucket S3**: Armazena arquivos enviados pelo usuário.
- **Lambda Function**: Acionada automaticamente quando um objeto é criado no bucket S3.
- **CloudFormation Stack**: Provisiona a infraestrutura completa de forma automatizada, incluindo o bucket S3 e a Lambda Function.
- **IAM Role**: Permissões necessárias para a Lambda Function acessar o bucket S3.

## Objetivo do Projeto
Automatizar tarefas simples de processamento de arquivos, aplicando conceitos de infraestrutura como código (IaC), padronização e segurança na nuvem. Este projeto demonstra como é possível criar fluxos automatizados com Lambda e S3 sem intervenção manual.

## Como Funciona
1. Um arquivo é enviado para o bucket S3.
2. O evento de criação do objeto aciona automaticamente a Lambda Function.
3. A Lambda Function processa o arquivo conforme a lógica definida (ex: renomear, registrar logs, enviar notificação, etc.).
4. Todos os recursos foram provisionados via CloudFormation, garantindo replicabilidade e versionamento da infraestrutura.

## Como Testar
- Criar ou atualizar a stack via CloudFormation utilizando o template `template.yaml` ou `template.json`.
- Enviar um arquivo para o bucket S3.
- Verificar nos logs do CloudWatch se a Lambda Function foi acionada e executou a ação esperada.

--

## Aprendizados
- Criação e gerenciamento de recursos AWS via **CloudFormation**.
- Automação de tarefas usando **AWS Lambda**.
- Integração de eventos **S3 → Lambda** para processamento automático de arquivos.
- Configuração de permissões seguras usando **IAM Roles**.
- Aplicação de boas práticas de infraestrutura como código (IaC).
