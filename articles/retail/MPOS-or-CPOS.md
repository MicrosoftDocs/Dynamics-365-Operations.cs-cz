---
title: "Výběr mezi Modern POS a Cloud POS"
description: "Toto téma vysvětluje klíčové rozdíly mezi Retail Modern POS a Cloud POS. Také popisuje různé faktory, které prodejci implementující aplikaci Microsoft Dynamics 365 for Retail musí zvážit, aby mohli vytěžit pro své požadavky maximum."
author: jblucher
manager: AnnBe
ms.date: 10/12/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-10-12
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7efda507ad826b7765431e6cbdd78c3c9246bc7c
ms.openlocfilehash: 03b7b4d468e35c7b77cf2a2e52c038c0995c7f53
ms.contentlocale: cs-cz
ms.lasthandoff: 12/08/2017

---

# <a name="choose-between-modern-pos-and-cloud-pos"></a>Výběr mezi Modern POS a Cloud POS

[!include[banner](includes/banner.md)]

Toto téma poskytuje implementátorům dodatečné tipy a návody pro faktory, které je třeba při nasazení aplikace Microsoft Dynamics 365 for Retail zvážit. Zrevidováním a dodržováním těchto pokynů v rámci procesu nasazení se mohou implementátoři vyhnout problémům, které by mohly ovlivnit spokojenost nebo výkon uživatele.

## <a name="insights"></a>Informace
Retail poskytuje celou řadu možností topologie a nasazení. Prodejci si mohou zvolit komponenty a konfigurace, které nejlépe splňují jejich obchodní a technologické požadavky. Jeden aspekt implementace, která vyžaduje pečlivé zvážení, je výběr platformy a provedení pro komponentu pokladního místa (POS).

### <a name="pos-platform-and-form-factor-considerations"></a>Zvažování POS platformy a provedení
Retail podporuje následující POS možnosti:

- Retail Modern POS (MPOS) pro Microsoft Windows
- MPOS pro Microsoft Windows Phone
- MPOS pro Apple iPad nebo Google Android tablet
- Cloud POS (CPOS), který podporuje prohlížeče Microsoft Edge, Internet Explorer a Google Chrome

Ve všech případech POS (MPOS a CPOS) sdílí stejný základní kód aplikace. Tento bod je důležitý z následujících důvodů:

- Uživatelské rozhraní je konzistentní, bez ohledu na platformu nebo provedení.
- Většina funkčních možností je stejných, bez ohledu na platformu nebo provedení. Existují však některé důležité rozdíly. O těchto rozdílech pojednává toto téma.
- V konkrétním obchodě lze varianty POS kombinovat a spouštět souběžně. Například pro své hlavní registrační pokladny může prodejce použít MPOS na počítačích se systémem Windows. Prodejce však může doplnit tyto registrační poklady o terminály založené na prohlížeči nebo o mobilní zařízení.
- Přizpůsobení a rozšíření lze snadno použít napříč platformami a provedeními. Vzhledem k tomu, že je základní kód aplikace sdílen, většinu vlastních nastavení lze implementovat jednou, nikoliv vícekrát.

### <a name="mpos-vs-cpos"></a>MPOS a CPOS
Přestože MPOS a CPOS jsou převážně stejné, existují některé důležité rozdíly, které je nutné pochopit.

#### <a name="mpos"></a>MPOS

MPOS na zařízeních se systémem Windows, iOS nebo Android je aplikace, která je zabalená, nainstalována a servisovaná na takovém zařízení.

- **Windows** – MPOS pro aplikaci Windows obsahuje celý kód aplikace a integrovanou službu commerce runtime (CRT). 
- **iOS/Android** – Na těchto platformách se aplikace chová jako hostitel pro kód aplikace CPOS. Jinak řečeno, kód aplikace pochází z CPOS serveru na Microsoft Azure or the Retail Store Scale Unit (RSSU). Další informace naleznete v tématu [přehled Retail Store Scale Unit](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/dev-itpro/retail-store-system-begin).

#### <a name="cpos"></a>CPOS

Vzhledem k tomu, že CPOS běží v prohlížeči, aplikace není nainstalována na zařízení. Místo toho prohlížeč přistupuje ke kódu aplikace z CPOS serveru. Proto CPOS nemůže přímo přistupovat k hardwaru POS nebo pracovat v offline stavu.

### <a name="store-deployment-considerations"></a>Zvažování při nasazení v obchodu
Kromě platformy a provedení musí prodejci také zvolit možnost nasazení v obchodě. Následující tabulka popisuje konfigurace, které jsou k dispozici pro každou možnost POS.

| Aplikace POS         | Server maloobchodu | K dispozici offline |
|-------------------------|---------------|-------------------|
| MPOS pro Windows        | Cloud nebo RSSU | Ano               |
| MPOS pro iOS nebo Android | Cloud nebo RSSU | Žádný                |
| Cloud POS               | Cloud nebo RSSU | Žádný                |

#### <a name="retail-server"></a>Server maloobchodu

Retail Server je komponenta, která je hostitelem CRT. CRT obsahuje veškerou obchodní logiku, kterou POS používá, a poskytuje přístup k databázi kanálů. Když jsou online, všichni klienti POS v obchodě používají Retail Server. Retail Server lze nasadit buď do cloudu nebo do obchodu (RSSU).

#### <a name="offline-mode"></a>Offline režim

MPOS pro systém Windows podporuje offline režim. V offline režimu může POS pokračovat ve zpracování prodeje i v případě, když je odpojen od serveru Retail Server. Lze ho poté synchronizovat s databází kanálů po obnovení připojení. MPOS používá svou vlastní integrovanou instanci CRT a dočasně používá svůj vlastní místní zdroj dat (offline databázi serveru SQL Server). Další informace o offline funkcích naleznete v tématu [Offline funkce POS](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/pos-offline-functionality).

### <a name="pos-peripheralhardware-considerations"></a>Zvažování periferních zařízení/hardwaru POS
Prodejci musí také přihlížet k tomu, jak POS bude přistupovat k zařízením a periferním zařízením, jako jsou například tiskárny, zásuvky s hotovostí nebo platební terminály. Pouze MPOS pro systém Windows podporuje přímou komunikaci s těmito zařízeními. MPOS pro Windows Phone, iOS nebo Android a Cloud POS vyžadují hardwarovou stanici, aby mohly přistupovat k těmto zařízením. Hardwarové stanice mohou být vyhrazeny pro registrační pokladnu POS nebo sdíleny mezi registračními pokladnami v obchodě. Další informace o hardwarových stanicích viz [Konfigurace a instalace hardwarové stanice Retail](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/retail-hardware-station-configuration-installation).

## <a name="implementation-considerations"></a>Na co myslet při implementaci
Při plánování POS implementace ve svých maloobchodech vezměte v úvahu následující informace:

- **Funkční požadavky** – Základní obchodní procesy a možnosti jsou stejné, bez ohledu na platformu, provedení a topologii nasazení. Většina obchodníků nemusí proto zvažovat funkční požadavky při plánování své implementace.
- **Připojení** - Síťová dostupnost (síť \[WAN\] a síť \[LAN\]) je hlavním faktorem, který vyžaduje pečlivé zvážení. Všechny výhody, které řešení hostované na cloudu bez nutnosti lokální instalace přináší, pokud jde o náklady a jednoduchost, se vytratí, pokud není systém k dispozici pro důležité obchodní procesy.

    Pokud není připojení k pro dané zařízení velmi spolehlivé a stálé, nebo pokud není pro obchodníka přijatelný určitý čas odstávky, doporučujeme jednu z následujících možností:

    - Použít MPOS v systému Windows a povolit offline režim.
    - Nasadit místní RSSU.

    Tyto dvě možnosti se vzájemně nevylučují. Pro většinu spolehlivé topologie mohou obchodníci nasadit místní RSSU ke snížení závislosti na připojení k internetu nebo dostupnosti služby Azure, a rovněž mohou nasadit registrační pokladny POS tam, kde je povolen offline režim, pokud dojde k problému s místním serverem nebo sítí.

- **Hardwarová zařízení/periferní zařízení** – Jedním z důležitých aspektů systému Retail POS je jeho schopnost používat periferní zařízení POS, například tiskárny, zásuvky s hotovostí nebo platební terminály. Ačkoliv všechny dostupné možnosti POS mohou použít periferní zařízení, pouze MPOS pro systém Windows je podporuje přímo. Pro všechny jiné aplikace se vyžaduje jedna nebo více hardwarových stanic. I když tento přístup přidá flexibilitu, je třeba nasadit, nakonfigurovat a obsluhovat další komponenty.
- **Systémové požadavky** – Požadavky na systém pro POS se liší. Ujistěte se, že ověříte nejnovější informace před provedením výběru. Například vzhledem k tomu, že CPOS běží v prohlížeči, podporuje širokou škálu operačních systémů. Další informace o systémových požadavcích naleznete v části [Systémové požadavky pro nasazení cloudu](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/system-requirements).
- **Nasazení a údržba** – Složitost požadavků na nasazení a údržbu se může lišit v závislosti na výběru aplikace a nasazení. Například pro nasazení CPOS hostované na cloudu CPOS nemusíte instalovat a aktualizovat každé zařízení. Proto tento přístup výrazně snižuje složitost a náklady. Pokud však MPOS nasadíte na každé registrační pokladně a povolíte offline režim offline, a současně nasadíte sdílené hardwarové stanice, výrazně zvýšíte počet koncových bodů, které je třeba spravovat.

