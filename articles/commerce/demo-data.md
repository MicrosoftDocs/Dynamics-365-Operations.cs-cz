---
title: Rozložení obrazovky ukázkových dat Modern POS (MPOS) a Cloud POS
description: Toto téma poskytuje informace o rozvrženích obrazovky, která jsou zahrnuta se sadou ukázkových dat v uživatelském prostředí pokladních míst (POS) v aplikaci Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 10/05/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2017-10-05
ms.dyn365.ops.version: Retail April 2017 update
ms.openlocfilehash: 935e1a550160515e2c325c39eab86be3b9fa5394
ms.sourcegitcommit: d82f319cf7dd26c93a3fd342de4fd537272fa8d2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2020
ms.locfileid: "4410939"
---
# <a name="demo-data-screen-layouts-in-modern-pos-mpos-and-cloud-pos"></a>Rozložení obrazovky ukázkových dat Modern POS (MPOS) a Cloud POS

[!include [banner](includes/banner.md)]

Toto téma poskytuje informace o rozvrženích obrazovky, která jsou zahrnuta se sadou ukázkových dat v uživatelském prostředí pokladních míst (POS) v aplikaci Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Vzorová rozvržení obrazovky zahrnutá v ukázkových datech Commerce poskytují obsah, který je optimalizován pro různé maloobchodní segmenty, role pracovníků skladu a zařízení. Jedno rozvržení může obsahovat několik velikostí rozvržení a kombinací mřížek tlačítek, aby se zajistilo pokrytí pro případy, kdy se zaměstnanci obchodu pohybují mezi zařízeními a stanicemi. Toto téma zdůrazňuje rozdíly mezi těmito rozloženími, operace, které tato rozložení poskytují, a celkovou uživatelskou zkušenost.

![Rozvržení ukázkových dat mezi zařízeními](../commerce/media/demo-screen-layouts-fig-1-1.png)

## <a name="anatomy-of-a-screen-layout-id"></a>Podrobný rozbor ID rozvržení obrazovky

Chcete-li nalézt rozvržení obrazovky, přejděte na **Retail a Commerce** \> **Nastavení kanálu** \> **Nastavení POS** \> **POS** \> **Rozvržení obrazovky**.

![Stránka rozložení obrazovky](../commerce/media/demo-screen-layouts-fig-2-1.png)

ID rozložení obrazovky může obsahovat maximálně 10 znaků. ID je řetězec, který se skládá ze tří částí informací, v tomto pořadí:

1. Společnost
2. Verze rozvržení
3. Osoba

### <a name="company"></a>Společnost

| Dopis | Společnost         |
|--------|-----------------|
| A      | Adventure Works |
| F      | Fabrikam        |
| o      | Contoso         |

### <a name="layout-version"></a>Verze rozvržení

| Číslo verze | popis                                                                                |
|----------------|--------------------------------------------------------------------------------------------|
| 3              | Základní verze, která podporuje více velikostí obrazovky pro různá zařízení a poměry stran |
| 3.1            | Základní verze, která obsahuje další podporu pro panel **Doporučené produkty**        |
| 4              | Rozšířená verze pro rozšířené aktualizované rozložení Fabrikam                                  |

### <a name="persona"></a>Osoba

| Zkratka | Osoba       | Obsah |
|--------------|---------------|----------|
| CSH          | Pokladník       | Rozvržení pokladníka zahrnuje všechny operace související s transakcí, jako jsou například objednávky odběratele, vrácení, slevy, anulování a dárkové poukazy. Tato rozvržení rovněž zahrnují denní úkoly pro řízení zásob, jako jsou kontroly ceny, vyhledávání zásob a počty na skladě. Je rovněž poskytnuta základní správa směn pro počáteční částky, pozastavení směn a čas. |
| MGR          | Manažer obchodu | Rozvržení manažera obchodu zahrnují všechny operace související s transakcí, které se nacházejí v rozvržení pokladního, ale také zahrnují přepsání daně. Tato rozvržení rovněž zahrnují denní úkoly pro řízení zásob, jako jsou kontroly ceny, vyhledávání zásob a počty na skladě. Správa směn poskytuje spuštění, pozastavení a uzavření směn. Dále rozvržení zahrnuje operace zásuvky pro položky, odebrání, návraty, výkazy úhrad a odvody do trezoru a do banky. Nakonec tato rozložení zahrnují přístup k sestavám výkonnosti a povolují tisk sestav X a Y. |
| STK          | Pracovník skladu   | Rozvržení pracovníka skladu jsou optimalizována pro řízení zásob. Mohou zahrnovat přístup ke každodenním úkolům pro kontroly ceny, vyhledávání zásob, výdej a příjem, počty na skladě a demontáž sady. Tato rozvržení poskytují také základní operace směny pro čas a pozastavení směny. Ačkoliv tato rozvržení slouží zejména pro administrativní úlohy, pracovníci skladu mají k dispozici stejné operace jako pokladníci pro obrazovky transakcí. |

### <a name="example-layout"></a>Příklad rozvržení

Následuje příklad ID rozvržení obrazovky pro společnost Fabrikam, verze rozvržení 4, a osobu manažera obchodu:

F4MGR

Následující obrázek znázorňuje příklad uvítací obrazovky manažera obchodu Fabrikam.

![Uvítací obrazovka pro manažera obchodu Fabrikam](../commerce/media/demo-screen-layouts-fig-2-2.png)

## <a name="layout-sizes"></a>Velikosti rozvržení

### <a name="full-vs-compact-layouts"></a>Úplné a kompaktní rozvržení

Rozvržení obrazovky může mít konfigurace pro úplné i kompaktní zařízení. Uživatel může být přiřazen k jednomu rozvržení obrazovky, které bude fungovat v různých velikostech a formátech v obchodě.

- **Moderní POS - Úplné** - Úplná rozložení jsou obvykle nejvhodnější pro větší displeje, jako mají například PC monitory nebo tablety. Uživatelé mohou vybrat prvky uživatelského rozhraní, které rozvržení zahrnuje, určit velikost a umístění těchto prvků a nakonfigurovat jejich podrobné vlastnosti. Plná rozložení podporují konfigurace na výšku a na šířku.
- **Modern POS - Kompaktní -** - Kompaktní rozložení jsou obvykle nejvhodnější pro telefony a malé tablety. Možnosti návrhu jsou omezeny pro kompaktní zařízení. Uživatelé mohou konfigurovat sloupce a pole pro podokna stvrzenek a součtů.

### <a name="screen-resolutions-that-are-provided"></a>Rozlišení obrazovky, která jsou k dispozici

Následující tabulka zobrazuje velikosti rozvržení, které jsou k dispozici pro typická rozlišení obrazovky.

| Typ rozvržení | Rozlišení | Poměr stran | Cílový displej          |
|-------------|------------|--------------|-------------------------|
| Komprimovat\*   | 480 × 853  | 16:9         | Telefony                  |
| Plné        | 1024 × 768 | 4:3          | Tablety                 |
| Plné\*      | 1280 × 720 | 16:9         | Tablety                 |
| Plné        | 1366 × 768 | 16:9         | Tablety, větší obrazovky |
| Plné        | 1440 × 960 | 3:2          | Tablety, větší obrazovky |
| Plné\*      | 1536 × 864 | 16:9         | Tablety, větší obrazovky |

\* Tyto dodatečné velikosti rozvržení jsou k dispozici pouze v rozvrženích Fabrikam a Adventure Works.

> [!TIP]
> POS automaticky vybere velikost rozvržení, v závislosti na nejbližší velikosti, která je k dispozici pro rozlišení obrazovky aktuálního okna aplikace. Pokud chcete nalézt ID rozvržení obrazovky a rozlišení rozvržení, která jsou aktuálně používána v Modern POS (MPOS) nebo v Retail Cloud POS (CPOS), otevřete stránku **Nastavení** a nahlédněte do části **Informace o relaci**. Můžete také vidět skutečné rozlišení okna vaší aktuální aplikace nebo rámce prohlížeče. Jakmile máte tyto informace, lze vyhledat zdroj obsahu rozvržení přechodem na **Nastavení kanálu** \> **Nastavení POS** \> **POS** \> **Rozvržení obrazovky**.

![Rozvržení obrazovky a rozlišení rozvržení/velikosti v aplikaci Commerce a v POS](../commerce/media/demo-screen-layouts-fig-3-1.png)

## <a name="companies-and-brands"></a>Společnosti a značky

Každá fiktivní společnost je zacílena na jiný maloobchodní segment a obsahuje katalogy produktů, které jsou uzpůsobeny trhu společnosti. Každá společnost používá jedinečnou vizuální značku, která doprovází její produkty. Prvky firemní značky zahrnují barvy zvýraznění, tmavé nebo světlé motivy a průvodní fotografie, poskytující realistický zážitek.

### <a name="company-segment-and-visual-characteristics"></a>Segmenty společnosti a vizuální vlastnosti

| Společnost         | Skl. místo | Segment         | Zvýraznění | Motiv |
|-----------------|----------|----------------|--------|-------|
| Adventure Works | Seattle  | Sportovní zboží | Modrá   | Tmavý  |
| Fabrikam        | San Francisco  | Fashion        | Zelená  | Světlý |
| Contoso         | Boston   | Elektronika    | Červená    | Tmavý  |

> [!NOTE]
> Společnosti Adventure Works a Fabrikam jsou dvě přední značkové společnosti. Contoso je k dispozici, ale nebyla poskytnuta všechna rozvržení.

Následující obrázky ukazují příklady uvítací stránky a stránky transakcí pro tři fiktivní společnosti.

### <a name="adventure-works"></a>Adventure Works

![Uvítací stránka ukázkových dat pro společnost Adventure Works](../commerce/media/demo-screen-layouts-fig-4-1a.png)

![Stránka transakcí ukázkových dat pro společnost Adventure Works](../commerce/media/demo-screen-layouts-fig-4-1b.png)

### <a name="fabrikam"></a>Fabrikam

![Uvítací stránka ukázkových dat pro společnost Fabrikam](../commerce/media/demo-screen-layouts-fig-4-2a.png)

![Stránka transakcí ukázkových dat pro společnost Fabrikam](../commerce/media/demo-screen-layouts-fig-4-2b.png)

### <a name="contoso"></a>Contoso

![Rozvržení ukázkových dat pro společnost Contoso](../commerce/media/demo-screen-layouts-fig-4-3.png)

## <a name="user-sign-in-matrix"></a>Matice přihlášení uživatele

Pro různá rozvržení obrazovky byli zadáni uživatelé. Pomocí následující tabulky byste měli být schopni se dostat na jakoukoliv obrazovku. Pouze se přihlaste pomocí příslušného ID operátora.

| Společnost         | ID rozvržení obrazovky | Osoba       | ID operátora           |
|-----------------|------------------|---------------|------------------------|
| Adventure Works | A3MGR            | Manažer obchodu | 000154, 000137, 000073 |
| Adventure Works | A3CSH            | Pokladník       | 000150, 000175, 000165 |
| Adventure Works | A3STK            | Pracovník skladu   | 000155, 000181, 000152 |
| Fabrikam        | F4MGR            | Manažer obchodu | 000160, 000713         |
| Fabrikam        | F3CSH            | Pokladník       | 000161, 000113, 000114 |
| Fabrikam        | F3STK            | Pracovník skladu   | 000164, 000112, 000123 |
| Contoso         | C3MGR            | Manažer obchodu | 000100, 000111         |
| Contoso         | C3CSH            | Pokladník       | 000110, 000120         |
| Contoso         | Nelze použít   | Pracovník skladu   | Nelze použít         |

> [!TIP]
> Abyste dosáhli nejlepších výsledků, aktivujte pokladnu v odpovídajícím umístění obchodu a nastavte společnosti na společnost osoby, kterou chcete použít při přihlášení. Tímto způsobem zajistíte, že vizuální profil a obrázky týkajíc se značky budou sjednoceny napříč uživatelskými možnostmi. Například pokud chcete zobrazit Fabrikam rozvržení pro pokladníka, musíte aktivovat pokladnu obchodu v Houstonu.

<!-- Hiding until the content page is available on CustomerSource -->

<!-- ## Reference icons and images -->

<!-- The screen layouts, button grids, and visual profiles were created using images and icons that can be found in **Retail and Commerce \> Channel setup \> POS setup \> POS \> Images**. -->

<!-- ![Images in Dynamics 365 Commerce](../commerce/media/demo-screen-layouts-fig-5-1.png) -->

<!-- Use the [POS Icon and Image Mapping](../commerce/media/POS_Icon_and_Image_Mapping.xlsx) reference spreadsheet to locate operation icons, reference photos, swap logos, or provide new images of your own that can be referenced in custom designs. -->

<!-- END HIDDEN CONTENT -->
