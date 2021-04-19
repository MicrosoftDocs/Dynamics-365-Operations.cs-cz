---
title: zpeněžení potenciálního zákazníka
description: Toto téma obsahuje přehled řešení zpeněžení potenciálního zákazníka mezi Dynamics 365 Supply Chain Management a Dynamics 365 Sales.
author: ChristianRytt
ms.date: 04/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 7b70b44a1d61d956f133cf0994647bd56adffa6b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836511"
---
# <a name="prospect-to-cash"></a>Zpeněžení potenciálního zákazníka

[!include [banner](../includes/banner.md)]

Řešení zpeněžení potenciálního zákazníka poskytuje přímou synchronizaci mezi aplikací Dynamics 365 Supply Chain Management a Dynamics 365 Sales. Šablony zpeněžení potenciálního zákazníka dostupné v rámci funkce integrace dat umožňují tok dat účtů, kontaktů, produktů, prodejních kvót, prodejních objednávek a prodejních faktur. V průběhu toku dat mezi aplikacemi Finance and Operations a Sales můžete provádět prodejní a marketingové aktivity v aplikaci Sales a můžete zpracovávat plnění objednávky pomocí správy skladů v aplikaci Supply Chain Management. 

Další informace o integraci zpeněžení potenciálního zákazníka uvádí krátké video na YouTube [Integrace zpeněžení potenciálního zákazníka](https://www.youtube.com/watch?v=AVV9x5x-XCg).

V aktuální verzi poskytuje řešení zpeněžení potenciálního zákazníka následující typy přímé synchronizace:

- [Synchronizace obchodních vztahů přímo z aplikace Sales na odběratele v Supply Chain Management.](accounts-template-mapping-direct.md)
- [Synchronizace produktů přímo z aplikace Supply Chain Management do produktů v Sales](products-template-mapping-direct.md)
- [Synchronizace kontaktů přímo z aplikace Sales na kontakty nebo odběratele v aplikaci Supply Chain Management](contacts-template-mapping-direct.md)
- [Synchronizace hlaviček a řádků prodejní nabídky přímo z aplikace Sales do Supply Chain Management](sales-quotation-template-mapping-sales-fin.md)
- [Synchronizace prodejních objednávek přímo mezi aplikacemi Sales a Supply Chain Management](sales-order-template-mapping-direct-two-ways.md)
- [Synchronizace hlaviček a řádků faktury přímo z aplikace Supply Chain Management do aplikace Sales](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-supply-chain-management"></a>Systémové požadavky pro Supply Chain Management
Integrace zpeněžení potenciálního zákazníka je podporována v následujících verzích:

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a>Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (prosinec 2017)

- Dynamics 365 for Finance and Operations, Enterprise edition (prosinec 2017) - sestavení aplikace 7.3.11971.56116 s aktualizací platformy 12 (7.0.4709.41129)

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>Dynamics 365 for Finance and Operations, Enterprise edition (červenec 2017)

- Dynamics 365 for Finance and Operations, Enterprise edition (červenec 2017) - s aktualizací platformy 8 (sestavení aplikace 7.2.11792.56024 se sestavením platformy 7.0.4565.16212).
- Následující opravy hotfix jsou vyžadovány:

  - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – Tato oprava hotfix umožňuje synchronizaci prodejní objednávky pomocí funkce integrace z aplikace Sales do aplikace Supply Chain Management. Poskytuje několik různých vylepšení.
  - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – Tato oprava hotfix umožňuje synchronizaci řádky prodejní objednávky pomocí funkce integrace z aplikace Supply Chain Management do Sales.
  - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – Tato oprava hotfix umožňuje synchronizaci prodejní objednávky pomocí funkce integrace z aplikace Supply Chain Management do Sales.

    > [!NOTE]
    > Musíte pouze nainstalovat KB4045570, protože instalace obsahuje změny z jiných oprav hotfix. 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a>Dynamics 365 for Finance and Operations verze 1611 (listopad 2016)

- Dynamics 365 for Finance and Operations verze 1611 (listopad 2016) s aktualizací platformy 8 nebo vyšší

- Následující opravy hotfix jsou vyžadovány:

  - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Povoluje synchronizaci prodejní objednávky s integrátorem dat z aplikace Supply Chain Management do Sales. 
  - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Povoluje synchronizaci záhlaví a řádky prodejní objednávky s integrátorem dat z aplikace Supply Chain Management do Sales.
  - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Podpora integrace zpeněžení potenciálního zákazníka prostřednictvím datových entit je požadována.
    
    > [!NOTE]
    > Po instalaci oprav hotfix je nutné spustit následující dávkovou úlohu z formuláře **SalesPopulateProspectToCash**. Tento formulář je skrytý, protože ho potřebujete pouze jednou. Abyste získali přístup k formuláři, přihlaste se do prostředí a přidejte do URL adresy ve svém prohlížeči toto: *&mi=action:SalesPopulateProspectToCash*, for example, `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`. Když se formulář otevře, klikněte na OK. Vypublikuje se nové pole **LineCreationSequnceNumber** v tabulkách **SalesLine**, **SalesQuotationLine** a **CustInvoiceTrans** s jedinečnými hodnotami a obnoví se seznam produktů. To je nutné pro fungování integrace zpeněžení potenciálního zákazníka.


## <a name="system-requirements-for-sales"></a>Systémové požadavky pro aplikaci Sales

Chcete-li použít řešení zpeněžení potenciálního zákazníka, je nutné nainstalovat následující komponenty:

- Dynamics 365 for Sales verze 1612 (8.2.1.207) (DB 8.2.1.207) online nebo vyšší verze.
- Řešení Prospect to Cash (P2C) pro Dynamics 365 Sales, verze 1.15.0.0 nebo novější. Řešení je k dispozici ke stažení z AppSource. [Stáhnout Dynamics 365, zpeněžení potenciálního zákazníka](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]