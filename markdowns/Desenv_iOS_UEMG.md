# Entendendo o processo de desenvolvimento de aplicativos iOS

---

## Salmo Junior

Mineiro, Chapter Leader do CocoaHeads BH, dev iOS desde 2011, corinthiano, viajante e viciado em queijo.



![right](../assets/eu.png)

<br><br><br><br><br><br><br><br><br><br><br><br>

Sênior iOS Developer at CI&T
salmo@ciandt.com
@salmojr

---

## Agenda

- Overview
- Guidelines
- Consumo de Serviços
- Armazenamento de Dados
- Hardware/Limitações
- Ferramentas
- Dicas

---

## Overview

---

#### Overview
## 

---

#### Overview
## iOS Development Kit

- Xcode
- Interface Builder
- iOS Simulator
- Instruments

![right 40%](https://lh3.googleusercontent.com/_eCHMq-Js-JWbfhwEq7WmcmokLhZWPVImz2xB148DM8k8t1wnubQACX9KnP-pqEwawJQvKChARRK3VFbtMYAMRnjIBpmoiyx_K5J5RwzKekAuK05woY2aJFPWYMCTt2ugMWcLBAVzg)

---

#### Overview
## 

---

## Guidelines

---

#### Guidelines
## Utilização da Main Thread

![inline](https://lh5.googleusercontent.com/SLIDz-TmTSI29kPSo7pi907dtSuph76-2yRQw4Oi2Udi-xOpaNh-_PESzh64oQAENxkiMqHJI_cRqNztFIRhue2f2lspVFAfqUWAz7yDSMY3py7hpGqqgKajk9XE9PFiIkTcpK-nFA) ![inline](https://lh4.googleusercontent.com/lXWEKqR9vhqNWY_YGa_H4gD1QyPYQQzH1gi7j9DCpbMwG6ohEEvGValceylDMRuFuWeC6tToBfoMRLjBBYC0Js_qn7vsiWQrl-v17WMPwaN0L48HioYcwmrhV9xFEzEOTXXKcEdOjg)

---

#### Guidelines
## Notificações

Para o Usuário

- Local Notification
- Push Notification

![](https://lh5.googleusercontent.com/xvxY92g0AYjY8dzb2e00WHJ_AnxhVJMwS7HamcYmC89BB7UvMFb3ypfDaoE93UA9-XKw856nX-wTG5MXkC27qfW72rfS_GF7qog--L642s1t3X6IxrxlHVuU_1aP5clVGgLDNSBL_w) ![inline](https://lh4.googleusercontent.com/p8kD4kVpytzYAjtrOTZBJ2QaB2gjntsxg5kLBdtN89ML9A6DIta-W7VueNennH1Q82wRd3E1XmdUbmp3uwW2zqLshnzcWcs0aQGwD0_jzXCfxjPRXib0NpT8hg1HmobWtQfJNbKHBA) ![inline](https://lh5.googleusercontent.com/mPZxUF0NmW_BKQ_M4NXe2GqhrPmyA1InvxD6uPI0Q6JOM7Fg-LPbJRw6XQXlbX4AtgEEhD7yQeW-1Kkjz6XMGf9R8PZt5dL4QDk4uRJ3TMfWaTI-6LQUHGXByb48OGsSuOSczMl4ew)

---

#### Guidelines
## Notificações

Para o S.O.

- Notification Center
- Silent Push Notification

![right 110%](https://lh4.googleusercontent.com/QH645IwcQ9y6PC5LEigLJPmv62sOWn2DG9X_ZOLXqnQMz0bmZpTm_avBKB5-1dNDfz7yCVq5aJ5_uTHIDBVuYC54JQ-LxPhPzKnSFPMrzwoGOZytioMhJ8pf86UqdEkfoP9hDKXlmA)

---

#### Guidelines
## Interrupções

![inline](https://lh4.googleusercontent.com/5YTB51qpHCe7sQW4rnOA3GfRv2IjvY-6hyusAq9YBvRUQR-xRah4TIBt1UfLEszM7eLXGaNpo3HCBpX7fj7LHU4Gze_4INwWoCpxOzHeX-ipFoWUI-ApKbgiGXUPTHo1myHFN4oMVg) ![inline](https://lh5.googleusercontent.com/GTaLdayR8eyFEw8ivgzlSXvz4i_1aL-3S5QxSUlapaUUDO5qLVEBhZP5zn8gZuHao3NA1W6X9nzSK-l7cNo6VTfMGSTMiWb9m0Sahced61J2GsY7dteyhTzdQsn27s_quqKV-QWmdw)

---

#### Guidelines
## Internacionalização

![inline](https://developer.apple.com/library/ios/documentation/MacOSX/Conceptual/BPInternational/Art/internationalization_intro_2x.png)

---

#### Guidelines
## Sincronismo de dados

![inline](https://lh6.googleusercontent.com/f-g7E_0HtcFuKsLX4Gj4iJBLU13oOTWzlGZNgrsoKRg1vz4H-jHZAOiWQMmazdi0ur4xwf3Uo0T8Mwr0UWagA64aiELSxdg6r1wrBffm1HIiSR1CPhTrfsmRaLEcR8sTIBbfZ7x8qA)

<!--um conteúdo inicial offline 
Todos os syncs de dados pesados (Ex: Produtos de uma loja), devem ser feitos em segundo plano, sem alterar a User Experience.
-->

---

#### Guidelines
## Semantic Versioning 2.0.0 

![inline](https://lh5.googleusercontent.com/IXO28FSczqULIfxNkqmsvuHVbs-5KQ3bMv9oydqPi4hyzQ9IKtcQy2hzJ13zC0ypZKPJ9UzJb_ejy_XRNr-3rOEuf_k3Zj8He-UrYRRSjtexFkTbn8BaxRg-mHlMa27tB213RsIHNQ)

---

#### Guidelines
## Segurança

Keychain
Senhas, usuários e chaves de APIs

Plist
Configurações da app

NSUserDefaults
Preferências do usuário

---

## Consumo de Serviços

---

#### Consumo de Serviços
## REST com formato JSON

- Menor e mais simples, poupando o consumo de dados
- Menor processamento devido a facilidade de conversão e interpretação
- Fornece melhores tempos de resposta

---

#### Consumo de Serviços
## Ambiente

![inline](https://lh5.googleusercontent.com/En1zhL2s34Ch2fDUTiRYnmKV8zi0BWEyPFj9hNicNTXe5o_kIPC2ApgPadHrDysSueGJZ-BTlybJ2wWFxCAYGK5kQabrrWxFYYpHG_fU0wKMAE5suQ5t8IjL0GSNXYHLKqH9FfKnvQ)

---

#### Consumo de Serviços
## Versionamento e tempo de desenvolvimento

![inline](https://lh3.googleusercontent.com/lRSEtZz0dGIBNvhbSklft3uhpz2YOGucOkVupihYQJYQvJ9WCyMXhEQpiwwnhHrYXlWf0LxMMYdbR54ezeW0z-H_8W2VymnMCzGVp95McyPJMt1KT-a9ZrV8ZBL_upgf4R_iF3pCkA)

<!--Evita Retrabalho e Testes duplicados, com Mockup / Consumo real.
Evita Refactor tardio do time de Backend.
Desenvolvimento mobile simulando um ambiente real e já testado.
-->

---

## Armazenamento de Dados

---

#### Armazenamento de Dados
##

---

#### Armazenamento de Dados
##

---

#### Armazenamento de Dados
##

---

#### Armazenamento de Dados
##

---

## Hardware/Limitações

---

#### Hardware/Limitações
## Versões de S.O. são lançadas frequentemente

![inline](https://lh6.googleusercontent.com/oGwVv1HgWR8Wyoiye61pf0bBOxGyRxaiaSnzhv5DzCWilnj4PxKmSvsbkzdTDqpzspeEq5UgyElp54y-Fc6zuKu4emfIy7xm63FFl8Ui853GvN0ROO2zhVayedagCk1-GMkZcabsRg)

---

#### Hardware/Limitações
## Sensores

São um dos grandes diferenciais dos smartphones

![inline](https://lh5.googleusercontent.com/sE297ADrqOk5NqnAB64b3xU0HPZEphD6P9SyuN3C8tBJxdl1GZcJ9qW7or-6MSIDMF6_1ilCKbrjevq4jQJ-BrORACmh0R3Bre8RCZSUKrA2SfjiOox9Aa62n8NV-DLnGi9SSAmHkg)

---

#### Hardware/Limitações
## Sensores

Mas também podem ser os grande vilões

![inline](https://lh3.googleusercontent.com/MwY2t7bxd33eIkM2ZI7uX6sAh63nEWlJIPaCcxbVy-QGqaECTOkHSvifpmdmvOGIUljrzWrs1s9vPOL0LMH6r6JYmQ4M1N2QFcnNZtLjNGA6fQZXy5euCbE77_sS2Ox3rfJH9udFbg)

---

#### Hardware/Limitações
## Localização

![inline](https://lh6.googleusercontent.com/6uFiHMEOBP2mVOD7MIedJlKogfl0LHDkkhuBUovGW0Rh1fs94sElttqUKUUZ3503zWergHgVhWLpik8w0kK-TZ4pLCgHXyaEWQidl1k9pRCdbfnOmiQs9sQ7PFQwXQXTfUPuX6_UPg)

---

#### Hardware/Limitações
## Uso de banda de internet

- Preocupar com os tipos e quantidade de requisições
- Fazer cache sempre que possível das informações
- Verificar o tipo de conexão antes de fazer requisições pesadas e downloads de arquivos
- Pedir permissão do usuário para usar a rede 3G para downloads de arquivos.

<!--Nos preocupar com os tipos e quantidade de requisições
Fazer cache sempre que possível das informações
Verificar o tipo de conexão antes de fazer requisições pesadas e downloads de arquivos
Pedir permissão do usuário para usar a rede 3G para downloads de arquivos.
-->

---

#### Hardware/Limitações
## Divisão de processamento entre Aplicativo e Backend

- Uma alteração do lado mobile implica no lançamento de uma nova versão
- Tempo de alteração/correção
- Poder de processamento

---

#### Hardware/Limitações
## Tamanho do Aplicativo

![inline](https://lh5.googleusercontent.com/sMTo_wtjorzd0NhlzKg-2_hB1jaG7Q_uAgVHTrOV10ydDnsdI40KxBqKYEjVeJbkoikaGjXuhOtug3Td2t1MWrWnG6_vLg18tvp99kAbwDBEbXzHpVK_gzH8-HUL_2tKYVQ0mFQ9Ew)

---

#### Hardware/Limitações
## Armazenamento limitado

![inline 75%](https://lh5.googleusercontent.com/9CEOaBv_8ruScVlgzIIb5-IsmmaiV4992WqkzMu08EqrEyd1u1J3epmOuDcM8PwRMAogzGbGdmlTaA2BK-vqV5mUKdAPoSOmnH2-caJPtSLQzRcSh3heNX5P8Cw56PcF6KDmRNf9eg)

<!--Implementar rotinas para limpar os dados que não estão sendo mais utilizados pelo usuário, como Imagens e PDFs. 

Remover os assets que não são mais utilizados no projeto, sempre que lançar uma nova versão.
-->

---

## Ferramentas

---

#### Ferramentas
## Xcode

![inline](https://developer.apple.com/xcode/images/xcode-hero-large.png)

---

#### Ferramentas
## Integração Contínua

![inline](https://d3r49iyjzglexf.cloudfront.net/mobile/mobile-diagram@2x-1bafa256595b159e874b503c188f61367dd495b27743426f190d4b9799ff9f1c.jpg)

---

#### Ferramentas
## Integração Contínua

- **Jenkins** (http://jenkins-ci.org/)
- **CircleCI** (https://circleci.com/)
- **Bitrise** (https://www.bitrise.io/)
- **Travis CI** (https://travis-ci.org/)
- **Buddybuild** (https://buddybuild.com/)

---

#### Ferramentas
## Crash Reporting

![inline](http://try.crashlytics.com/reports/css/images/top_screen3.png)

---

#### Ferramentas
## Análise de performance

![inline](https://spin.atomicobject.com/wp-content/uploads/Intro.png)

---

#### Ferramentas
## Gerenciamento de dependências

![inline](http://cdn1.tnwcdn.com/wp-content/blogs.dir/1/files/2015/05/cocoapods.png) ![inline 50%](https://raw.githubusercontent.com/Carthage/Carthage/master/Logo/PNG/colored.png)

---

#### Ferramentas
## Analytics

![inline](https://developer.apple.com/app-store/app-analytics/images/app-analytics-hero.png)

---

#### Ferramentas
## Distribuíção/Beta Test

- a

---

## Dicas

---

#### Dicas
## Ganhe tempo matendo a qualidade 

![inline](https://1.bp.blogspot.com/-YIfQT6q8ZM4/Vzyq5z1B8HI/AAAAAAAAAAc/UmWSSMLKtKgtH7CACElUp12zXkrPK5UoACLcB/s1600/image00.png) ![inline](https://1.bp.blogspot.com/-tw1WkD2LdBQ/VY07710_e8I/AAAAAAAADI8/4il9OwOizmQ/s1600/partner_ibm.png)

---

#### Dicas
## Acessibilidade

![inline](http://images.apple.com/support/assets/images/products/accessibility/hero_accessibility.png)

---

#### Dicas
## Qual versão de iOS Suportar?

![inline](/Users/salmojunior/Documents/Git Projects/talks/assets/iOSVersions.png)

---

#### Dicas
## Extenda as funcionalidades de sua App

![inline](https://tractusonline.com/wp-content/uploads/2015/09/apple-watch-apps.png)![inline](http://www.imore.com/sites/imore.com/files/styles/large/public/topic_images/2015/apple-tv-4-topic.png?itok=qAEoCCk0)

---

# [fit] Dúvidas?

---

# Obrigado!
## salmo@ciandt.com
### @salmojr
#### https://speakerdeck.com/salmojunior