---
title: "Synchronizujte informace o množství zásob z aplikace Finance and Operations do služby Field Service"
description: "Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci informací i mnoství zásob z aplikace Microsoft Dynamics 365 for Finance and Operations do aplikace Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: 3ccc4d406fa4f9800dcdf8697a91892408783196
ms.contentlocale: cs-cz
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a>Synchronizujte informace o množství zásob z aplikace Finance and Operations do služby Field Service 

[!include[banner](../includes/banner.md)]

Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci informací i mnoství zásob z aplikace Microsoft Dynamics 365 for Finance and Operations do aplikace Microsoft Dynamics 365 for Field Service.

[![Synchronizace obchodních procesů mezi aplikacemi Finance a Operations and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Šablony a úkoly
Následující šablona a základní úlohy, které se používají k synchronizaci dostupného množství zásob z aplikace Microsoft Dynamics 365 for Finance and Operations do aplikace Microsoft Dynamics 365 or Field Service.

**Název šablony v integraci dat:**
- Zásob produktu (z aplikace Finance and Operations do služby Field Service)
  
**Názvy úkolů v projektu integrace dat:**
- Zásoby produktu

Následující úlohy synchronizace jsou vyžadovány před zobrazením synchronizace množství zásob:
- Sklady (z aplikace Finance and Operations do služby Field Service) 
- Produkty služby Field Service s jednotkou zásob (z aplikace Finance and Operations do služby Prodej) 

## <a name="entity-set"></a>Sada entit

| Field Service                      | Finance and Operations                 |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | CDS zásoby na skladě podle skladu     |

## <a name="entity-flow"></a>Tok entity
Informace o množství zásob z aplikace Finance and Operations jsou pro vybrané produkty odeslány do služby Field Service. Skladové úrovně informace zahrnují: 
- Množství na skladě (aktuální evidované fyzické množství, které se nachází ve skladu)
- Množství objednávky (celkové zaznamenané množství na objednávce - tj. prodejní objednávky)
- Objednané množství (celkové zaznamenané objednané množství - tj. prodejní objednávky)

Tyto informace jsou zaznamenány pro uvolněný produkt pro každý sklad a synchronizovány podle sledování změn, když se změní úroveň zásob.

Ve službě Field Service, řešení integrace tvorby deníků zásob pro deltu, pro získání množství ve službě Field Service, aby odpovídaly množstvím v aplikaci Finance and Operations.

Aplikace Finance and Operations bude sloužit jako hlavní zdro pro úroveň zásob. Proto je důležité nastavit integrace pro zakázky, převody a opravy ze služby Field Service do aplikace Finance and Operations, pokud se tato funkce používá ve službě Field Service, dohromady se synchronizací množství zásob z aplikace Finance and Operations.

Produkty a sklady, kde jsou zásoby řízení z aplikace Finance and Operations lze ovládat pomocí Rozšířeného dotazu a filtrování (Power Query).

Poznámka: Je možné vytvořit více skladů ve službě Field Service (pomocí Je externě spravován = Ne) a poté je namapovat do jediného skladu v aplikaci Finance and Operations pomocí funkce filtrování a pokročilých dotazů. Používá se v situacích, kdy si přejete, aby služba Field Service spravovala podrobné informace o zásobách a jen odesílala aktuální informace do aplikace Finance and Operations. V tomto případě neobdrží služba Field Service aktualizace úrovně zásob z aplikace Finance and Operations. Zobrazit další informace v Synchronizovat úpravy zásob ze služby Field Service do aplikace Finance and Operations a v Synchronizovat pracovní příkazy ve službě Field Service do prodejních objednávce propojených s projektem v aplikaci Finance and Operations.

## <a name="field-service-crm-solution"></a>Řešení Field Service CRM
Entita zásoby externího produktu je nová entita, která se používá pouze v integraci. Přijme integrované hodnoty úrovně zásob z aplikace Finance and Operations a potom tyto hodnoty transformuje do deníků ručních zásob, které poté změní produkty zásob skladu. 

## <a name="prerequisites-and-mapping-setup"></a>Nastavení mapování a předpokladů

### <a name="in-the-data-integration-project"></a>V projektu Integrace dat
Použijte filtry s pokročilým dotazováním a filtrování, pomocí kterých lze řídit, že informace o zásobách budou z aplikace Finance and Operations do služby Field Service odesílat pouze požadované produkty a sklady.

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a>Zásoby produktu (z aplikace Finance and Operations do služby Field Service): zásoby produktu

[![Mapování šablony v integraci dat](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)

