# RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS

**Data:** 26/12/2025  
**Empresa:** Abstergo Industries  
**Responsável:** Rodrigo Goulart de Moraes

---

## Introdução

Este relatório apresenta a implementação de serviços da Amazon Web Services (AWS) na Abstergo Industries, com objetivo de otimizar a infraestrutura de TI, reduzir custos operacionais, garantir escalabilidade e alta disponibilidade, e aumentar a eficiência das operações digitais da empresa.  

A adoção de soluções em nuvem permite maior flexibilidade, automação e segurança, atendendo às demandas de uma plataforma digital moderna e preparada para crescimento contínuo.

---

## Descrição da Implementação

A implementação foi estruturada em três etapas, cada uma dedicada a um serviço específico da AWS, com foco em resolver desafios operacionais e promover eficiência tecnológica.

### Etapa 1: Amazon Elastic Compute Cloud (EC2)

- **Foco:** Hospedagem e processamento da aplicação web  
- **Descrição detalhada:** O Amazon EC2 fornece capacidade de computação escalável na nuvem, permitindo criar instâncias virtuais de servidores sob demanda. Na Abstergo Industries, o EC2 foi utilizado para hospedar a aplicação web principal, garantindo:

  - **Flexibilidade de configuração:** Seleção de tipos de instâncias conforme CPU, memória e armazenamento necessário para cada workload.  
  - **Escalabilidade dinâmica:** Ajuste automático da capacidade computacional conforme o aumento ou diminuição de tráfego de usuários.  
  - **Redução de custos:** Evita provisionamento excessivo, pagando apenas pelos recursos utilizados.  
  - **Alta disponibilidade:** Integração com grupos de Auto Scaling e Elastic Load Balancing para distribuir carga e manter a aplicação sempre online.  

- **Serviços complementares utilizados:**  
  - Amazon CloudWatch para monitoramento de performance e alertas proativos  
  - Elastic Load Balancer (ELB) para balanceamento de tráfego  
  - Amazon VPC para isolamento seguro da rede

### Etapa 2: Amazon Relational Database Service (RDS)

- **Foco:** Gerenciamento de banco de dados relacional  
- **Descrição detalhada:** O Amazon RDS foi implementado para gerenciar os dados estruturados da plataforma, incluindo informações de clientes, pedidos, produtos e estoque. Benefícios observados:

  - **Automação de operações de banco de dados:** Incluindo backups automatizados, atualizações de segurança e manutenção.  
  - **Alta disponibilidade e tolerância a falhas:** Configuração Multi-AZ (disponibilidade em múltiplas zonas) para reduzir risco de downtime.  
  - **Escalabilidade vertical e horizontal:** Ajuste de capacidade de armazenamento e instância conforme necessidade, sem impacto na aplicação.  
  - **Segurança de dados:** Criptografia em repouso e em trânsito, gestão de acessos via AWS IAM e VPC Security Groups.  

- **Serviços complementares utilizados:**  
  - Amazon CloudWatch para métricas de desempenho do banco de dados  
  - Amazon RDS Performance Insights para análise de queries e otimização de performance  

### Etapa 3: Amazon Simple Storage Service (S3)

- **Foco:** Armazenamento de arquivos e conteúdos estáticos  
- **Descrição detalhada:** O Amazon S3 foi utilizado para armazenar arquivos estáticos da plataforma, incluindo imagens de produtos, documentos e materiais multimídia. Principais vantagens:  

  - **Alta durabilidade e disponibilidade:** Garantia de 99,999999999% de durabilidade e replicação entre regiões.  
  - **Custo otimizado:** Estrutura de armazenamento em camadas (Standard, Infrequent Access, Glacier) para reduzir despesas conforme frequência de acesso.  
  - **Escalabilidade ilimitada:** Capacidade de armazenamento praticamente infinita, sem necessidade de gerenciamento de infraestrutura física.  
  - **Integração com outros serviços AWS:** Facilita o uso em conjunto com CloudFront (CDN), Lambda (processamento de arquivos) e EC2.  

- **Serviços complementares utilizados:**  
  - Amazon S3 Versioning para controle de versões de arquivos  
  - Amazon S3 Lifecycle Policies para movimentação automática de arquivos entre classes de armazenamento  
  - Amazon CloudFront para distribuição global de conteúdo com baixa latência

---

## Benefícios Observados

A implementação dos serviços AWS trouxe impactos positivos significativos para a Abstergo Industries:

- Redução de custos operacionais devido à elasticidade e pagamento sob demanda  
- Garantia de alta disponibilidade e resiliência da aplicação  
- Melhoria na performance da plataforma web e bancos de dados  
- Maior segurança e confiabilidade dos dados armazenados  
- Capacidade de escalabilidade para suportar crescimento de usuários e volume de dados  
- Automação de tarefas operacionais, reduzindo esforço manual da equipe de TI  

---

## Diagramas da arquitetura da solução
```

                 ┌────────────────────┐
                 │     Usuários       │
                 │ (Web / Mobile)     │
                 └─────────┬──────────┘
                           │
                           ▼
                ┌─────────────────────┐
                │     Amazon EC2      │
                │   Aplicação Web     │
                └─────────┬───────────┘
                          │
          ┌───────────────┴───────────────┐
          │                               │
          ▼                               ▼
┌─────────────────────┐       ┌─────────────────────┐
│    Amazon RDS       │       │     Amazon S3       │
│ Banco de Dados      │       │ Arquivos Estáticos  │
│ (Clientes, Pedidos) │       │ (Imagens, Docs)     │
└─────────────────────┘       └─────────────────────┘
```

---

## Fontes

- [AWS Documentation – Amazon EC2](https://docs.aws.amazon.com/ec2/)
- [AWS Documentation – Amazon RDS](https://docs.aws.amazon.com/rds/)
- [AWS Documentation – Amazon S3](https://docs.aws.amazon.com/s3/)
- [AWS Well-Architected Framework](https://docs.aws.amazon.com/wellarchitected/)
- [Plataforma DIO – Desafio de Projeto AWS](https://www.dio.me/)



**Responsável pelo Projeto:** Rodrigo Goulart de Moraes
