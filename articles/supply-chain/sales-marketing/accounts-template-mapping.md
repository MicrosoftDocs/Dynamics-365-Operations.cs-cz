---
title: "Synchronizace obchodních vztahů z aplikace Sales na odběratele v aplikaci Finance and Operations"
description: "Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci obchodních vztahů z aplikace Microsoft Dynamics 365 for Sales do aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1fdbeaaba53cd439d9872be78b1cf67cbc5a57b9
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-accounts-from-sales-to-customers-in-finance-and-operations"></a>Synchronizace obchodních vztahů z aplikace Sales na odběratele v aplikaci Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Než budete moci použít řešení Zpeněžnění potenciálního zákazníka, seznamte se s modulem [Integrace dat Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration). 

Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci účtů z aplikace Microsoft Dynamics 365 for Sales (Sales) do aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (Finance and Operations).

## <a name="template-and-task"></a>Šablona a úkol

K synchronizaci účtů a řádků prodejních nabídek v aplikaci Finance and Operations slouží následující šablony a základní úkoly:

- **Název šablony:** Accounts (Sales to Fin and Ops)
- **Název úkolu do projektu:** účty – účet – Odběratelé

Synchronizace úkolů vyžadovaných před synchronizací Účet / Odběratel

## <a name="entity-set"></a>Sada entit

| Prodej.    | CDS     | Finance and Operations |
|----------|---------|------------------------|
| Účty | Účet | Zákazníci              |

## <a name="entity-flow"></a>Tok entity

Účty se spravují v aplikaci Sales a synchronizují s aplikací Finance and Operations jako zákazníci. Vlastnost **Je externě udržována** těchto odběratelů je nastavena na **Ano** ke sledování odběratelů, kteří pocházejí z prodeje. Při fakturaci tyto informace slouží k filtrování faktur, které budou synchronizovány s aplikací Sales.

## <a name="prospect-to-cash-solution-for-sales"></a>Řešení Potenciální zákazník pro hotovost v aplikaci Sales

Pole **Číslo účtu** je k dispozici na stránce **Účet**. Slouží jako fyzický a jedinečný klíč k podpoře integrace. Přirozená klíčová funkce řešení řízení vztahů se zákazníky (CRM) může mít vliv na zákazníky, kteří již používají pole **číslo účtu**, které však nepoužívá jedinečné hodnoty **Číslo účtu** na účet. V současné době nepodporuje řešení integrace tento případ.

Když je vytvořen nový účet a pokud hodnota **Číslo účtu** ještě neexistuje, je automaticky generováno pomocí číselné řady. Hodnota se skládá z údaje **ACC** a následně dalšího čísla číselné řady, a pak přípony šest znaků. Tady je příklad: **ACC-01000-BVRCPS**

Při použití řešení integrace prodeje nastaví skript pro upgrade pole **číslo účtu** pole existující účty v aplikaci Sales. Pokud neexistují žádné hodnoty **Číslo účtu**, použije se číselná řada, která byla uvedena dříve.

## <a name="preconditions-and-mapping-setup"></a>Nastavení mapování a předpokladů

- **CustomerGroupId** mapování z **CDS &gt; Cíl** musí být v aplikaci Finance and Operations aktualizováno na platnou hodnotu. Lze určit výchozí hodnotu nebo můžete nastavit hodnoty pomocí mapování hodnot. Výchozí hodnota šablony je **10**.
- **Kód země/oblasti pro adresu** je v aplikaci Finance and Operations vyžadován. Aby nedocházelo k chybám synchronizace, můžete zadat výchozí hodnotu v mapování z **CDS &gt; Cíl**. Tato výchozí hodnota se pak použije, pokud pole v aplikaci Sales zůstane prázdné.

    - Výchozí hodnota šablony pro **AddressCountryRegionISOCode** je **USA**.
    - Výchozí hodnota šablony pro **DeliveryAddressCountryRegionISOCode** je **USA**.

- Přidáním následujících mapování z aplikace **CD &gt; Cíl** můžete snížit počet ručních aktualizací, které jsou potřebné v aplikaci Finance and Operations. Můžete použít výchozí hodnotu nebo mapu hodnot například z pole **Země/oblast** nebo **Město**.

    - **SiteId** – pracoviště je nutné za účelem generování nabídky a řádky prodejní objednávky v aplikaci Finance and Operations. Výchozí pracoviště lze získávat z produktu nebo od odběratele ze záhlaví objednávky. Výchozí hodnota šablony pro **SiteId** je **1**.
    - **WarehouseId** – sklad je nutný za účelem zpracování nabídek a řádky prodejní objednávky v aplikaci Finance and Operations. Výchozí sklad lze získat z produktu nebo od odběratele ze záhlaví objednávky aplikace Finance and Operations. Výchozí hodnota šablony pro **WarehouseId** je **13**.
    - **LanguageId** – jazyk je nutný za účelem generování nabídek a prodejních objednávek v aplikaci Finance and Operations. Ve výchozím nastavení se používá jazyk ze záhlaví objednávky od odběratele. Výchozí hodnota šablony pro **LanguageId** je **en-us**.

- Aktualizujte ID objednávky CDS (**Organization_OrganizationId**) v mapování **Zdroj &gt; CDS**. Výchozí hodnota šablony je **ORG001**.

## <a name="template-mapping-in-data-integrator"></a>Mapování šablony v integrátoru dat

> [!NOTE]
> Pole **Platební podmínky**, **Dopravní podmínky**, **Dodací podmínky**, **způsob dopravy** a **způsob dodání** nejsou zahrnuta do výchozího mapování. Pokud chcete tato pole mapovat, nastavte mapování hodnoty. Mapování hodnot jsou specifická pro data v organizacích, mezi nimiž probíhá synchronizace dané entity.

Na následujícím obrázku je příklad mapování šablony v integrátoru dat.

![Mapování šablony v integrátoru dat](./media/accounts-template-mapping-data-integrator-1.png)

![Mapování šablony pro účty v integrátoru dat](./media/accounts-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Související témata

[Synchronizace produktů z aplikace Finance and Operations na produkty v aplikaci Sales](products-template-mapping.md)

[Synchronizace kontaktů z aplikace Sales na kontakty nebo odběratele v aplikaci Finance and Operations](contacts-template-mapping.md)

[Synchronizace hlaviček a řádků prodejních nabídek z aplikace Sales do aplikace Finance and Operations](sales-quotation-template-mapping.md)

[Synchronizace hlaviček a řádků prodejní objednávky z aplikace Finance and Operations do Sales](sales-order-template-mapping.md)

[Synchronizace hlaviček a řádků prodejní faktury z aplikace Finance and Operations do Sales](sales-invoice-template-mapping.md)




