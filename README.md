-----

# Desafio DIO: Entendendo o Monitoramento de Máquinas Virtuais no Azure (Conceitual)

-----

Este repositório foi criado como parte do desafio "Entendendo Desafio" da DIO. Embora eu não tenha acesso a uma conta Azure ativa para realizar as configurações na prática, este material demonstra minha compreensão profunda dos conceitos de monitoramento de Máquinas Virtuais (VMs) no Microsoft Azure, com base nas vídeo-aulas da plataforma DIO e na documentação oficial da Microsoft.

-----

## Objetivos de Aprendizagem Demonstrados

Ao longo deste material, busco demonstrar minha capacidade de:

  * Compreender os conceitos de monitoramento de recursos no Azure.
  * Entender como configurar o monitoramento para Máquinas Virtuais.
  * Saber como criar alertas para eventos críticos, como a exclusão de uma VM.
  * Documentar processos técnicos de forma clara e estruturada.
  * Utilizar o GitHub para compartilhar documentação técnica.

-----

## O que é Monitoramento no Azure?

Explique aqui, com suas palavras, o que significa monitorar recursos no Azure. Fale sobre:

  * **Visibilidade e Controle:** Por que é importante saber o que está acontecendo com seus recursos.
  * **Identificação de Problemas:** Como o monitoramento ajuda a detectar falhas, gargalos de desempenho, etc.
  * **Resposta Proativa:** Como os alertas permitem agir antes que pequenos problemas se tornem grandes.

-----

## Componentes Essenciais do Monitoramento de VMs

Descreva os principais elementos que você aprendeu para monitorar uma VM:

  * ### Métricas:

      * O que são? (Ex: CPU, memória, I/O de disco, tráfego de rede).
      * Onde seriam visualizadas no Portal do Azure?
      * Qual a importância de monitorá-las?

  * ### Logs (Log de Atividades e Logs de Diagnóstico):

      * **Log de Atividades:** Explique o que ele registra (ações de gerenciamento como criar, parar, excluir recursos). **Este é crucial para o alerta de exclusão de VM.**
      * **Logs de Diagnóstico:** O que eles coletam? (Ex: logs do sistema operacional, logs de desempenho).
      * Como eles complementam o monitoramento de métricas?

  * ### Alertas:

      * O que são e por que são usados? (Notificações automáticas quando uma condição é atendida).
      * Como eles são configurados (condição, ação, escopo)?

-----

## Simulação: Como Configurar o Monitoramento de uma VM (Conceitual)

Nesta seção, **descreva passo a passo como você faria as configurações**, imaginando que estivesse no Portal do Azure. Seja detalhado, como se estivesse dando um tutorial para alguém.

1.  ### Criação de uma Máquina Virtual (VM) para Monitoramento (Simulado):

      * Descreva os passos básicos que você seguiria para criar uma VM (selecionar assinatura, grupo de recursos, nome, região, imagem, tamanho, credenciais).
      * Mencione a importância de escolher um tamanho **gratuito ou de baixo custo** para quem usa a conta gratuita.

2.  ### Ativando as Configurações de Diagnóstico da VM:

      * Descreva onde ir no Portal do Azure (na VM, seção "Monitoramento" -\> "Configurações de diagnóstico").
      * Explique o que você ativaria (Métricas e Logs) e onde os dados seriam enviados (conta de armazenamento ou Log Analytics Workspace).

3.  ### Configurando um Alerta para Alta Utilização da CPU (Exemplo de Métrica):

      * Descreva como você navegaria para "Alertas" e "Criar regra de alerta".
      * Explique a **condição** (métrica "Porcentagem da CPU", limite, período de avaliação).
      * Explique as **ações** (grupo de ações, tipo de notificação como e-mail).

4.  ### Configurando um Alerta para Exclusão de VM (Crucial para o Desafio\!):

      * **Este é o ponto mais importante.** Explique detalhadamente:
          * Como navegaria até "Monitor" -\> "Alertas" -\> "Criar regra de alerta".
          * Como definiria o **Escopo** (assinatura ou grupo de recursos).
          * Como selecionaria o **Tipo de Sinal** como **"Log de Atividades"**.
          * Como filtraria o **Nome da Operação** para encontrar "Excluir Máquina Virtual (Microsoft.Compute/virtualMachines/delete)".
          * Como configuraria as **Ações** para receber uma notificação de e-mail.
          * Mencione a importância de testar esse alerta com uma VM de teste.

-----

## Aprendizados e Reflexões

  * Compartilhe o que você mais aprendeu sobre monitoramento no Azure.
  * Quais seriam os desafios de implementar isso na prática (custos, complexidade, etc.)?
  * Como o monitoramento ajuda na segurança e na otimização de custos?

-----

## Dicas e Boas Práticas (Conceituais)

  * O que você recomendaria para alguém que vai configurar monitoramento de VMs?
  * A importância de documentar os alertas.

-----

## Recursos Utilizados

  * **Plataforma DIO:** [Link para a DIO, se quiser]
  * **Microsoft Learn - Configurar o monitoramento de máquinas virtuais:** [Link para a documentação oficial: `https://learn.microsoft.com/pt-br/azure/azure-monitor/vm/monitor-vm-quickstart`]([https://learn.microsoft.com/pt-br/azure/azure-monitor/vm/monitor-vm-quickstart]\(https://learn.microsoft.com/pt-br/azure/azure-monitor/vm/monitor-vm-quickstart\))
  * **Documentação GitHub para Markdown:** [Link, se você usou: `https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax`]([https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax]\(https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax\))
