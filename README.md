

#  Implementação de Stack com AWS CloudFormation

Projeto desenvolvido durante o curso **Computação em Nuvem com AWS** da **DIO (Digital Innovation One)** em parceria com o **Santander Code Girls - 2025**.

---

##  Sobre o Projeto

Este projeto teve como objetivo compreender o funcionamento do **AWS CloudFormation**, um serviço que permite **criar e gerenciar recursos da AWS de forma automatizada** por meio de modelos (templates) em formato YAML ou JSON.

A proposta foi realizar a **implementação de uma Stack** (pilha de recursos) utilizando um template CloudFormation, automatizando a criação da infraestrutura e reduzindo o esforço manual de configuração.

---

##  O que é o AWS CloudFormation

O **AWS CloudFormation** é um serviço que permite **definir, provisionar e gerenciar recursos da AWS como código (IaC — Infrastructure as Code)**.  
Com ele, é possível criar **modelos declarativos** que descrevem toda a infraestrutura necessária para um ambiente, garantindo **padronização, repetibilidade e controle de versões**.

Em resumo, ele transforma a criação de recursos na nuvem — como instâncias EC2, buckets S3, bancos de dados e funções Lambda — em um processo totalmente automatizado.

---

##  Benefícios do CloudFormation

-  **Automatização total** da criação e configuração de recursos.  
-  **Reprodutibilidade:** fácil replicar ambientes de forma consistente.  
-  **Controle como código:** versionamento de templates em repositórios Git.  
-  **Otimização de custos:** evita criação manual e duplicada de recursos.  
-  **Gerenciamento simplificado:** facilita atualizações e exclusões de pilhas.

---

##  Serviços Utilizados

- **AWS CloudFormation** – Criação e gerenciamento das Stacks.  
- **Amazon S3** – Armazenamento de templates e logs de execução.  
- **Amazon EC2 (opcional)** – Instância criada via template.  
- **IAM** – Permissões de acesso necessárias para execução do CloudFormation.  

---

##  Passo a Passo: Criando uma Stack no AWS CloudFormation

Abaixo está um passo a passo simples para criar sua primeira Stack.  


###  1. Acessar o serviço
- No console da AWS, procure por **CloudFormation** e clique no serviço.
  <img width="864" height="334" alt="image" src="https://github.com/user-attachments/assets/df18f639-26c5-411f-9859-814ee41ada5c" />


###  2. Criar uma nova Stack
- Clique em **Create stack** → **With new resources (standard)**.  
- Escolha como deseja fornecer o template:
  - **Template pronto no S3**, ou  
  - **Upload de arquivo local (YAML ou JSON)**.


###  3. Carregar o template
- Faça upload de um arquivo **.yaml** ou **.json** que descreva sua infraestrutura.  
  Exemplo simples de template YAML:

  ```yaml
  AWSTemplateFormatVersion: '2010-09-09'
  Description: Criação de um bucket S3 de exemplo
  Resources:
    MeuBucketS3:
      Type: AWS::S3::Bucket
      Properties:
        BucketName: meu-bucket-exemplo-cloudformation
  ```

<img width="1526" height="694" alt="image" src="https://github.com/user-attachments/assets/cd24cc61-3acd-4996-8ac7-f3f0be0edcc2" />

### 4. Configurar detalhes da Stack

* Defina um nome para sua Stack (ex: `MinhaPrimeiraStack`).
* Preencha parâmetros (se houver) e avance.

<img width="1550" height="481" alt="image" src="https://github.com/user-attachments/assets/97dd44a5-21c9-4a50-841e-0a05b9c34257" />


###  5. Revisar e criar

* Verifique as configurações.
* Marque a opção de **acknowledgement** (confirmação de permissões).
* Clique em **Create stack**.

<img width="1527" height="717" alt="image" src="https://github.com/user-attachments/assets/cecfc9ab-137d-4ad4-bad7-9e3d6bc97c3c" />


###  6. Acompanhar a criação

* Acompanhe o status da Stack em tempo real na aba **Events**.
* Quando o status aparecer como **CREATE_COMPLETE**, sua infraestrutura estará pronta.

<img width="1367" height="352" alt="image" src="https://github.com/user-attachments/assets/3c94e152-10a4-43e4-ac2b-8c8d463296d7" />


###  7. (Opcional) Deletar a Stack

* Para remover todos os recursos criados automaticamente:

  * Selecione a Stack → **Delete** → **Confirmar exclusão**.

<img width="1876" height="495" alt="image" src="https://github.com/user-attachments/assets/930d0916-e0d4-463b-8317-d0899959e942" />


---

## Insights Aprendidos

Durante a prática com o CloudFormation, foi possível compreender:

* Como o **conceito de Infrastructure as Code** facilita a automação e consistência dos ambientes.
* Que as **Stacks** funcionam como agrupamentos lógicos de recursos, simplificando o controle.
* A importância de **validar templates** antes da execução para evitar falhas.
* Como **variáveis e parâmetros** tornam os templates reutilizáveis.

---

## Conclusão

O **AWS CloudFormation** é uma ferramenta poderosa para profissionais de cloud e desenvolvedores que desejam **automatizar a infraestrutura de forma escalável e controlada**.
Com ele, é possível construir ambientes complexos de forma simples, segura e totalmente versionável.

