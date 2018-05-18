---
title: "Synchronizace účtů přímo z aplikace Sales na odběratele v aplikaci Finance and Operations"
description: "Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci účtů z aplikace Microsoft Dynamics 365 for Sales do aplikace Microsoft Dynamics 365 for Finance and Operations."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: fb694db32638756328623c186594cf5ba2e7d6b8
ms.contentlocale: cs-cz
ms.lasthandoff: 03/26/2018

---

# <a name="synchronize-accounts-directly-from-sales-to-customers-in-finance-and-operations"></a>Synchronizace obchodních vztahů přímo z aplikace Sales na odběratele v aplikaci Finance and Operations

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Než budete moci použít řešení Zpeněžnění potenciálního zákazníka, měli byste se seznámit s modulem [Integrace dat Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration).

Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci účtů přímo z aplikace Microsoft Dynamics 365 for Sales do aplikace Microsoft Dynamics 365 for Finance and Operations.

## <a name="data-flow-in-prospect-to-cash"></a>Tok dat ve zpeněžení potenciálního zákazníka

Řešení Zpeněžení potenciálního zákazníka používá funkci Integrace dat k synchronizaci dat mezi instancemi aplikací Finance and Operations a Sales.  Šablony zpeněžení potenciálního zákazníka dostupné v rámci funkce integrace dat umožňují tok dat účtů, kontaktů, produktů, prodejních kvót, prodejních objednávek a prodejních faktur mezi aplikacemi Finance and Operations a Sales. Následující obrázek znázorňuje, jak jsou data synchronizována mezi aplikacemi Finance and Operations a Sales.

[![Tok dat ve zpeněžení potenciálního zákazníka](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Šablony a úkoly

Chcete-li získat přístup k dostupným šablonám, otevřete [Centrum pro správu PowerApps](https://preview.admin.powerapps.com/dataintegration). Vyberte **Projekty**a v pravém horním rohu vyberte **Nový projekt**, abyste zvolili veřejné šablony.

K synchronizaci účtů z aplikace Sales do aplikace Finance and Operations slouží následující šablony a základní úkol:

- **Název šablony v integraci dat:** Účty (Sales do Fin and Ops) - Přímo
- **Název úkolu v projektu:** Účty – Odběratelé

Nejsou požadovány žádné úkoly synchronizace, než může dojít k synchronizaci účtu/odběratele.

## <a name="entity-set"></a>Sada entit

| Prodej.    | Finance and Operations |
|----------|------------------------|
| Účty | Zákazníci V2           |

## <a name="entity-flow"></a>Tok entity

Účty se spravují v aplikaci Sales a synchronizují se do aplikace Finance and Operations jako odběratelé. Vlastnost **Je externě udržována** těchto odběratelů je nastavena na **Ano** ke sledování odběratelů, kteří pocházejí z aplikace Sales. Při fakturaci tyto informace slouží k filtrování faktur, které budou synchronizovány s aplikací Sales.

## <a name="prospect-to-cash-solution-for-sales"></a>Řešení Potenciální zákazník pro hotovost v aplikaci Sales

Pole **Číslo účtu** je k dispozici na stránce **Účet**. Slouží jako fyzický a jedinečný klíč k podpoře integrace. Přirozená klíčová funkce řešení řízení vztahů se zákazníky (CRM) může mít vliv na zákazníky, kteří již používají pole **číslo účtu**, které však nepoužívá jedinečné hodnoty **Číslo účtu** na účet. V současné době nepodporuje řešení integrace tento případ.

Když je vytvořen nový účet a pokud hodnota **Číslo účtu** ještě neexistuje, je automaticky generováno pomocí číselné řady. Hodnota se skládá z údaje **ACC** a následně dalšího čísla číselné řady, a pak přípony šest znaků. Tady je příklad: **ACC-01000-BVRCPS**

Při použití řešení integrace prodeje nastaví skript pro upgrade pole **číslo účtu** pole existující účty v aplikaci Sales. Pokud neexistují žádné hodnoty pro **Číslo účtu**, použije se číselná řada, která byla zmíněna dříve.

## <a name="preconditions-and-mapping-setup"></a>Nastavení mapování a předpokladů

- Mapování **CustomerGroupId** musí být aktualizováno na platnou hodnotu v aplikaci Finance and Operations. Lze určit výchozí hodnotu nebo můžete nastavit hodnoty pomocí mapování hodnot.

    Výchozí hodnota šablony je **10**.

- Přidáním následujících mapování můžete snížit počet ručních aktualizací, které jsou potřebné v aplikaci Finance and Operations. Můžete použít výchozí hodnotu nebo mapu hodnot například z pole **Země/oblast** nebo **Město**.

    - **SiteId** – pracoviště je nutné za účelem generování nabídky a řádky prodejní objednávky v aplikaci Finance and Operations. Výchozí pracoviště lze získávat z produktu nebo od odběratele ze záhlaví objednávky.

        Výchozí hodnota šablony je **1**.

    - **WarehouseId** – sklad je nutný za účelem zpracování nabídek a řádky prodejní objednávky v aplikaci Finance and Operations. Výchozí sklad lze získat z produktu nebo od odběratele ze záhlaví objednávky aplikace Finance and Operations.

        Výchozí hodnota šablony je **13**.

    - **LanguageId** – jazyk je nutný za účelem generování nabídek a prodejních objednávek v aplikaci Finance and Operations. Ve výchozím nastavení se používá jazyk ze záhlaví objednávky od odběratele.

        Výchozí hodnota šablony je **en-us**.

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

> [!NOTE]
> Pole **Platební podmínky**, **Dopravní podmínky**, **Dodací podmínky**, **způsob dopravy** a **způsob dodání** nejsou zahrnuta do výchozího mapování. Pokud chcete tato pole mapovat, je nutné nastavit mapování hodnoty, které je specifické pro data v organizacích, mezi nimiž je entita synchronizována.

Na následujícím obrázku je příklad mapování šablony v integraci dat. 

> [!NOTE]
> Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Sales do aplikace Finance and Operations.

![Mapování šablony v integraci dat](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a>Související témata


[zpeněžení potenciálního zákazníka](prospect-to-cash.md)

[Synchronizace účtů přímo z aplikace Sales na odběratele v aplikaci Finance and Operations](accounts-template-mapping-direct.md)

[Synchronizace kontaktů přímo z aplikace Sales na kontakty nebo odběratele v aplikaci Finance and Operations](contacts-template-mapping-direct.md)

[Synchronizace hlaviček a řádků prodejní objednávky přímo z aplikace Finance and Operations do Sales](sales-order-template-mapping-direct-two-ways.md)

[Synchronizace hlaviček a řádků prodejní faktury přímo z aplikace Finance and Operations do Sales](sales-invoice-template-mapping-direct.md)


