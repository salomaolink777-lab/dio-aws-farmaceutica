# Relatório de Arquitetura Cloud - Operação Farmacêutica

**Desenvolvedor:** Salomão
**Objetivo:** Implementar uma infraestrutura robusta para uma rede farmacêutica nacional.

## 1. Estratégia de Rede e Segurança
- **VPC:** Dividida em sub-redes públicas (para o Load Balancer e Bastion Host) e privadas (para servidores de aplicação e bancos de dados).
- **Segurança:** Utilização de **Security Groups** (Stateful) para proteger as instâncias e **Network ACLs** (Stateless) para controle rígido no nível de sub-rede.

## 2. Camada de Aplicação (PaaS e IaaS)
- **Elastic Beanstalk:** Utilizado para o deploy rápido das APIs de pedidos, permitindo que os desenvolvedores foquem no código enquanto a AWS gerencia a infraestrutura.
- **Auto Scaling:** Configurado em modo **Preditivo**, antecipando o aumento de tráfego nos horários de pico de vendas.
- **Fargate:** Utilizado para tarefas de processamento de dados em segundo plano (Serverless), otimizando custos.

## 3. Armazenamento e Bancos de Dados
- **S3 (Intelligent-Tiering):** Armazenamento de receitas digitais e documentos legais, otimizando custos automaticamente conforme o padrão de acesso.
- **DynamoDB com DAX:** Utilizado para o catálogo de produtos e cache de consultas, garantindo que o tempo de resposta seja de microssegundos.
- **EBS (st1):** Para o processamento de logs de transações e data warehouse analítico.

## 4. Conclusão
A arquitetura foi desenhada para ser **Regional**, utilizando múltiplas Zonas de Disponibilidade (Multi-AZ) para garantir que, caso uma zona falhe, a operação farmacêutica continue operando sem perda de dados ou downtime.
