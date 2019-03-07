---
title: Synchronizujte informace o množství zásob z aplikace Finance and Operations do služby Field Service
description: Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci informací na úrovni zásob z Microsoft Dynamics 365 for Finance and Operations do Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 01/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: b81694f1ed56d8542de46203ac5faf5fae2b6645
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "356776"
---
# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a>Synchronizace informací o úrovni zásob z aplikace Finance and Operations do služby Field Service 

[!include[banner](../includes/banner.md)]

Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci informací na úrovni zásob z Microsoft Dynamics 365 for Finance and Operations do Microsoft Dynamics 365 for Field Service.

[![Synchronizace obchodních procesů mezi aplikacemi Finance a Operations and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Šablony a úkoly
Následující šablony a základní úkoly se používají k synchronizaci úprav zásob na skladě a převodů z Microsoft Dynamics 365 for Finance and Operations do Microsoft Dynamics 365 for Field Service.

**Šablona v integraci dat**
- Zásob produktu (z aplikace Finance and Operations do služby Field Service)
  
**Úkol v projektu integrace dat**
- Zásoby produktu

Následující úlohy synchronizace jsou vyžadovány před zobrazením synchronizace množství zásob:
- Sklady (z aplikace Finance and Operations do služby Field Service) 
- Produkty služby Field Service s jednotkou zásob (z aplikace Finance and Operations do služby Prodej) 

## <a name="entity-set"></a>Sada entit

| Field Service                      | Finance and Operations                 |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | CDS zásoby na skladě podle skladu     |

## <a name="entity-flow"></a>Tok entity
Informace o množství zásob z aplikace Finance and Operations jsou pro vybrané produkty odeslány do služby Field Service. Informace na úrovni zásob zahrnují: 
- Množství na skladě (aktuální evidované fyzické množství, které se nachází ve skladu)
- Množství objednávky (celkové zaznamenané množství na objednávce, jako jsou prodejní objednávky)
- Objednané množství (celkové zaznamenané objednané množství, jako jsou prodejní objednávky)

Tyto informace jsou zaznamenány pro uvolněný produkt pro každý sklad a synchronizovány podle sledování změn, když se změní úroveň zásob.

Ve službě Field Service, řešení integrace vytváří deníky zásob pro deltu, takže úrovně ve službě Field Service odpovídají množstvím v aplikaci Finance and Operations.

Aplikace Finance and Operations bude sloužit jako hlavní zdro pro úroveň zásob. Proto je důležité nastavit integraci pro pracovní příkazy, převody a opravy ze služby Field Service do aplikace Finance and Operations, pokud se tato funkce používá ve službě Field Service, dohromady se synchronizací množství zásob z aplikace Finance and Operations.

Produkty a sklady, kde jsou zásoby řízení z aplikace Finance and Operations lze ovládat pomocí Rozšířeného dotazu a filtrování (Power Query).

> [!NOTE]
> Poznámka: Je možné vytvořit více skladů ve službě Field Services (pomocí **Je externě spravován = Ne**) a poté je namapovat do jediného skladu v aplikaci Finance and Operations pomocí funkce filtrování a pokročilých dotazů. Používá se v situacích, kdy si přejete, aby služba Field Service spravovala podrobné informace o zásobách a jen odesílala aktuální informace do aplikace Finance and Operations. V tomto případě neobdrží služba Field Service aktualizace úrovně zásob z aplikace Finance and Operations. Další informace získáte v části [Synchronizace skladových úprav z aplikace Field Service do Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronizace pracovních příkazů z Field Service na prodejní objednávky navázané na projekt ve Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="field-service-crm-solution"></a>Řešení Field Service CRM
Entita **zásoby externího produktu** je nová entita, která se používá pouze pro jištění při integraci. Tato entita přijme integrované hodnoty úrovně zásob z aplikace Finance and Operations a potom tyto hodnoty transformuje do deníků ručních zásob, které poté změní produkty zásob skladu.

## <a name="prerequisites-and-mapping-setup"></a>Nastavení mapování a předpokladů

### <a name="data-integration-project"></a>Projekt integrace dat
Můžete použít filtry s pokročilým dotazováním a filtrování, pomocí kterých lze řídit, že informace o zásobách budou z aplikace Finance and Operations do služby Field Service odesílat pouze požadované produkty a sklady.

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a>Zásoby produktu (z aplikace Finance and Operations do služby Field Service): zásoby produktu

[![Mapování šablony v integraci dat](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)
