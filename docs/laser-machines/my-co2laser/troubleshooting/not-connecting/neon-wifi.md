# Direct Wi-Fi Connection (Neon Access Point)

A **Neon** está equipada com um módulo wireless integrado que permite a criação de uma rede local própria. Este artigo detalha como estabelecer uma ligação direta "peer-to-peer" entre o seu computador e a máquina, sem a necessidade de routers externos ou cabos.

---

## Understanding the Network Architecture

Ao utilizar este método, a máquina laser atua como um **Wireless Access Point (AP)**. Antes de prosseguir, considere as características operacionais desta configuração:

* **Vantagens:** Mobilidade total dentro do alcance do sinal e uma ligação dedicada e estável entre o hardware e o software.
* **Limitações:** Como a placa de rede Wi-Fi do seu computador estará ocupada com o sinal da máquina, perderá o acesso à internet do seu local de trabalho. 
* **Dica de Optimização:** Para manter o acesso à internet enquanto está ligado à **Neon** via Wi-Fi, pode ligar o seu computador à rede local através de um cabo Ethernet (LAN).

---

## Connectivity Setup: Step-by-Step

Siga estas instruções para sincronizar o seu hardware com o **Due Studio**:

### 1. Identify the Network
Abra a lista de redes sem fios no seu computador. Procure por um SSID identificado como **Neon + [Número de Série]**. 

<figure markdown="span">
--8<-- "image-placeholder.md"
  <figcaption>Figure 1: Localizar o SSID da Neon na lista de redes (Brevemente)</figcaption>
</figure>

### 2. Authentication
Selecione a rede e insira a chave de segurança predefinida: `due-laser`. 

<figure markdown="span">
--8<-- "image-placeholder.md"
  <figcaption>Figure 2: Inserir as credenciais da rede (Brevemente)</figcaption>
</figure>

### 3. Verification in Due Studio
Assim que o sistema operativo confirmar a ligação Wi-Fi, abra o **Due Studio**. Verifique o indicador de "Estado de Conexão" na interface do software. Se o ícone estiver verde, o "handshake" entre o computador e o controlador da **Neon** foi bem-sucedido.

<figure markdown="span">
--8<-- "image-placeholder.md"
  <figcaption>Figure 3: Indicador de estado de conexão no Due Studio (Brevemente)</figcaption>
</figure>

---

!!! info "Troubleshooting"
    Se a rede não aparecer ou a ligação falhar, consulte o nosso guia de **Resolução de Problemas de Rede** ou certifique-se de que a máquina está dentro do alcance ideal do sinal.

---
**Precisa de mais ajuda?**
Se preferir integrar a máquina na rede Wi-Fi existente no seu escritório em vez de usar o modo AP Direto, contacte o suporte técnico para o guia de integração de rede.