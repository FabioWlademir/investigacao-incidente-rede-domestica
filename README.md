# Diagnóstico técnico e segurança em redes domésticas • Passo a passo com ferramentas gratuitas e profissionais

![MIT License](https://img.shields.io/github/license/FabioWlademir/investigacao-incidente-rede-domestica)
![Stars](https://img.shields.io/github/stars/FabioWlademir/investigacao-incidente-rede-domestica?style=social)
![Last Commit](https://img.shields.io/github/last-commit/FabioWlademir/investigacao-incidente-rede-domestica)

# 🔍 Investigação de Incidente em Rede Doméstica – Guia Prático

Este repositório apresenta um passo a passo prático e acessível para ajudar usuários e profissionais de segurança a investigarem **possíveis invasões em redes domésticas**, com foco em dispositivos como notebooks, celulares, TVs e roteadores Wi-Fi.
cybersecurity, home-network, malware-analysis, incident-response, pentest, nmap, wireshark, soc, noc, router-security


> ✅ Ideal para profissionais de **Suporte Técnico**, **Cibersegurança Doméstica**, **SOC/NOC**, ou consultorias especializadas.

---

## 🛡️ 1. Entendimento do Contexto e Coleta Inicial

Antes de iniciar qualquer análise, é fundamental compreender o cenário com o cliente:

* Quando começaram os comportamentos suspeitos?
* O que foi observado? (ex: câmera liga sozinha, lentidão, superaquecimento)
* Algum app, extensão ou programa foi instalado recentemente?
* Terceiros ou visitas usaram a rede Wi-Fi?
* Verificar se dados foram vazados:
  🔗 [Have I Been Pwned](https://haveibeenpwned.com/)

---

## 📶 2. Análise da Infraestrutura de Rede

### Acesso ao roteador:

* Acesse via navegador: `192.168.0.1` ou `192.168.1.1`
* Altere login/senha padrão
* Atualize o firmware
* Verifique:

  * Dispositivos conectados (IP e MAC)
  * Redirecionamento de portas
  * DNS personalizado
  * UPnP e Acesso WAN (desative)
  * Logs de conexões

### Ferramentas recomendadas:

* ✅ [Fing App](https://www.fing.com/products/fing-app)
* ✅ [Nmap + Zenmap GUI](https://nmap.org/download.html)
* ✅ [Wireshark](https://www.wireshark.org/download.html)

---

## 🧪 3. Análise de Dispositivos (TVs, Notebooks, Celulares)

### 💻 Notebooks e PCs

* Verifique programas ocultos ou recentemente instalados
* Analise extensões de navegador suspeitas
* Verifique tarefas agendadas com `taskschd.msc`
* Analise os processos com ferramentas específicas

#### Ferramentas:

* [Malwarebytes Free](https://www.malwarebytes.com/mwb-download)
* [Autoruns](https://learn.microsoft.com/en-us/sysinternals/downloads/autoruns)
* [Process Explorer](https://learn.microsoft.com/en-us/sysinternals/downloads/process-explorer)
* [Kaspersky Virus Removal Tool](https://www.kaspersky.com/downloads/thank-you/free-virus-removal-tool)

#### Comandos úteis:

```bash
sfc /scannow
chkdsk /f
```

---

## 📱 Celulares Android

* Apps instalados fora da Play Store?
* Permissões excessivas concedidas?
* Uso anormal de bateria ou dados móveis?

### Apps recomendados:

* [Malwarebytes Mobile](https://play.google.com/store/apps/details?id=org.malwarebytes.antimalware)
* [Kaspersky Mobile](https://play.google.com/store/apps/details?id=com.kms.free)
* [VirusTotal Mobile](https://play.google.com/store/apps/details?id=com.funnycat.virustotal)

---

## 📱 iOS (iPhone/iPad)

* O dispositivo foi jailbreakado?
* Verifique: Ajustes > Geral > VPN e Gerenciamento de Dispositivo
* Redefina as configurações de rede e privacidade, se necessário

---

## 📺 Smart TVs

* Verifique se conexões remotas estão habilitadas
* Remova apps desconhecidos
* Atualize o firmware da TV
* Execute um reset de fábrica se necessário

---

## 🔓 4. Teste de Vulnerabilidades

Ferramentas poderosas para escaneamento e análise:

* ✅ [Nessus Essentials](https://www.tenable.com/products/nessus/nessus-essentials)
* ✅ [OpenVAS (Greenbone)](https://www.greenbone.net/en/)
* ✅ [RouterScan](https://github.com/stascorp/rdpwrap/issues/903)
* ✅ [Shodan.io](https://www.shodan.io/)

### Testes avançados (com autorização do cliente):

* [Aircrack-ng](https://www.aircrack-ng.org/)
* [Hashcat](https://hashcat.net/hashcat/)

---

## 📁 5. Relatório Técnico

O relatório final deve incluir:

* Dispositivos comprometidos ou vulneráveis
* Vulnerabilidades detectadas
* Prints e logs das análises (Nmap, Fing, Process Explorer etc.)
* Medidas tomadas durante a investigação

### 📌 Recomendações ao cliente:

* Trocar todas as senhas (Wi-Fi, e-mail, roteador)
* Resetar e reconfigurar o roteador com segurança
* Atualizar firmwares e sistemas operacionais
* Separar dispositivos IoT em uma rede diferente
* Utilizar antivírus confiável e mantê-lo sempre atualizado

---

## 📚 Ferramentas Gratuitas Listadas

| Ferramenta        | Finalidade                         | Link                                                                                          |
| ----------------- | ---------------------------------- | --------------------------------------------------------------------------------------------- |
| Fing              | Mapear dispositivos na rede        | [fing.com](https://www.fing.com/products/fing-app)                                            |
| Nmap / Zenmap     | Escaneamento de portas e serviços  | [nmap.org](https://nmap.org/)                                                                 |
| Wireshark         | Análise de pacotes da rede         | [wireshark.org](https://www.wireshark.org/)                                                   |
| VirusTotal        | Análise online de arquivos e links | [virustotal.com](https://www.virustotal.com/)                                                 |
| Autoruns          | Programas iniciando com o sistema  | [Autoruns](https://learn.microsoft.com/en-us/sysinternals/downloads/autoruns)                 |
| Process Explorer  | Análise de processos ativos        | [Process Explorer](https://learn.microsoft.com/en-us/sysinternals/downloads/process-explorer) |
| Malwarebytes      | Antivírus gratuito                 | [malwarebytes.com](https://www.malwarebytes.com/)                                             |
| Nessus Essentials | Scanner de vulnerabilidades        | [tenable.com](https://www.tenable.com/products/nessus/nessus-essentials)                      |
| Aircrack-ng       | Teste de força de senhas Wi-Fi     | [aircrack-ng.org](https://www.aircrack-ng.org/)                                               |

---

## ⚠️ Considerações Éticas

* Obtenha autorização formal escrita do cliente
* Informe os riscos envolvidos (perda de dados, interrupção de serviços, etc.)
* Nunca acesse dados pessoais sem consentimento
* Respeite a LGPD e as boas práticas da segurança digital

---

## 📜 Licença

Este conteúdo está licenciado sob a **Licença MIT**.
Sinta-se livre para usar, adaptar e compartilhar com atribuição.

---

## ✍️ Autor

**Fábio Wlademir**
Especialista em TI • NOC • SOC • Segurança Digital • Automação com IA

🔗 [Blog Técnico - F2 Suporte](https://f2suporte.blogspot.com/search/label/SOC%20e%20NOC)
🔗 [LinkedIn](https://www.linkedin.com/in/fabiowlademir)
🔗 [GitHub](https://github.com/FabioWlademir)

---

## 🧰 Veja também meus outros projetos:

* 🔗 [scripts-suporte](https://github.com/FabioWlademir/scripts-suporte): Scripts úceis para suporte técnico e diagnóstico
* 🔗 [siem-inteligente](https://github.com/FabioWlademir/siem-inteligente): SIEM com foco em detecção e correlação inteligente
* 🔗 [zabbix-monitoring-lab](https://github.com/FabioWlademir/zabbix-monitoring-lab): Laboratório prático com Zabbix
* 🔗 [network-security-audit](https://github.com/FabioWlademir/network-security-audit): Checklist e scripts para auditoria de rede
* 🔗 [enterprise-web-infra-security](https://github.com/FabioWlademir/enterprise-web-infra-security): Hardening e segurança para infraestruturas web

---

## 🚀 Curtiu o conteúdo?

Se esse material foi últil para você ou para seus clientes,
**⭐ dê uma estrela neste repositório** e compartilhe com outros profissionais de TI e segurança.

Juntos, podemos construir um ecossistema mais seguro e consciente, mesmo fora dos datacenters!

