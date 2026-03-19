# 💊 Cloud Health: Arquitetura de Operação Farmacêutica na AWS

Este repositório contém a proposta de arquitetura de nuvem para o desafio de projeto da DIO: "Missão - Operação Farmacêutica". O foco é criar uma infraestrutura resiliente, segura e escalável para gerenciar dados críticos de saúde.

## 🚀 Desafio
Construir uma solução que suporte:
- Alta disponibilidade de APIs.
- Armazenamento seguro de registros médicos e farmacêuticos.
- Monitoramento em tempo real (focado em resiliência de rede).

## 🛠️ Tecnologias Utilizadas
- **Computação:** Amazon EC2 com Auto Scaling e AWS Fargate.
- **Armazenamento:** Amazon S3 (Imagens/Documentos) e Amazon EBS (Volumes de sistema).
- **Banco de Dados:** Amazon RDS (Dados Relacionais) e DynamoDB (Logs de acesso).
- **Segurança:** Security Groups e Network ACLs.
- **Rede:** Amazon VPC com Sub-redes Públicas e Privadas.

## 📈 Diferencial Técnico
Como especialista em monitoramento de redes no setor público, integrei conceitos de **Soberania de Dados** e **Multi-AZ** para garantir que a operação farmacêutica esteja em conformidade com leis locais (LGPD) e nunca sofra interrupções.
