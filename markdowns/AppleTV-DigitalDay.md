<!-- build-lists: true -->

# Criando aplicativos para a nova Apple TV

---

## Salmo Junior

Mineiro, Chapter Leader do CocoaHeads BH, dev iOS desde 2011, corinthiano, viajante e viciado em queijo.

![right](../assets/eu.png)

<br><br><br><br><br><br><br><br><br><br><br><br><br>

salmo@ciandt.com
@salmojr

---

## Agenda

- Overview
- Interação com Usuário
- Design Guidelines
- Focus API
- On-Demand Resources
- TVMLKit
- Dicas

---

# Overview

---

![](../assets/AppleTVApps.png)

---

![](http://media.148apps.com/screenshots/919000809/us-appletv-1-zova-personal-trainer.png)

---

![](http://tock.cdn.assets.watchaware.com/wp-content/uploads/2015/10/zova.png)

---

![](https://static-s.aa-cdn.net/img/appletv/50600001000193/58715296bbee4114f05cccff36078072)

---

![](http://media.148apps.com/screenshots/1042117856/us-appletv-2-gilt-on-tv.png)

---

![](http://media.148apps.com/screenshots/533379666/us-appletv-1-madefire-comics-and-motion-books.png)

---

![](https://i.ytimg.com/vi/H4iMslz3VwY/maxresdefault.jpg)

---

## Apple TV

- Lançamento Set/2015
- Novo S.O. (tvOS)
- Experiencia personalizada
- Acessibilidade
- Developer Tools
- App Store

![right 60%](https://brused.com.br/blog/wp-content/uploads/2016/06/apple-tv.png)

---

## Hardware

- 64-bit processador A8
- 32 GB ou 64 GB
- 2 GB de RAM
- 1080p
- HDMI

![right 60%](https://brused.com.br/blog/wp-content/uploads/2016/06/apple-tv.png)

---

## tvOS 

Desenvolvimento

- SDK separado
- 64-bit com bitcode
- Universal Purchase
- Não necessita suporte à versões anteriores

---

## tvOS 

Desenvolvimento

- UIKit
- TVMLKit
- Swift / Objective-C / TVML / TVJS

---

## tvOS

Experiencia de uso

- Interação baseada em foco
- Utilizacão em família
- Device compartilhado

---

## tvOS

Sempre conectado

- Live Streaming
- On-Demand Resources
- Cloud Storage

---

## tvOS

Armazenamento de dados

- Armazenamento local limitado
- Não há garantia que as informações vão continuar no device na próxima vez que foi utilizado
- A pasta Documents existe, mas não tem permissão de escrita

![100% right](../assets/cloud.png)

---

## tvOS

Armazenamento de dados

- iCloud Key-Value Storage
- CloudKit
- Cloud Storage desejado

![100% right](../assets/cloud.png)

---

# Interação com Usuário

---

## Navegação

- Use gestos para dar fluidez
- Implemente o Voltar através do botão Menu
- Não exiba opção de Voltar
- Dar preferencia para navegação horizontal
- Use a navegação padrão dos compoentes

![right 40% autoplay loop](https://developer.apple.com/tvos/human-interface-guidelines/user-interaction/images/navigation-and-focus-fluidity.mp4)

---

## Foco e Seleção

- Deixe nítido qual item está selecionado
- Implemente comportamento para diferentes status
- Nunca mostre um cursos

![right 80%](https://developer.apple.com/tvos/human-interface-guidelines/user-interaction/images/user-interaction-focus.png)

---

## Carregando conteúdo

- Deixe claro quando estiver carregando novos conteúdos
- Aproveite esse tempo para ensinar o usuário

![right 80%](https://developer.apple.com/tvos/human-interface-guidelines/user-interaction/images/user-interaction-loading-instruction.png)

---

## Carregando conteúdo

Customize suas telas de loading

![right autoplay loop 80%](https://developer.apple.com/tvos/human-interface-guidelines/user-interaction/images/user-interaction-progress-explicit.mp4)

---

## Carregando conteúdo

Exiba sua tela o mais rápido possível, não faça o usuário esperar até que todo o conteúdo seja baixado.

![right 80%](https://developer.apple.com/tvos/human-interface-guidelines/user-interaction/images/user-interaction-placeholder-content.png)

---

## Autenticação

- Retarde ao máximo possível o sign-in
- Evite o input de texto
- Mantenha suporte a multiplos perfis

![right 105%](http://core0.staticworld.net/images/article/2015/10/apple_id-100625201-large.png)

---

## Top Shelf

![inline](https://developer.apple.com/tvos/human-interface-guidelines/icons-and-images/images/icons-and-images-static-image.png)

---

## Top Shelf

Faça uso dos conteúdos dinâmicos

- Atalhos 
- Exibir favoritos
- Mostre conteúdo atrativo
- Não usar para propagandas e ofertas com preços

---

## Top Shelf

Sectioned Content Row

- Necessário conteúdo suficiente para completar uma linha

![right 80%](https://developer.apple.com/tvos/human-interface-guidelines/icons-and-images/images/icons-and-images-content-row.png)

---

## Top Shelf

Scrolling Inset Banner 

- Necessário entre 3 e 8 imagens
- Textos somente dentro da imagem
- Scroll automatico entre os banners

![right 80%](http://developer.apple.com/tvos/human-interface-guidelines/icons-and-images/images/icons-and-images-scrolling-inset.png)

---

## New Siri Remote /<br>Apple TV Remote

![right 60%](https://developer.apple.com/tvos/human-interface-guidelines/remote-and-controllers/images/remote-and-interaction-remote_2x.png)

---

## Botões

- Implemente o comportamento esperado para cada botão
- Volume, Siri e Home são botões restritos

![right](http://cdn2.knowyourmobile.com/sites/knowyourmobilecom/files/2015/11/siri_remote.jpg)

---

## Gestos

``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` Swipe ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` Click ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` ``` Tap 


![inline autoplay loop](https://developer.apple.com/tvos/human-interface-guidelines/remote-and-controllers/images/swipe.mp4) ![inline autoplay loop](https://developer.apple.com/tvos/human-interface-guidelines/remote-and-controllers/images/click.mp4) ![inline autoplay loop](https://developer.apple.com/tvos/human-interface-guidelines/remote-and-controllers/images/tap.mp4)

---

## Acelerômetro e Giroscópio

![inline](http://static3.techinsider.io/image/562fa8bdbd86ef1b008c5192-1920-1080/screen%20shot%202015-10-27%20at%2012.38.30%20pm.png)

---

# Design Guidelines

---

## Otimize seus assets para tela grande

- Desenvolva para resolução de 1920x1080
- Assets somente @1x
- Teste suas imagens na TV

![right 120%](https://developer.apple.com/tvos/human-interface-guidelines/visual-design/images/visual-design-16x9.png)

---

## Mantenha seu conteúdo principal distante das bordas

- 60 píxeis para Top e Bottom
- 90 píxeis para os lados

![right 120%](https://developer.apple.com/tvos/human-interface-guidelines/visual-design/images/visual-design-safe-zone.png)

---

## Mantenha distância entre elementos

Com UIKit e Focus API, elementos de UI ficam maiores ao receber o foco.

![right 120%](https://developer.apple.com/tvos/human-interface-guidelines/visual-design/images/visual-design-padding.png)

---

## Mostre partes de elementos escondidos

Indique sempre que existe mais conteúdo fora area da tela, facilitando assim o acesso pelo usuário.

![right 120%](https://developer.apple.com/tvos/human-interface-guidelines/visual-design/images/visual-design-peeking.png)

---

## Faça uso de Grids

- Fácil de encontrar conteúdo a distância
- Rápido de navegar com o controle

![right 80%](https://developer.apple.com/tvos/human-interface-guidelines/visual-design/images/visual-design-grid-3-column.png)

---

## Parallax

Use parallax para tornar itens com foco ainda mais responsiveis a interação do usuário.

Extensões:

- .lsr
- .lcr

![right](http://designmodo.com/demo/apple-tv-parallax/apple-tv-poster.gif)

---

## Parallax Tools

- Parallax Previewer para macOS
- Parallax Exporter Plug-In para Adobe Photoshop
- Xcode

![right 50%](https://7c8767f40fd77b0a0655-213ce4ca2fa294c548547246ac17375c.ssl.cf1.rackcdn.com/parallax.jpg)

---

## Criando imagens LSR pelo Xcode

- Basta adicionar seus PNGs no Assets Catalog e organizá-las usando o menu esquerdo.
- É possível exportar a imagem em formato LSR
- E também adicionar um arquivo LSR direto ao projeto


![right 95%](https://developer.apple.com/library/tvos/documentation/General/Conceptual/AppleTV_PG/Art/xcodeimages_2x.png)

---

## Criando imagens LCR pelo Xcode

Para usar parallax em imagens fora do Bundle da app, é preciso converte-las para o formato .lcr

Basta usar a `layerutil` command-line tool que vem instalada junto com o Xcode.

```
xcrun —-sdk appletvos layerutil —-c <filename.lsr>
```

---

## Ícone

- Crie ícones com apenas um foco de atenção
- Mantenha o background simples
- Use texto somente quando for essencial ou parte do logo
- Mantenha as bordas do ícone quadradas

![right 80%](https://developer.apple.com/tvos/human-interface-guidelines/icons-and-images/images/icons-and-images-app-icon-grid.png)

---

## Ícone

É preciso prover dois tamanhos de ícones

- Apple TV Home Screen

	- 400 X 240 px

- App Store
	
	- 1280 X 768 px

![right 100%](../assets/AppSize.png)

---

## Ícone

Seu ícone deve ter entre 2 e 5 camadas para dar a sensação de profundidade e vitalidae quando estiver em foco.


![right 100%](https://developer.apple.com/tvos/human-interface-guidelines/icons-and-images/images/icons-and-images-icon-structure.png)

---

# Focus API

---

## Focus API

Introdução....
 
![right]()

---

## Focus API

### 

- 
 
![right]()

---

## Focus API

Preferred Focus

- 
 
![right]()

---

## Focus API

### 

- 
 
![right autoplay loop 40%](https://developer.apple.com/tvos/human-interface-guidelines/user-interaction/images/navigation-and-focus-tilt-screen.mp4)

---

## Focus API

Restoring Focus

- 
 
![right]()

---

# On-Demand Resources

---

## On-Demand Resources

Recurso lançado no iOS 9 que permite armazenar conteúdo na App Store, separado do bundle da aplicação.

Conteúdo baixado somente quando necessário.

![100% right](../assets/ondemand.png)

---

## On-Demand Resources

Por que usar?

- Aplicativo disponível para uso em poucos segundos
- Armazenamento remoto de arquivos raramente usados
- Armazenamento remote de arquivo in-app purchase

![inline](https://developer.apple.com/library/ios/documentation/FileManagement/Conceptual/On_Demand_Resources_Guide/Art/adventure_odr_2x.png)

---

## On-Demand Resources

Por que usar para tvOS?

- App de no máximo 200mb para a App Store
- Apple TV não permite armazenamento local de dados
- Device conectado 100% do tempo

---

## On-Demand Resources

Os arquivos podem ser divididos em 3 tipos de tags

- Initial install
- Prefetch
- On demand

---

## On-Demand Resources

Limites

![inline](../assets/on-demand-resources.jpg)

---

## On-Demand Resources

Boas práticas

- Tente criar tags de no máximo 64mb
- Baixe sempre com antecedência
- Descarte os arquivos quando não forem mais necessários

---

## On-Demand Resources

Habilitando ODR no Xcode

![inline](https://developer.apple.com/library/ios/documentation/FileManagement/Conceptual/On_Demand_Resources_Guide/Art/ODR_Enabling_ODR_2x.png)

---

## On-Demand Resources

Criando tags

![inline](https://developer.apple.com/library/ios/documentation/FileManagement/Conceptual/On_Demand_Resources_Guide/Art/ODR_Resource_Tags_Pane_Prefetch_2x.png)

---

## On-Demand Resources

Use a classe **NSBundleResourceRequest** para

- Requisitar/Descartar on-demand resources
- Atualizar a prioridade dos downloads
- Acompanhar progresso de download
- Receber notificação de falta de espaço em disco

---

# TVMLKit

---

## TVMLKit

Usado para criar aplicações Client-Server.

É composto pela combinação de 3 frameworks

- TVML
- TVMLKit JS
- TVMLKit

![right 90%](http://devstreaming.apple.com/videos/wwdc/2016/212s41rh77qgdg26s86/212/images/212_734x413.jpg)

---

## TVMLKit

Aplicação Client-Server

![inline 65%](https://developer.apple.com/library/tvos/documentation/General/Conceptual/AppleTV_PG/Art/flow_diagram_2x.png)

---

## TVMLKit

Fluxo de uma aplicação 
Client-Server

<br>
#### Para garantir que todas últimas alterações estejam visiveis para o usuário, adicione sempre `Cache-Control:no-cache` no header de response da sua requisição HTTP.

![right 75%](https://developer.apple.com/library/tvos/documentation/General/Conceptual/AppleTV_PG/Art/flow_diagram2_2x.png)

---

# Dicas

---

## Dark Appearence

- Adote os dois modos
- Adicione imagens diferentes caso necessário
- Somente a partir do iOS 10

![right 70%](http://images.apple.com/v/tv/f/images/overview/tvos_update_tv_large.jpg)

---

## Dark Appearence

![inline](http://media.idownloadblog.com/wp-content/uploads/2016/07/tvOS-10-Settings-Light-Mode-Apple-TV-screenshot-001.jpg) ![inline](http://media.idownloadblog.com/wp-content/uploads/2016/07/tvOS-10-Settings-Dark-Mode-Apple-TV-screenshot-001.jpg)

---

## HomeKit

![inline](../assets/AppleTVHomeKit.png)

---

## VoiceOver

![inline](../assets/AppleTVVoiceOver.png)

---

# Referências

**Apple TV Tech Talks**

[https://developer.apple.com/videos/techtalks-apple-tv/](https://developer.apple.com/videos/techtalks-apple-tv/)

**WWDC 2016**

[https://developer.apple.com/videos/wwdc2016](https://developer.apple.com/videos/wwdc2016)

---

# Dúvidas?

---

# Obrigado!
## salmo@ciandt.com
### @salmojr