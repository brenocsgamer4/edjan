# PROJETO DE REDE ESTRUTURADA PARA O PAVILHÃO LUIS VIANA

**Instituição:** Centro Territorial de Educação Profissional do Litoral Norte e Agreste Baiano

**Projeto:** Rede Estruturada para o Pavilhão Luis Viana

**Equipe:** Breno Almeida, Octavio Rick, Misael Mateus, Alailson Santana

**Orientador:** Edjan 

**Turma:** 3TIM4

**Local:** Alagoinhas, 2025

---

## Sumário

1. [Identificação do Projeto](#1-identificação-do-projeto)
2. [Introdução](#2-introdução)
3. [Análise de Requisitos](#3-análise-de-requisitos)
4. [Escolha do Provedor de Internet](#4-escolha-do-provedor-de-internet)
5. [Equipamentos Necessários](#5-equipamentos-necessários)
6. [Topologia da Rede](#6-topologia-da-rede)
7. [Cabeamento Estruturado](#7-cabeamento-estruturado)
8. [Planejamento de Endereçamento IP](#8-planejamento-de-endereçamento-ip)
9. [Segurança da Rede](#9-segurança-da-rede)
10. [Conclusão](#10-conclusão)
11. [Referências](#11-referências)

---

### 1. Identificação do Projeto

*   **Nome da equipe:** Equipe 3
*   **Integrantes:** Octavio Rick,Breno Almeida, Misael Mateus, Alailson Santana
*   **Turma:** 3TIM4
*   **Título do projeto:** Projeto de Rede Estruturada para o Pavilhão Luis Viana

### 2. Introdução

Este projeto visa resolver a ausência de uma infraestrutura de rede de computadores centralizada, segura e eficiente no pavilhão escolar, conforme a planta baixa fornecida. A implementação de uma rede estruturada é fundamental para modernizar o ambiente educacional, garantindo que alunos, professores e funcionários administrativos tenham acesso rápido e confiável a recursos digitais, sistemas acadêmicos e à internet.

A finalidade da rede é interconectar todos os ambientes, incluindo laboratórios, salas administrativas, sala de recursos e sala multimídia, além de prover cobertura Wi-Fi para áreas comuns, suportando acesso à internet, compartilhamento de impressoras, e futura integração de câmeras de segurança.

### 3. Análise de Requisitos

Com base na planta baixa, foram identificados os seguintes requisitos:

*   **Número de salas atendidas:** Aproximadamente 15 ambientes distintos, incluindo 2 laboratórios, salas administrativas, sala multimídia, entre outros.
*   **Número de computadores que serão conectados:** Estimativa de 75 computadores, distribuídos entre laboratórios (~40), áreas administrativas (~20), salas de apoio (~10) e outros pontos (~5).
*   **Estimativa de usuários simultâneos:** Cerca de 100 usuários, considerando a lotação dos laboratórios, corpo docente e administrativo.
*   **Necessidade de Internet:** Sim. É essencial para as atividades pedagógicas e administrativas.
    *   **Plano sugerido:** Link de fibra óptica empresarial.
    *   **Velocidade contratada:** 500 Mbps de download e 250 Mbps de upload (simétrico, se possível), para garantir performance em navegação, streaming de vídeo e uso de sistemas em nuvem.
*   **Aplicações principais:** Navegação web, acesso a plataformas de ensino, sistemas de gestão escolar, impressão em rede e streaming de conteúdo multimídia.

### 4. Escolha do Provedor de Internet

Foram pesquisadas 3 opções de provedores de fibra óptica na cidade:

*   **Brisanet:** 300 Mbps (Download) / 150 Mbps (Upload) - R$ 299,00/mês.
*   **Startnet:** 500 Mbps (Download) / 250 Mbps (Upload) + IP Fixo - R$ 449,00/mês.
*   **Global Connect - Provedor C:** 600 Mbps (Download) / 300 Mbps (Upload) - R$ 599,00/mês.

**Justificativa da Escolha:** A **Opção 2 Startnet** foi a escolhida. Apresenta o melhor custo-benefício, com uma velocidade robusta para atender a demanda de usuários simultâneos e a inclusão de um IP fixo, que é vantajoso para a configuração de serviços de acesso remoto seguro e servidores internos.

### 5. Equipamentos Necessários

| Equipamento | Quant. | Especificação | Preço Unit. (Est.) | Preço Total (Est.) |
| :--- | :---: | :--- | :---: | :---: |
| Roteador/Firewall | 1 | Ubiquiti EdgeRouter X | R$ 800,00 | R$ 800,00 |
| Switch | 2 | Switch Gerenciável 48 Portas Gigabit | R$ 2.500,00 | R$ 5.000,00 |
| Access Point | 4 | Wi-Fi 6 (802.11ax) | R$ 600,00 | R$ 2.400,00 |
| Cabo de Rede | 2 caixas | Cat6 UTP (305m cada) | R$ 700,00 | R$ 1.400,00 |
| Rack de Parede | 1 | 12U x 570mm | R$ 600,00 | R$ 600,00 |
| Patch Panel | 2 | 24 Portas Cat6 | R$ 250,00 | R$ 500,00 |
| Canaletas e Tomadas | Lote | PVC 20x10mm e Tomadas RJ45 | R$ 1.000,00 | R$ 1.000,00 |
| **TOTAL ESTIMADO** | | | | **R$ 11.700,00** |

### 6. Topologia da Rede

*   **Desenho:** O ponto central da rede (rack com roteador e switches) será instalado na "Sala de Recursos" por ser uma localização central e de acesso restrito. A partir deste ponto, os cabos serão distribuídos para todos os ambientes.
*   **Topologia usada:** **Estrela Estendida**. O roteador principal se conecta aos dois switches de 48 portas no rack. Cada switch, por sua vez, conecta os pontos de rede em todas as salas e os Access Points, garantindo uma estrutura organizada e de fácil manutenção.
*   **Tipo de rede:** **Mista (LAN e WLAN)**. A rede será composta por uma rede local cabeada (LAN) para os computadores fixos, garantindo máxima velocidade e estabilidade, e uma rede local sem fio (WLAN) para cobrir as áreas comuns e permitir o uso de dispositivos móveis.

### 7. Cabeamento Estruturado

*   **Passagem dos cabos:** Os cabos Cat6 sairão do rack central e passarão por canaletas de PVC instaladas no rodapé ou na parte superior das paredes, de forma a minimizar o impacto na estrutura física do prédio.
*   **Divisão por setores:** A rede será logicamente dividida em setores usando VLANs (ver seção 8) para separar o tráfego: Administrativo, Laboratórios, Alunos (Wi-Fi) e Gerenciamento.
*   **Organização do rack:** O rack será organizado seguindo as boas práticas: patch panels para organização dos cabos, switches para conexão e roteador. Serão utilizados organizadores de cabos (guias) para manter o rack limpo e facilitar futuras manutenções.

### 8. Planejamento de Endereçamento IP

*   **Serviço de Endereçamento:** Será utilizado **DHCP** na maior parte da rede para atribuição dinâmica de IPs a computadores e dispositivos móveis. **IPs fixos** serão reservados para equipamentos de infraestrutura (roteador, switches, servidores) e impressoras.
*   **Faixa IP utilizada:** A rede principal utilizará a faixa **192.168.0.0/22**, que oferece sub-redes e IPs suficientes para a demanda atual e expansão futura.
*   **Exemplo de distribuição com VLANs:**
    *   **VLAN 10 (Gerência):** 192.168.0.0/29 - IPs fixos para equipamentos.
    *   **VLAN 20 (Administrativo):** 192.168.1.0/26 - DHCP para o setor administrativo.
    *   **VLAN 30 (Laboratórios):** 192.168.2.0/25 - DHCP para os computadores dos laboratórios.
    *   **VLAN 40 (Wi-Fi Alunos/Visitantes):** 192.168.3.0/24 - DHCP para a rede sem fio.

### 9. Segurança da Rede

*   **Senha para Wi-Fi:** Serão criadas duas redes sem fio (SSIDs):
    1.  `ETE_ADMIN`: com segurança WPA3 e senha forte, exclusiva para funcionários.
    2.  `ETE_ALUNOS`: com portal cativo para autenticação e aceite dos termos de uso.
*   **Separação entre redes:** O uso de VLANs garantirá que o tráfego da rede administrativa seja completamente isolado do tráfego dos laboratórios e da rede Wi-Fi dos alunos, prevenindo acessos não autorizados.
*   **Firewall:** O roteador será configurado com regras de firewall para bloquear acessos externos não solicitados e filtrar conteúdo inadequado na rede dos alunos, conforme as políticas da instituição.

### 10. Conclusão

O projeto detalhado nesta documentação apresenta uma solução de rede estruturada, moderna, segura e escalável, capaz de atender plenamente às necessidades da comunidade escolar. A implementação desta infraestrutura representa um avanço significativo para a instituição, proporcionando uma base tecnológica sólida para as atividades pedagógicas e administrativas, otimizando a comunicação e o acesso à informação.

As vantagens do projeto incluem a centralização do gerenciamento, a melhoria drástica no desempenho da conexão, o aumento da segurança dos dados e a preparação da escola para futuras tecnologias.

### 11. Referências

*   KUROSE, J. F.; ROSS, K. W. **Redes de Computadores e a Internet: Uma Abordagem Top-Down**. 8. ed. São Paulo: Pearson, 2021.
*   ABNT. **NBR 14565**: Cabeamento Estruturado para Edifícios Comerciais. Rio de Janeiro, 2019.
*   Tanenbaum, A. S.; Wetherall, D. J. **Redes de Computadores**. 5. ed. São Paulo: Pearson, 2011.

