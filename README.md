# Introduction-to-Netoworks-NotebookLM
Notebook para estudo dos fundamentos da computação usando o NotebookLM

Este repositório foi desenvolvido para o desafio de projeto da **DIO**, utilizando o **NotebookLM** como ferramenta de aprendizagem ativa.  O foco deste projeto é a compreensão profunda de como a infraestrutura de redes sustenta a comunicação digital moderna. O diferencial deste caderno temático é que sua base de conhecimento foi integralmente construída a partir da série "Introdução a Redes" do **Fabio Akita**, garantindo um conteúdo de alta densidade técnica e visão crítica sobre computação.

### 🎯 Objetivos:
* **Compreender a Camada Física:** Analisar o processo de modulação e como dados digitais são convertidos em ondas para transmissão.
* **Garantia de Integridade:** Estudar os métodos de detecção e correção de erros em transmissões de dados.
* **Arquitetura de Sistemas:** Dominar o funcionamento de Sockets e a relação Cliente-Servidor na Web.
* **Segurança e Infraestrutura:** Explorar o uso de túneis SSH para contornar firewalls e a implementação de VPNs e servidores NAS para redes domésticas seguras.

### 📚 Fontes:
As seguintes fontes foram utilizadas como base de conhecimento para a IA:

1.  **Introdução a Redes: Como Dados viram Ondas? | Parte 1**
     * [Assistir no YouTube](https://www.youtube.com/watch?v=0TndL-Nh6Ok&list=PLdsnXVqbHDUcTGjNZuRYCVj3AZtdt6oG7&index=1)
2.  **Detecção e Correção de Erros | Introdução a Redes Parte 2**
    * [Assistir no YouTube](https://www.youtube.com/watch?v=3W-8TQJwuWY&list=PLdsnXVqbHDUcTGjNZuRYCVj3AZtdt6oG7&index=2)
3.  **Como sua Internet Funciona | Introdução a Redes Parte 3**
    * [Assistir no YouTube]([https://www.youtube.com/watch?v=gcv5hXyTcIo](https://www.youtube.com/watch?v=gcv5hXyTcIo&list=PLdsnXVqbHDUcTGjNZuRYCVj3AZtdt6oG7&index=3)
4.  **Como Funciona Sockets, Cliente, Servidor e a Web? | Introdução a Redes Parte 4**
    * [Assistir no YouTube]([https://www.youtube.com/watch?v=lc6U93P4Sxw](https://www.youtube.com/watch?v=lc6U93P4Sxw&list=PLdsnXVqbHDUcTGjNZuRYCVj3AZtdt6oG7&index=4)
5.  **Burlando Proxies e Firewalls | Introdução a Redes Parte 5 - SSH**
    * [Assistir no YouTube]([https://www.youtube.com/watch?v=T-jHuFnxZ2k](https://www.youtube.com/watch?v=T-jHuFnxZ2k&list=PLdsnXVqbHDUcTGjNZuRYCVj3AZtdt6oG7&index=5)
6.  **Criando uma Rede Segura | Introdução a Redes Parte 6 - VPN e NAS**
    * [Assistir no YouTube]([https://www.youtube.com/watch?v=EOmzo5d0F9Y](https://www.youtube.com/watch?v=EOmzo5d0F9Y&list=PLdsnXVqbHDUcTGjNZuRYCVj3AZtdt6oG7&index=6)

---

### 🧠 Testes de prompt:
* **Prompt Exploratório:** *"Faça um resumo dos principais conceitos abordados."*
* *"O que é exatamente o bit-flip e como evitá-lo?"*
* *"Como o túnel SSH consegue burlar um firewall?"*
  
    * **Resultado:** O NotebookLM conseguiu correlacionar as fontes e responder de forma apropriada para todas as perguntas feitas.

---

### 📖 Miniguia:

#### 📝 Resumo Estruturado
A introdução a redes abordada nas fontes abrange desde a física da transmissão de dados até protocolos complexos de segurança e armazenamento. Os principais conceitos podem ser divididos nas seguintes áreas fundamentais:
1. Camada Física e Transmissão de Dados
A comunicação em rede começa com a transformação de bits digitais em ondas analógicas (modulação) para trafegarem por meios como fios de cobre, fibra ótica ou ar (wi-fi).

    Modem: É o dispositivo que realiza a modulação e demodulação do sinal.
    Largura de Banda (Bandwidth): Refere-se à capacidade teórica do meio físico; velocidades são medidas em bits (ex: 300 Mbps), enquanto o armazenamento usa bytes (1 byte = 8 bits).
    Comutação de Pacotes (Packet Switching): Ao contrário da antiga comutação de circuitos, os dados modernos são fragmentados em pacotes (datagramas), permitindo que múltiplos usuários compartilhem o mesmo canal simultaneamente.

2. Endereçamento e Roteamento (Camada de Rede)
Para que os pacotes cheguem ao destino, a rede utiliza identificadores específicos:

    Endereço IP: Um número (IPv4 de 32 bits ou IPv6 de 128 bits) que identifica dispositivos na rede. Máscaras de sub-rede definem quais partes do IP pertencem à rede e quais ao host.
    NAT (Network Address Translation): Devido à escassez de IPv4, o NAT permite que vários dispositivos em uma rede privada compartilhem um único IP público.
    MAC Address e ARP: O MAC é o endereço físico único da placa de rede. O protocolo ARP mapeia endereços IP para endereços MAC dentro de uma rede local.
    DNS: Funciona como uma "lista telefônica", traduzindo nomes de domínio (como youtube.com) em endereços IP.

3. Sockets e Protocolos de Aplicação
A comunicação entre programas ocorre através de Sockets, que são a combinação de um Endereço IP e uma Porta.

    Portas: São identificadores numéricos (0 a 65535) que direcionam o tráfego para processos específicos no sistema operacional. Por convenção, a porta 80 é usada para HTTP e a 443 para HTTPS.
    Modelo OSI e TCP/IP: O modelo OSI define 7 camadas de rede, embora na prática o modelo TCP/IP seja o mais utilizado. O TCP garante a entrega confiável de pacotes, enquanto o UDP é mais rápido, mas sem garantias de entrega (ideal para streaming).

4. Segurança e Tunelamento
A segurança envolve proteger a integridade dos dados e o acesso à rede:

    Firewall: Filtra pacotes com base em regras de "permitir" ou "negar" (allow/deny).
    Sanitização de Dados: É essencial para prevenir ataques de injeção, onde comandos maliciosos são inseridos em inputs de usuários.
    SSH e Tunelamento: O SSH permite criar túneis criptografados. O Remote Forward pode ser usado para "furar" firewalls de dentro para fora, expondo um serviço local para a internet.
    VPN (Virtual Private Network): Cria uma rede privada virtual usando drivers de rede virtuais (Tun/Tap) para conectar dispositivos remotos como se estivessem na mesma rede local de forma segura.

5. Confiabilidade e Armazenamento (NAS)
Redes modernas frequentemente integram sistemas de armazenamento robustos:

    NAS (Network Attached Storage): Um servidor dedicado ao armazenamento de arquivos.
    RAID: Tecnologia que utiliza múltiplos discos para oferecer performance (RAID 0) ou redundância/segurança (RAID 1, 5, 6).
    Correção de Erros: Algoritmos como Hamming Code e Reed-Solomon são usados para detectar e corrigir o "bit-flip" (corrupção de bits causada por interferências ou falhas físicas).

#### 📕 Glossário
Este glossário reúne os conceitos fundamentais sobre redes de computadores, abrangendo desde a física da transmissão até protocolos de segurança e armazenamento, conforme detalhado nas fontes.
Transmissão e Camada Física

    Modem: Dispositivo que realiza a modulação (converte bits digitais em ondas analógicas) e a demodulação (converte ondas de volta em bits) para permitir a comunicação por meios físicos como fibra ótica ou cabos de cobre.
    Largura de Banda (Bandwidth): Refere-se à capacidade teórica máxima de faixas de frequência que um meio físico permite passar, determinando quantos dados podem trafegar.
    Comutação de Pacotes (Packet Switching): Ao contrário da antiga comutação de circuito, aqui a informação é fragmentada em pacotes (datagramas) que compartilham o canal de comunicação, permitindo maior escalabilidade e eficiência.
    Fibra Ótica: Meio de transmissão que utiliza pulsos de luz através de fios de vidro, permitindo velocidades altíssimas (até 10 Gbps ou mais) com baixa perda de sinal em longas distâncias.

Endereçamento e Protocolos de Rede

    Endereço IP: Identificador numérico de um dispositivo na rede. O IPv4 usa 32 bits e enfrenta escassez, enquanto o IPv6 usa 128 bits, oferecendo um número virtualmente infinito de endereços.
    DNS (Domain Name System): Funciona como uma "lista telefônica" da internet, traduzindo nomes de domínio humanos (como youtube.com) nos endereços IP que as máquinas entendem.
    MAC Address: Endereço físico único de 48 bits gravado de fábrica em cada placa de rede.
    ARP (Address Resolution Protocol): Protocolo responsável por mapear endereços IP aos seus respectivos endereços físicos MAC dentro de uma rede local.
    DHCP (Dynamic Host Configuration Protocol): Protocolo que atribui automaticamente endereços IP e configurações de rede aos dispositivos que se conectam a um roteador.
    NAT (Network Address Translation): Técnica que permite que múltiplos dispositivos em uma rede privada compartilhem um único IP público para acessar a internet, ajudando a mitigar a falta de endereços IPv4.

Comunicação entre Processos e Aplicações

    Socket: A combinação de um Endereço IP e uma Porta. É a interface que permite a conexão e troca de dados entre dois processos (programas) rodando em máquinas diferentes.
    Portas: Identificadores numéricos (0 a 65535) que direcionam o tráfego para serviços específicos. Portas abaixo de 1024 são reservadas para o sistema (ex: 80 para HTTP, 443 para HTTPS).
    TCP (Transmission Control Protocol): Protocolo da camada de transporte que garante a entrega confiável e sequencial dos pacotes.
    UDP (User Datagram Protocol): Protocolo de transporte mais rápido e leve que o TCP, mas que não garante a entrega nem a ordem dos pacotes, sendo ideal para streaming de vídeo e áudio.
    Modelo OSI: Modelo de referência dividido em 7 camadas (Física até Aplicação) que padroniza como as comunicações de rede devem ocorrer.

Segurança e Conectividade Avançada

    Firewall: Programa que atua como filtro de segurança, aplicando regras de "permitir" (allow) ou "negar" (deny) ao tráfego que entra ou sai de uma rede.
    Sanitização: Prática essencial de segurança que consiste em limpar e filtrar as entradas de dados de usuários para remover caracteres maliciosos e evitar ataques de Injeção (Injection).
    SSH (Secure Shell): Protocolo para acesso remoto seguro que permite criar túneis criptografados para burlar firewalls e acessar serviços internos de fora da rede.
    VPN (Virtual Private Network): Cria uma rede privada virtual sobre a internet pública, utilizando interfaces virtuais (Tun/Tap) para conectar dispositivos distantes como se estivessem na mesma rede local.

Confiabilidade e Erros

    Bit-flip: Inversão acidental de um bit (de 0 para 1 ou vice-versa) causada por interferências eletromagnéticas, falhas físicas ou raios cósmicos.
    ECC (Error Correction Code): Memória com capacidade de detectar e corrigir erros de bit simples automaticamente.
    RAID: Tecnologia que combina vários discos rígidos. O RAID 0 foca em performance (divisão de dados), enquanto o RAID 1, 5 e 6 focam em redundância e segurança contra falhas físicas.
    NAS (Network Attached Storage): Servidor dedicado ao armazenamento e compartilhamento de arquivos em rede, geralmente utilizando configurações de RAID para segurança dos dados.
    
#### 🛠️ Prompts Reutilizáveis
* *"Explique o conceito de encapsulamento de dados usando o exemplo da VPN nas fontes."*
* *"Crie uma tabela comparativa entre SSH e VPN com base no conteúdo de segurança das aulas 5 e 6."*
* *"Quais são os principais tipos de erros de rede mencionados e como o Checksum ajuda a resolvê-los?"*

---
✨ *Projeto desenvolvido para fins educacionais - Portfólio de Infraestrutura e Segurança.*
