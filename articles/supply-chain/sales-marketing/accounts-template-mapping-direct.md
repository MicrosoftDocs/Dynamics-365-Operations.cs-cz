---
title: Synchronizace obchodních vztahů přímo z aplikace Sales na odběratele v Supply Chain Management.
description: Toto téma se věnuje šablonám a základní úloze, které se používají k synchronizaci obchodních vztahů z Dynamics 365 Sales do Supply Chain Management.
author: ChristianRytt
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 7948a87c6e40a4d45a23265bbb98a9bef2296974164fc65119b4b6596c81b139
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756864"
---
# <a name="synchronize-accounts-directly-from-sales-to-customers-in-supply-chain-management"></a>Synchronizace obchodních vztahů přímo z aplikace Sales na odběratele v Supply Chain Management.

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> Než budete moci použít řešení Zpeněžnění potenciálního zákazníka, měli byste se seznámit s modulem [Integrace dat do služby Microsoft Dataverse for Apps](/powerapps/administrator/data-integrator).

Toto téma se věnuje šablonám a základní úloze, které se používají k synchronizaci obchodních vztahů přímo z Dynamics 365 Sales do Dynamics 365 Supply Chain Management.

## <a name="data-flow-in-prospect-to-cash"></a>Tok dat ve zpeněžení potenciálního zákazníka

Řešení Zpeněžení potenciálního zákazníka používá funkci Integrace dat k synchronizaci dat mezi instancemi aplikací Supply Chain Management a Sales.  Šablony zpeněžení potenciálního zákazníka dostupné v rámci funkce integrace dat umožňují tok dat účtů, kontaktů, produktů, prodejních kvót, prodejních objednávek a prodejních faktur mezi aplikacemi Supply Chain Management a Sales. Následující obrázek znázorňuje, jak jsou data synchronizována mezi aplikacemi Supply Chain Management a Sales.

[![Tok dat ve zpeněžení potenciálního zákazníka.](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Šablony a úkoly

Chcete-li získat přístup k dostupným šablonám, otevřete [Centrum pro správu Power Apps](https://preview.admin.powerapps.com/dataintegration). Vyberte **Projekty** a v pravém horním rohu vyberte **Nový projekt**, abyste zvolili veřejné šablony.

K synchronizaci účtů z aplikace Sales do aplikace Supply Chain Management slouží následující šablony a základní úkol:

- **Název šablony v integraci dat:** Účty (Sales do Fin and Ops) - Přímo
- **Název úkolu v projektu:** Účty – Odběratelé

Nejsou požadovány žádné úkoly synchronizace, než může dojít k synchronizaci účtu/odběratele.

## <a name="entity-set"></a>Sada entit

| Prodej.    | Správa dodavatelsko-odběratelského řetězce |
|----------|------------------------|
| Účty | Zákazníci V2           |

## <a name="entity-flow"></a>Tok entity

Účty se spravují v aplikaci Sales a synchronizují se do aplikace Supply Chain Management jako odběratelé. Vlastnost **Je externě udržována** těchto odběratelů je nastavena na **Ano** ke sledování odběratelů, kteří pocházejí z aplikace Sales. Při fakturaci tyto informace slouží k filtrování faktur, které budou synchronizovány s aplikací Sales.

## <a name="prospect-to-cash-solution-for-sales"></a>Řešení Potenciální zákazník pro hotovost v aplikaci Sales

Sloupec **Číslo účtu** je dostupný na stránce **Účet**. Slouží jako fyzický a jedinečný klíč k podpoře integrace. Přirozená klíčová funkce řešení řízení vztahů se zákazníky (CRM) může mít vliv na zákazníky, kteří již používají sloupec **číslo účtu**, které však nepoužívá jedinečné hodnoty **Číslo účtu** na účet. V současné době nepodporuje řešení integrace tento případ.

Když je vytvořen nový účet a pokud hodnota **Číslo účtu** ještě neexistuje, je automaticky generováno pomocí číselné řady. Hodnota se skládá z údaje **ACC** a následně dalšího čísla číselné řady, a pak přípony šest znaků. Tady je příklad: **ACC-01000-BVRCPS**

Při použití řešení integrace prodeje nastaví skript pro upgrade sloupec **číslo účtu** pro existující účty v aplikaci Sales. Pokud neexistují žádné hodnoty pro **Číslo účtu**, použije se číselná řada, která byla zmíněna dříve.

## <a name="preconditions-and-mapping-setup"></a>Nastavení mapování a předpokladů

- Mapování **CustomerGroupId** musí být aktualizováno na platnou hodnotu v aplikaci Supply Chain Management. Lze určit výchozí hodnotu nebo můžete nastavit hodnoty pomocí mapování hodnot.

    Výchozí hodnota šablony je **10**.

- Přidáním následujících mapování můžete snížit počet ručních aktualizací, které jsou potřebné v aplikaci Supply Chain Management. Můžete použít výchozí hodnotu nebo mapu hodnot například z pole **Země/oblast** nebo **Město**.

    - **SiteId** – pracoviště je nutné za účelem generování nabídky a řádky prodejní objednávky v aplikaci Supply Chain Management. Výchozí pracoviště lze získávat z produktu nebo od odběratele ze záhlaví objednávky.

        Výchozí hodnota šablony je **1**.

    - **WarehouseId** – sklad je nutný za účelem zpracování nabídek a řádky prodejní objednávky v aplikaci Supply Chain Management. Výchozí sklad lze získat z produktu nebo od odběratele ze záhlaví objednávky aplikace Supply Chain Management.

        Výchozí hodnota šablony je **13**.

    - **LanguageId** – jazyk je nutný za účelem generování nabídek a prodejních objednávek v aplikaci Supply Chain Management. Ve výchozím nastavení se používá jazyk ze záhlaví objednávky od odběratele.

        Výchozí hodnota šablony je **en-us**.

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

> [!NOTE]
> Sloupce **Platební podmínky**, **Dopravní podmínky**, **Dodací podmínky**, **Způsob dopravy** a **Způsob dodání** nejsou zahrnuty do výchozího mapování. Pokud chcete tyto sloupce mapovat, je nutné nastavit mapování hodnoty, které je specifické pro data v organizacích, mezi nimiž je tabulka synchronizována.

Na následujícím obrázku je příklad mapování šablony v integraci dat. 

> [!NOTE]
> Mapování ukazuje, jaké informace o sloupci budou synchronizovány z aplikace Sales do aplikace Supply Chain Management.

![Mapování šablony v integraci dat.](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a>Související témata


[Zpeněžení potenciálního zákazníka](prospect-to-cash.md)

[Synchronizace obchodních vztahů přímo z aplikace Sales na odběratele v Supply Chain Management.](accounts-template-mapping-direct.md)

[Synchronizace kontaktů přímo z aplikace Sales na kontakty nebo odběratele v aplikaci Supply Chain Management](contacts-template-mapping-direct.md)

[Synchronizace prodejních objednávek přímo mezi aplikacemi Sales a Supply Chain Management](sales-order-template-mapping-direct-two-ways.md)

[Synchronizace hlaviček a řádků faktury přímo z aplikace Supply Chain Management do aplikace Sales](sales-invoice-template-mapping-direct.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]