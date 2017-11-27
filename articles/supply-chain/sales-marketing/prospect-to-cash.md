---
title: "zpeněžení potenciálního zákazníka"
description: "Toto téma uvádí přehled řešení zpeněžení potenciálního zákazníka mezi aplikacemi Dynamics 365 for Finance and Operations, Enterprise Edition a Dynamics 365 for Sales."
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 674d2e1f2c5cdbccf43618a9083ca01abed0735a
ms.openlocfilehash: 2accf77c5241adff7ad1648737dde451153fde46
ms.contentlocale: cs-cz
ms.lasthandoff: 11/14/2017

---

# <a name="prospect-to-cash"></a>zpeněžení potenciálního zákazníka  

[!include[banner](../includes/banner.md)]

Řešení zpeněžení potenciálního zákazníka používá [Integraci dat](/common-data-service/entity-reference/dynamics-365-integration) k synchronizaci dat mezi instancemi aplikací Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition a Dynamics 365 for Sales prostřednictvím služby Common Data Service (CDS). Šablony zpeněžení potenciálního zákazníka dostupné v rámci funkce integrace dat umožňují tok účtů, kontaktů, produktů, prodejních kvót, prodejních objednávek a prodejních faktur mezi aplikacemi Finance and Operations a Sales. V průběhu toku dat mezi aplikacemi Finance and Operations a Sales můžete provádět prodejní a marketingové aktivity v aplikaci Sales a zpracovávat plnění objednávky v rámci správy skladů v aplikaci Finance and Operations. 

Toto řešení umožňuje integraci v rámci následujících oblastí: 

-   [Správa účtů v aplikaci Sales a jejich synchronizace do aplikaci Finance and Operations](accounts-template-mapping.md)
-   [Správa kontaktů v aplikaci Sales a jejich synchronizace do aplikaci Finance and Operations](contacts-template-mapping.md)
-   [Správa produktů v aplikaci Finance and Operations a jejich synchronizace do aplikace Sales](products-template-mapping.md)
-   [Vytvoření prodejních nabídek v aplikaci Sales a jejich synchronizace do aplikace Finance and Operations.](sales-quotation-template-mapping.md)
-   [Vytvoření prodejních objednávek v aplikaci Finance and Operations a jejich synchronizace do aplikace Sales](sales-order-template-mapping.md)
-   [Vytvoření prodejních faktur v aplikaci Finance and Operations a jejich synchronizace do aplikace Sales](sales-invoice-template-mapping.md)

Toto řešení umožňuje přímou synchronizaci v rámci následujících oblastí:

-   [Správa účtů v aplikaci Sales a jejich synchronizace přímo z aplikace Sales do aplikace Finance and Operations](accounts-template-mapping-direct.md)
-   [Správa produktů v aplikaci Finance and Operations a jejich synchronizace přímo do aplikace Sales](products-template-mapping-direct.md)
-   [Správa kontaktů v aplikaci Sales a jejich přímá synchronizace na kontakty nebo odběratele v aplikaci Finance and Operations](contacts-template-mapping-direct.md)
-   [Synchronizace hlaviček a řádků prodejních nabídek přímo z aplikace Sales do aplikace Finance and Operations](sales-quotation-template-mapping-sales-fin.md)
-   [Vytvoření prodejních objednávek v aplikaci Finance and Operations a jejich synchronizace přímo do aplikace Sales](sales-order-template-mapping-direct.md)
-  [Synchronizace hlaviček a řádků prodejní objednávky přímo mezi aplikacemi Sales a Finance and Operations](sales-order-template-mapping-between-sales-fin.md)
-   [Synchronizace prodejních objednávek přímo mezi aplikacemi Sales a Finance and Operations](sales-order-template-mapping-direct-two-ways.md)
-   [Vytvoření prodejních faktur v aplikaci Finance and Operations a jejich synchronizace přímo do aplikace Sales](sales-invoice-template-mapping-direct.md)


## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a>Systémové požadavky pro aplikaci Dynamics 365 for Finance and Operations, Enterprise Edition

Chcete-li použít řešení zpeněžení potenciálního zákazníka, je nutné nainstalovat následující:

- Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (července 2017) s aktualizací Platform update 8 (aplikací 7.2.11792.56024 s platformou 7.0.4565.16212)

- Opravy hotfix Dynamics 365 for Finance and Operations, Enterprise Edition (červenec 2017).
        
    -  [KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160) – Tato oprava hotfix umožňuje podporu pro synchronizaci prodejní objednávky s funkcí integrace dat z aplikace Sales do aplikace Finance and Operations, spolu s řadou dalších vylepšení.

    -  [KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - Tato oprava hotfix umožňuje synchronizaci řádku prodejní objednávky pomocí funkce integrace z aplikace Finance and Operations do Sales.
        
    -  [KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - Tato oprava hotfix umožňuje synchronizaci prodejní objednávky pomocí funkce integrace z aplikace Finance and Operations do Sales.

**Poznámka**: Musíte pouze nainstalovat KB4045570, protože instalace obsahuje změny z jiných článků znalostní báze.
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a>Systémové požadavky pro Dynamics 365 for Sales

Chcete-li použít řešení zpeněžení potenciálního zákazníka, je nutné nainstalovat následující:

- Dynamics 365 for Sales verze 1612 (8.2.1.207) (DB 8.2.1.207) online.
- Řešení zpeněžení potenciálního zákazníka pro Dynamics 365 for Sales, verze 1.14.0.0 (v14) nebo pozdější.

### <a name="install-the-prospect-to-cash-solution-for-sales"></a>Instalace řešení zpeněžení potenciálního zákazníka pro aplikaci Sales

- Stáhněte [Zip soubor s balíčkem řešení zpeněžení potenciálního zákazníka pro Dynamics 365 for Sales](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) z webu CustomerSource.

- Ujistěte se, že ZIP soubor není blokován, aby se vám při instalaci balíčku řešení nezobrazila chybová zpráva „Nebyl nalezen žádný balíček pro import“. Abyste odblokovali soubor, proveďte následující:

    -  Klikněte pravým tlačítkem soubor ZIP.
    -  Vyberte **Vlastnosti** a poté vyberte **Odblokovat**. 

- Rozbalte a spusťte soubor PackageDeployer.exe.

- Nainstalujte řešení zpeněžení potenciálního zákazníka do své instance aplikace Sales.

    - Vyberte typ nasazení **Office 365**.
    - Vyberte **Zobrazit podrobné**.
    - Pro rychlou instalaci zvolte **Oblast**. Vyberete-li **Nevím**, systém vyhledá všechny oblasti a instalace bude trvat déle.
    - Zadejte **Uživatelské jméno** a **Heslo** uživatele s rolí správce, který má k instalaci uživatelská práva.

