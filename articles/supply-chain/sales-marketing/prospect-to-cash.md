---
title: "zpeněžení potenciálního zákazníka"
description: "Toto téma uvádí přehled řešení zpeněžení potenciálního zákazníka mezi aplikacemi Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition a Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 02/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, SalesTable, EcoResProductListPage
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
ms.sourcegitcommit: 95d5bf26c22238753586cf4a7aaf5c26f061a705
ms.openlocfilehash: 62f328c5a6bf5343c97de0b7d907bbcfe2fcde4d
ms.contentlocale: cs-cz
ms.lasthandoff: 02/23/2018

---

# <a name="prospect-to-cash"></a>zpeněžení potenciálního zákazníka

[!include[banner](../includes/banner.md)]

Řešení zpeněžení potenciálního zákazníka nabízí přímou synchronizaci mezi aplikacemi Dynamics 365 for Finance and Operations, Enterprise Edition a Dynamics 365 for Sales. Šablony zpeněžení potenciálního zákazníka dostupné v rámci funkce integrace dat umožňují tok dat účtů, kontaktů, produktů, prodejních kvót, prodejních objednávek a prodejních faktur mezi aplikacemi Finance and Operations a Sales. V průběhu toku dat mezi aplikacemi Finance and Operations a Sales můžete provádět prodejní a marketingové aktivity v aplikaci Sales a můžete zpracovávat plnění objednávky pomocí správy skladů v aplikaci Finance and Operations. 

Další informace o zpeněžení potenciálního zákazníka naleznete v krátkém videu na YouTube:

> [!Video https://www.youtube.com/embed/AVV9x5x-XCg]

V aktuální verzi poskytuje řešení zpeněžení potenciálního zákazníka následující typy přímé synchronizace:

- [Správa účtů v aplikaci Sales a jejich synchronizace přímo z aplikace Sales do aplikace Finance and Operations](accounts-template-mapping-direct.md)
- [Správa produktů v aplikaci Finance and Operations a jejich synchronizace přímo do aplikace Sales](products-template-mapping-direct.md)
- [Správa kontaktů v aplikaci Sales a jejich přímá synchronizace na kontakty nebo odběratele v aplikaci Finance and Operations](contacts-template-mapping-direct.md)
- [Synchronizace prodejních nabídek přímo z aplikace Sales do aplikace Finance and Operations (šablona čekající na vydání)](sales-quotation-template-mapping-sales-fin.md)
- [Synchronizace prodejních objednávek přímo z aplikace Finance and Operations do aplikace Sales](sales-order-template-mapping-direct.md)
- [Synchronizace prodejních objednávek přímo mezi aplikací Finance and Operations a aplikací Sales (šablona čekající na vydání)](sales-order-template-mapping-direct-two-ways.md)
- [Synchronizace prodejních faktur přímo z aplikace Finance and Operations do aplikace Sales](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-finance-and-operations"></a>Systémové požadavky aplikaci Finance and Operations

Integrace zpeněžení potenciálního zákazníka je podporována v následujících verzích:

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a>Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (prosinec 2017)

- Dynamics 365 for Finance and Operations, Enterprise edition (prosinec 2017) - sestavení aplikace 7.3.11971.56116 s aktualizací Platform Update 12 (7.0.4709.41129)

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>Rozvržení v aplikaci Dynamics 365 for Finance and Operations, Enterprise edition (červenec 2017)

- Dynamics 365 for Finance and Operations, Enterprise Edition (července 2017) - s aktualizací Platform update 8 (sestavení aplikace 7.2.11792.56024 se sestavením platformou 7.0.4565.16212).
- Následující opravy hotfix jsou vyžadovány:

    - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – Tato oprava hotfix umožňuje synchronizaci prodejní objednávky pomocí funkce integrace z aplikace Sales do aplikace Finance and Operations. Poskytuje několik různých vylepšení.
    - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – Tato oprava hotfix umožňuje synchronizaci řádku prodejní objednávky pomocí funkce integrace z aplikace Finance and Operations do aplikace Sales.
    - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – Tato oprava hotfix umožňuje synchronizaci prodejní objednávky pomocí funkce integrace z aplikace Finance and Operations do aplikace Sales.

    > [!NOTE]
    > Musíte pouze nainstalovat KB4045570, protože instalace obsahuje změny z jiných oprav hotfix. 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a>Dynamics 365 for Finance and Operations, verze 1611 (listopad 2016)

- Dynamics 365 for Finance and Operations, verze 1611, s aktualizací platformy 8 nebo vyšší (listopad 2016)

- Následující opravy hotfix jsou vyžadovány:

    - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Povoluje synchronizaci prodejní objednávky s integrátorem dat z aplikace Finance and Operations do Sales 
    - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Povoluje synchronizaci řádku a záhlaví prodejní objednávky s integrátorem dat z aplikace Finance and Operations do Sales
    - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Podpora integrace zpeněžení potenciálního zákazníka prostřednictvím datových entit je požadována.
    
    > [!NOTE]
    > Po instalaci oprav hotfix je nutné spustit následující dávkovou úlohu z formuláře **SalesPopulateProspectToCash**. Tento formulář je skrytý, protože ho potřebujete pouze jednou. Abyste získali přístup k formuláři, přihlaste se do prostředí a přidejte do URL adresy ve svém prohlížeči toto: &mi=action:SalesPopulateProspectToCash, například `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`. Když se formulář otevře, klikněte na OK. Vypublikuje se nové pole **LineCreationSequnceNumber** v tabulkách **SalesLine**, **SalesQuotationLine** a **CustInvoiceTrans** s jedinečnými hodnotami a obnoví se seznam produktů. To je nutné pro fungování integrace zpeněžení potenciálního zákazníka.


## <a name="system-requirements-for-sales"></a>Systémové požadavky pro aplikaci Sales

Chcete-li použít řešení zpeněžení potenciálního zákazníka, je nutné nainstalovat následující komponenty:

- Dynamics 365 for Sales verze 1612 (8.2.1.207) (DB 8.2.1.207) online
- Řešení zpeněžení potenciálního zákazníka pro Dynamics 365 for Sales, verze 1.15.0.0 (v15) 

### <a name="install-the-prospect-to-cash-solution-for-sales"></a>Instalace řešení zpeněžení potenciálního zákazníka pro aplikaci Sales

1. Stáhněte [Zip soubor s balíčkem řešení zpeněžení potenciálního zákazníka pro Dynamics 365 for Sales](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) z webu CustomerSource.
2. Ověřte, že soubor zip není blokován. V opačném případě se při pokusu o instalací balíčku řešení může zobrazit následující chybová zpráva: Nebyly nalezeny žádné balíčky pro import. Chcete-li odblokovat zip soubor, klikněte pravým tlačítkem a vyberte **Vlastnosti**. Vyberte **Odblokovat**.
3. Rozbalte a spusťte soubor **PackageDeployer.exe**.
4. Nainstalujte řešení zpeněžení potenciálního zákazníka na své instanci aplikace Sales:

    1. Vyberte **Office 365** jako typ nasazení.
    2. Vyberte **Zobrazit podrobné**.
    3. Pro rychlou instalaci zvolte oblast. Vyberete-li **Nevím**, systém vyhledá všechny oblasti a instalace bude trvat déle.
    4. Zadejte uživatelské jméno a heslo uživatele s rolí správce, který má k instalaci práva.



