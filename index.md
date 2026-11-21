# Política de Privacidade — Net Toolkit

_Última atualização: 20 de novembro de 2026 (versão 1.2)._

O **Net Toolkit** ("o aplicativo") é uma ferramenta de diagnóstico de redes para
Android, **gratuito e sem anúncios**, com um botão opcional para **pagar um café** ao
desenvolvedor pela Google Play. Esta política explica quais dados o aplicativo
acessa, com quem eles são trocados e por quê.

**Resumo:** o desenvolvedor **não coleta, não recebe e não armazena** dados dos
usuários. Não há conta, cadastro, analytics, rastreamento nem publicidade. Algumas
funções, quando você as usa, conectam-se a serviços públicos de terceiros (como a
Cloudflare) que, como em qualquer acesso à internet, recebem o **endereço IP** do seu
aparelho. **Nenhum resultado** das ferramentas é enviado a ninguém. O café opcional
é pago e processado pelo **Google Play**.

## 1. Dados que ficam só no seu aparelho
- **Resultados das ferramentas** (dispositivos da rede, redes Wi-Fi, latências,
  rotas, medições de velocidade): exibidos na tela e **não enviados** ao desenvolvedor.
- **Preferências** (última sub-rede do Scanner, alvos do Monitor e do MTR, tema):
  salvas no armazenamento privado do aplicativo. Desinstalar o aplicativo apaga tudo.

## 2. Permissões
- **Internet e estado da rede** (`INTERNET`, `ACCESS_NETWORK_STATE`,
  `ACCESS_WIFI_STATE`, `CHANGE_WIFI_STATE`): fazer os testes e ler/disparar a busca
  de redes Wi-Fi.
- **Multicast do Wi-Fi** (`CHANGE_WIFI_MULTICAST_STATE`): durante o scan da rede,
  receber os anúncios que aparelhos da sua rede local fazem por broadcast (por
  exemplo, roteadores e tomadas inteligentes), usados só para mostrar o fabricante e
  o modelo de cada um na tela.
- **Localização** (`ACCESS_FINE_LOCATION`/`ACCESS_COARSE_LOCATION`): o Android só
  entrega a lista de redes Wi-Fi próximas (e o identificador da rede atual) a apps
  com essa permissão e com a Localização do aparelho ligada. O aplicativo a usa
  **exclusivamente** para isso, com o app aberto (nunca em segundo plano); **não**
  usa GPS, **não** calcula onde você está e **nunca** coleta, guarda ou envia esses
  dados.

Se a permissão for negada, só a aba Wi-Fi deixa de listar redes.

## 3. Conexões que o aplicativo faz (todas iniciadas pelo uso)
| Função | Para onde | O que o destino recebe |
|--------|-----------|------------------------|
| Scanner, Monitor, MTR, Diagnóstico | Aparelhos da sua rede local e endereços públicos de teste (ex.: 8.8.8.8, 1.1.1.1, 208.67.222.222, google.com, office.com, apple.com) | Pacotes de teste de rede (ping/TCP/UDP) e, no Scanner, consultas de descoberta e identificação na rede local (mDNS, SSDP, NetBIOS, SNMP de leitura, Ubiquiti, MikroTik, e a página inicial, o certificado e a saudação dos serviços de cada aparelho), com o IP do aparelho, como em qualquer conexão. Nada é alterado nos aparelhos. |
| Velocidade — teste | **Cloudflare** (speed.cloudflare.com), no servidor mais próximo | O tráfego do teste (dados de download e upload), com o IP do aparelho, como em qualquer conexão. **Os resultados ficam só no seu aparelho** — o aplicativo não os envia a ninguém. A Cloudflare trata o IP segundo a política dela: <https://www.cloudflare.com/privacypolicy/>. |
| Velocidade — latência sob carga | Cloudflare (1.1.1.1, porta 53/TCP) | Conexões TCP curtas, com o IP do aparelho. |
| Velocidade — IP público e país | **Cloudflare** (1.1.1.1) e, como reserva, **ipify** ou **icanhazip** | O IP do aparelho (é o que permite a resposta). O **provedor** é identificado **no próprio aparelho**, por uma base embutida — nada é enviado para isso. O resultado é **mostrado a você** e não é guardado nem enviado ao desenvolvedor. |
| Velocidade — CGNAT | Seu roteador (UPnP, na rede local) e um traceroute | Pacotes de diagnóstico; nenhum dado pessoal. |
| Ajustes — "Pagar um café" (opcional) | **Google Play** | Ver a seção 4. |

O aplicativo **não** envia endereços MAC, listas de dispositivos, nomes de redes
Wi-Fi nem resultados para nenhum servidor. A identificação de fabricantes usa uma
base **embutida** (listagem pública do IEEE), sem consulta online.

## 4. "Pagar um café" (opcional)
O aplicativo é gratuito. Em Ajustes, quem quiser pode pagar um café de R$ 5 ao
desenvolvedor — uma doação que **não libera nenhum recurso**. A compra é feita na tela
de pagamento do **Google Play** e processada pelo Google, segundo a política de
privacidade dele (<https://policies.google.com/privacy>):
- o aplicativo **não recebe nem guarda** dados de pagamento (cartão, conta, Pix etc.);
  só recebe da Play a confirmação da compra, para concluí-la;
- o desenvolvedor recebe do Google, na Play Console, as informações do pedido que a
  Play fornece a quem vende (como número do pedido, produto, valor, data e país),
  usadas só para a contabilidade e eventuais reembolsos;
- a biblioteca de faturamento do Google, embutida no aplicativo, envia ao Google
  registros técnicos do uso do pagamento (por exemplo, se a chamada funcionou ou
  falhou), que o Google usa para manter a biblioteca. Isso só acontece quando você
  toca em "Pagar um café".

Reembolsos seguem as regras do Google Play.

## 5. LGPD e GDPR
- **Controlador:** o desenvolvedor não trata dados pessoais dos usuários; não há base
  de dados nem servidor próprio.
- **Terceiros:** a Cloudflare e os demais serviços processam o IP apenas para
  responder às conexões, segundo as próprias políticas de privacidade; o Google Play
  processa o café (seção 4).
- **Base legal:** execução da função que você pediu (cada conexão só acontece quando
  você usa a função correspondente).
- **Seus direitos (LGPD art. 18 / GDPR):** o desenvolvedor não guarda dados no
  aplicativo nem em servidor próprio; os pedidos do café ficam no Google Play, e
  dúvidas sobre eles podem ser enviadas ao contato abaixo. Para dados tratados pelos
  serviços citados, fale diretamente com eles.

## 6. Crianças
O aplicativo não é direcionado a crianças.

## 7. Segurança
As consultas a serviços web e o teste de velocidade usam HTTPS (TLS) com verificação
de certificado.

## 8. Alterações
Mudanças nesta política serão publicadas nesta mesma URL, com a data atualizada.

## 9. Contato
Dúvidas sobre privacidade: **rogerio.de.queiroz.3l@gmail.com**.
