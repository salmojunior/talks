build-lists: true

# Migrando para o desenvolvimento mobile (iOS)

---

## Salmo Junior

Mineiro, Chapter Leader do CocoaHeads BH, dev iOS desde 2011, corintiano e viajante.

![right](../assets/Eu2.png)

<br><br><br><br><br><br><br><br><br>

Sênior iOS Developer at CI&T
salmo@ciandt.com
@salmojr

---

## Agenda

- Guidelines
- Serviços e Armazenamento
- Hardware e Limitações
- Dicas
- Ferramentas

---

## Guidelines

---

#### Guidelines
## Utilização da Main Thread

![inline](https://developer.apple.com/library/content/documentation/iPhone/Conceptual/iPhoneOSProgrammingGuide/Art/event_draw_cycle_a_2x.png)

---

#### Guidelines
## Internacionalização

![inline](https://developer.apple.com/library/ios/documentation/MacOSX/Conceptual/BPInternational/Art/internationalization_intro_2x.png)

---

#### Guidelines
## Interrupções

![inline](https://lh4.googleusercontent.com/5YTB51qpHCe7sQW4rnOA3GfRv2IjvY-6hyusAq9YBvRUQR-xRah4TIBt1UfLEszM7eLXGaNpo3HCBpX7fj7LHU4Gze_4INwWoCpxOzHeX-ipFoWUI-ApKbgiGXUPTHo1myHFN4oMVg) ![inline](https://lh5.googleusercontent.com/GTaLdayR8eyFEw8ivgzlSXvz4i_1aL-3S5QxSUlapaUUDO5qLVEBhZP5zn8gZuHao3NA1W6X9nzSK-l7cNo6VTfMGSTMiWb9m0Sahced61J2GsY7dteyhTzdQsn27s_quqKV-QWmdw)

---

#### Guidelines
## Semantic Versioning 2.0.0 

![inline](https://lh5.googleusercontent.com/IXO28FSczqULIfxNkqmsvuHVbs-5KQ3bMv9oydqPi4hyzQ9IKtcQy2hzJ13zC0ypZKPJ9UzJb_ejy_XRNr-3rOEuf_k3Zj8He-UrYRRSjtexFkTbn8BaxRg-mHlMa27tB213RsIHNQ)

---

#### Guidelines
## Segurança

![inline](https://lh6.googleusercontent.com/HBGTsB_c3wL9uY5yunZeJmzAKyH2AHy5SF25tHO5MzCPMTcaFlrmS-wimtw6ST3hFnarlQ6cIOWmlKwEzx86bhMQad_pGAql9mcXBPFUykjg4pzG6UQIU6Tywc2U8Wq5ImRXNLjlNw) ![inline](http://d.ibtimes.co.uk/en/full/1433208/touch-id.jpg)

---

## Serviços e Armazenamento

---

#### Serviços e Armazenamento
## REST com JSON

- Melhor tempo de resposta
- Objetos mais simples
- Menor processamento

<!--poupando o consumo de dados-->
<!--devido a facilidade de conversão e interpretação-->

![right 50%](http://sahinerbay.com/wordpress/wp-content/uploads/2016/03/JSON.png)

---

#### Serviços e Armazenamento
## Sincronismo de dados

- Tenha conteúdo inicial offline
- Sincronize em background e com antecedência
- Envie os dados da forma mais simplificada possível

![right 100%](../assets/sync.png)

---

#### Serviços e Armazenamento
## Versionamento e tempo de desenvolvimento

![inline](https://lh3.googleusercontent.com/lRSEtZz0dGIBNvhbSklft3uhpz2YOGucOkVupihYQJYQvJ9WCyMXhEQpiwwnhHrYXlWf0LxMMYdbR54ezeW0z-H_8W2VymnMCzGVp95McyPJMt1KT-a9ZrV8ZBL_upgf4R_iF3pCkA)

---

#### Serviços e Armazenamento
## Arquivos

Arquivos não devem ser armazenados direto no banco

![inline 100%](../assets/DB2.png)

---

## Hardware e Limitações

---

#### Hardware e Limitações
## Sensores

Uns dos grandes diferenciais dos smartphones

![inline](https://lh5.googleusercontent.com/sE297ADrqOk5NqnAB64b3xU0HPZEphD6P9SyuN3C8tBJxdl1GZcJ9qW7or-6MSIDMF6_1ilCKbrjevq4jQJ-BrORACmh0R3Bre8RCZSUKrA2SfjiOox9Aa62n8NV-DLnGi9SSAmHkg)

---

#### Hardware e Limitações
## Sensores

Mas também podem ser os grandes vilões

![inline](https://lh3.googleusercontent.com/MwY2t7bxd33eIkM2ZI7uX6sAh63nEWlJIPaCcxbVy-QGqaECTOkHSvifpmdmvOGIUljrzWrs1s9vPOL0LMH6r6JYmQ4M1N2QFcnNZtLjNGA6fQZXy5euCbE77_sS2Ox3rfJH9udFbg)

---

#### Hardware e Limitações
## Sensores 

Utilize de forma consciente

![inline](https://lh6.googleusercontent.com/6uFiHMEOBP2mVOD7MIedJlKogfl0LHDkkhuBUovGW0Rh1fs94sElttqUKUUZ3503zWergHgVhWLpik8w0kK-TZ4pLCgHXyaEWQidl1k9pRCdbfnOmiQs9sQ7PFQwXQXTfUPuX6_UPg)

---

#### Hardware e Limitações
## Uso de banda de internet

- Minimize a quantidade de requisições
- Faça cache sempre que possível
- Verifique o tipo de conexão antes de downloads grandes

![right](http://www.adweek.com/socialtimes/wp-content/uploads/sites/2/2015/09/Phone-Bored.png)

---

#### Hardware e Limitações
## Divisão de tarefas entre Aplicativo e Backend

![inline](https://upload.wikimedia.org/wikipedia/commons/f/fd/Tug_of_war_2.jpg)

<!--- Uma alteração do lado mobile implica no lançamento de uma nova versão
- Tempo de alteração/correção
- Poder de processamento-->

---

#### Hardware e Limitações
## Armazenamento

- Acima de 100MB, download somente com wifi
- Tamanho máximo de 2GB
- Até 20GB de conteúdo usando On-Demand Resouces

![right 70%](https://lh5.googleusercontent.com/sMTo_wtjorzd0NhlzKg-2_hB1jaG7Q_uAgVHTrOV10ydDnsdI40KxBqKYEjVeJbkoikaGjXuhOtug3Td2t1MWrWnG6_vLg18tvp99kAbwDBEbXzHpVK_gzH8-HUL_2tKYVQ0mFQ9Ew)

---

#### Hardware e Limitações
## Armazenamento

![inline 75%](https://lh5.googleusercontent.com/9CEOaBv_8ruScVlgzIIb5-IsmmaiV4992WqkzMu08EqrEyd1u1J3epmOuDcM8PwRMAogzGbGdmlTaA2BK-vqV5mUKdAPoSOmnH2-caJPtSLQzRcSh3heNX5P8Cw56PcF6KDmRNf9eg)

<!--Implementar rotinas para limpar os dados que não estão sendo mais utilizados pelo usuário, como Imagens e PDFs. 

Remover os assets que não são mais utilizados no projeto, sempre que lançar uma nova versão.
-->

---

#### Hardware e Limitações
## Versões de S.O. são lançadas frequentemente

![inline](https://www.smartface.io/wp-content/uploads/2015/01/smartface_ios_android_version_fragmentation-1030x533.png)

---

## Dicas

---

#### Dicas
## Ganhe tempo com qualidade 

![inline](https://1.bp.blogspot.com/-YIfQT6q8ZM4/Vzyq5z1B8HI/AAAAAAAAAAc/UmWSSMLKtKgtH7CACElUp12zXkrPK5UoACLcB/s1600/image00.png) ![inline](https://1.bp.blogspot.com/-tw1WkD2LdBQ/VY07710_e8I/AAAAAAAADI8/4il9OwOizmQ/s1600/partner_ibm.png)

---

#### Dicas
## Qual versão de iOS Suportar?

![inline](../assets/iOSVersions.png)

---

#### Dicas
## Engajamento

![inline](../assets/engagement.png)

---

#### Dicas
## Acessibilidade

![inline 150%](http://images.apple.com/support/assets/images/products/accessibility/hero_accessibility.png)

---

#### Dicas
## Extenda as funcionalidades de sua App

![inline](https://tractusonline.com/wp-content/uploads/2015/09/apple-watch-apps.png)![inline](http://www.imore.com/sites/imore.com/files/styles/large/public/topic_images/2015/apple-tv-4-topic.png?itok=qAEoCCk0)

---

## Ferramentas

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

<br>

![inline 75%](http://core0.staticworld.net/images/article/2014/10/twitter-fabric-logo-100527200-primary.idge.jpg) ![inline 75%](http://media.idownloadblog.com/wp-content/uploads/2014/09/TestFlight-1.0-for-iOS-app-icon-small-220x220.png) ![inline](https://www.cloudbees.com/sites/default/files/hockeyapp_logo.png)

---

# [fit] Dúvidas?

---

# Obrigado!
## salmo@ciandt.com
### @salmojr
#### https://speakerdeck.com/salmojunior
