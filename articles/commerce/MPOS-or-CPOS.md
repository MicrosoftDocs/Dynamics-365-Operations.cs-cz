---
title: Volba mezi Store Commerce a Cloud POS
description: Toto téma vysvětluje klíčové rozdíly mezi Store Commerce a Cloud POS a popisuje různé faktory, které by maloobchodníci při implementaci Dynamics 365 Commerce měli zvážit, aby zvolili to nejlepší řešení pro své požadavky.
author: jblucher
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-10-12
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b62e1737bc9e3b9d9e25a7a88e693a9aece80776
ms.sourcegitcommit: 836695c0e95d366ba993f34eee30f57191f356d8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/21/2022
ms.locfileid: "8629283"
---
# <a name="choose-between-store-commerce-and-cloud-pos"></a>Volba mezi Store Commerce a Cloud POS

[!include [banner](includes/banner.md)]

Toto téma vysvětluje klíčové rozdíly mezi Store Commerce a Cloud POS a popisuje různé faktory, které by maloobchodníci při implementaci Dynamics 365 Commerce měli zvážit, aby zvolili to nejlepší řešení pro své požadavky. Poskytuje také implementátorům dodatečné tipy a návody pro faktory, které je třeba při nasazení aplikace Dynamics 365 Commerce zvážit. Zrevidováním a dodržováním těchto pokynů v rámci procesu nasazení se mohou implementátoři vyhnout problémům, které by mohly ovlivnit spokojenost nebo výkon uživatele.

## <a name="insights"></a>Přehledy

Commerce poskytuje celou řadu možností topologie a nasazení. Prodejci si mohou zvolit komponenty a konfigurace, které nejlépe splňují jejich obchodní a technologické požadavky. Jeden aspekt implementace, která vyžaduje pečlivé zvážení, je výběr platformy a provedení pro komponentu pokladního místa (POS).

### <a name="pos-platform-and-form-factor-considerations"></a>Zvažování POS platformy a provedení

Commerce podporuje následující POS možnosti:

- Store Commerce pro Microsoft Windows
- Store Commerce pro iOS a Android
- Cloud POS (CPOS), který podporuje prohlížeče Microsoft Edge a Google Chrome
- Modern POS (MPOS) pro Microsoft Windows (Podpora MPOS bude ukončena v říjnu 2023.) 

Ve všech případech POS (Store Commerce a CPOS) sdílejí stejný základní kód aplikace. Tento bod je důležitý z následujících důvodů:

- Uživatelské rozhraní je konzistentní, bez ohledu na platformu nebo provedení.
- Většina funkčních možností je stejných, bez ohledu na platformu nebo provedení. Existují však některé důležité rozdíly. O těchto rozdílech pojednává toto téma.
- V každém obchodě lze varianty POS kombinovat a spouštět souběžně. Například pro své hlavní registrační pokladny může prodejce použít Store Commerce na počítačích se systémem Windows. Prodejce však může doplnit tyto registrační poklady o terminály založené na prohlížeči nebo o mobilní zařízení.
- Přizpůsobení a rozšíření lze snadno použít napříč platformami a provedeními. Vzhledem k tomu, že je základní kód aplikace sdílen, většinu vlastních nastavení lze implementovat jednou, nikoliv vícekrát.

### <a name="store-commerce-vs-cpos"></a>Srovnání Store Commerce a CPOS

Přestože Store Commerce a CPOS jsou převážně stejné, existují některé důležité rozdíly, které je nutné pochopit.

#### <a name="store-commerce"></a>Store Commerce

Store Commerce je desktopová aplikace, která se instaluje a obsluhuje na zařízení.

- **Windows** – Aplikace Store Commerce pro Windows obsahuje celý kód aplikace, Commerce Runtime (CRT) a Hardware Station (HWS).
- **iOS/Android** – Na těchto platformách se aplikace chová jako hostitel pro kód aplikace CPOS. Jinak řečeno, kód aplikace pochází ze serveru CPOS, který je hostován na Commerce Scale Unit. Další informace naleznete v tématu [přehled Commerce Scale Unit](dev-itpro/retail-store-system-begin.md).

#### <a name="cpos"></a>CPOS

Vzhledem k tomu, že CPOS běží v prohlížeči, aplikace není nainstalována na zařízení. Místo toho prohlížeč přistupuje ke kódu aplikace z CPOS serveru. Proto CPOS nemůže přímo přistupovat k hardwaru POS nebo pracovat v offline stavu.

### <a name="store-deployment-considerations"></a>Zvažování při nasazení v obchodu

Kromě platformy a provedení musí prodejci také zvolit možnost nasazení v obchodě. Následující tabulka popisuje konfigurace, které jsou k dispozici pro každou možnost POS.

| Aplikace POS            | Commerce Scale Unit | K dispozici offline | Místní podpora HWS |
|----------------------------|---------------------|-------------------|-------------------|
| Store Commerce pro Windows | Cloud nebo RSSU       | Ano               | Ano               |
| Store Commerce pro Android | Cloud nebo RSSU       | Číslo                | Ano               |
| Store Commerce pro iOS     | Cloud nebo RSSU       | Číslo                | Číslo                |
| Cloud POS                  | Cloud nebo RSSU       | Číslo                | Číslo                |

#### <a name="commerce-scale-unit"></a>Commerce Scale Unit

The Commerce Scale Unit je součást, která hostuje CRT. CRT obsahuje veškerou obchodní logiku, kterou POS používá, a poskytuje přístup k databázi kanálů. Když jsou online, všichni klienti POS v obchodě používají Commerce Scale Unit. Commerce Scale Unit lze nasadit buď do cloudu nebo do obchodu.

#### <a name="offline-mode"></a>Offline režim

Store Commerce pro Windows podporuje režim offline. V offline režimu může POS pokračovat ve zpracování prodeje i v případě, když je odpojen od Commerce Scale Unit. Lze ho poté synchronizovat s databází kanálů po obnovení připojení. Store Commerce používá svou vlastní integrovanou instanci CRT a dočasně používá svůj vlastní místní zdroj dat (offline databázi serveru SQL Server). Další informace o offline funkcích naleznete v tématu [Offline funkce POS](pos-offline-functionality.md).

### <a name="pos-peripheralhardware-considerations"></a>Zvažování periferních zařízení/hardwaru POS

Prodejci musí také přihlížet k tomu, jak POS bude přistupovat k zařízením a periferním zařízením, jako jsou například tiskárny, zásuvky s hotovostí nebo platební terminály. Hardwarové stanice mohou být vyhrazeny pro registrační pokladnu POS nebo sdíleny mezi registračními pokladnami v obchodě.

| Aplikace POS            | Místní HWS OPOS | Síťová příslušenství | Podpora sdíleného HWS |
|----------------------------|----------------|---------------------|--------------------|
| Store Commerce pro Windows | Ano            | Ano                 | Ano                |
| Store Commerce pro Android | Číslo             | Ano                 | Ano                |
| Store Commerce pro iOS     | Číslo             | Číslo                  | Ano                |
| Cloud POS                  | Číslo             | Číslo                  | Ano                |

Další informace o hardwarových stanicích viz [Konfigurace a instalace hardwarové stanice Retail](retail-hardware-station-configuration-installation.md).

## <a name="implementation-considerations"></a>Na co myslet při implementaci

Při plánování POS implementace ve svých obchodech vezměte v úvahu následující informace:

- **Funkční požadavky** – Základní obchodní procesy a možnosti jsou stejné, bez ohledu na platformu, provedení a topologii nasazení. Většina obchodníků nemusí proto zvažovat funkční požadavky při plánování své implementace.
- **Připojení** – Síťová dostupnost (síť \[WAN\] a síť \[LAN\]) je hlavním faktorem, který vyžaduje pečlivé zvážení. Všechny výhody, které řešení hostované na cloudu bez nutnosti lokální instalace přináší, pokud jde o náklady a jednoduchost, se vytratí, pokud není systém k dispozici pro důležité obchodní procesy.

    Pokud není připojení k pro dané zařízení velmi spolehlivé a stálé, nebo pokud není pro obchodníka přijatelný určitý čas odstávky, doporučujeme jednu z následujících možností:

    - Používejte Store Commerce pro Windows a povolte režim offline.
    - Nasaďte místní jednotku Commerce Scale Unit.

    Tyto dvě možnosti se vzájemně nevylučují. Pro většinu spolehlivé topologie mohou obchodníci nasadit místní RSSU ke snížení závislosti na připojení k internetu nebo dostupnosti služby Azure, a rovněž mohou nasadit registrační pokladny POS tam, kde je povolen offline režim, pokud dojde k problému s místním serverem nebo sítí.

- **Hardwarová zařízení/periferní zařízení** – Jedním z důležitých aspektů systému Retail POS je jeho schopnost používat periferní zařízení POS, například tiskárny, zásuvky s hotovostí nebo platební terminály. Ačkoliv všechny dostupné možnosti POS mohou použít periferní zařízení, pouze Store Commerce pro systém Windows je podporuje přímo. Pro všechny jiné aplikace se vyžaduje jedna nebo více hardwarových stanic. I když tento přístup přidá flexibilitu, je třeba nasadit, nakonfigurovat a obsluhovat další komponenty.
- **Systémové požadavky** – Požadavky na systém pro POS se liší. Ujistěte se, že ověříte nejnovější informace před provedením výběru. Například vzhledem k tomu, že CPOS běží v prohlížeči, podporuje širokou škálu operačních systémů. Další informace o systémových požadavcích naleznete v části [Systémové požadavky pro nasazení cloudu](../fin-ops-core/fin-ops/get-started/system-requirements.md).
- **Nasazení a údržba** – Složitost požadavků na nasazení a údržbu se může lišit v závislosti na výběru aplikace a nasazení. Například pro nasazení CPOS hostované na cloudu CPOS nemusíte instalovat a aktualizovat každé zařízení. Proto tento přístup výrazně snižuje složitost a náklady. Pokud však Store Commerce nasadíte na každé registrační pokladně a povolíte offline režim offline, a současně nasadíte sdílené hardwarové stanice, výrazně zvýšíte počet koncových bodů, které je třeba spravovat.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
