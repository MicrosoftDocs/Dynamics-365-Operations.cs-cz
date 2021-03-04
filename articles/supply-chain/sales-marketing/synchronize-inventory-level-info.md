---
title: Synchronizace informací o úrovni zásob z aplikace Supply Chain Management do služby Field Service
description: Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci informací na úrovni zásob z Dynamics 365 Supply Chain Management do Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 05/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 1228339c12d26f7b91875d15f0daa8da2869cba0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423696"
---
# <a name="synchronize-inventory-level-information-from-supply-chain-management-to-field-service"></a>Synchronizace informací o úrovni zásob z aplikace Supply Chain Management do služby Field Service 

[!include[banner](../includes/banner.md)]

Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci informací na úrovni zásob z Dynamics 365 Supply Chain Management do Dynamics 365 Field Service.

[![Synchronizace obchodních procesů mezi Supply Chain Management a Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Šablony a úkoly
Následující šablona a základní úlohy se používají k synchronizaci praktických úrovní skladů ze Supply Chain Management do Field Service.

**Šablona v integraci dat**
- Zásoby produktu (z aplikace Supply Chain Management do služby Field Service)
  
**Úkol v projektu integrace dat**
- Zásoby produktu

Následující úlohy synchronizace jsou vyžadovány před zobrazením synchronizace množství zásob:
- Sklady (z aplikace Supply Chain Management do služby Field Service) 
- Produkty Field Service se skladovou jednotkou (Supply Chain Management do Sales) 

## <a name="entity-set"></a>Sada entit

| Field Service                      | Správa dodavatelsko-odběratelského řetězce                |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | CDS zásoby na skladě podle skladu     |

## <a name="entity-flow"></a>Tok entity
Informace o množství zásob z aplikace Finance and Operations jsou pro vybrané produkty odeslány do služby Field Service. Informace na úrovni zásob zahrnují: 
- Množství na skladě (aktuální evidované fyzické množství, které se nachází ve skladu)
- Množství objednávky (celkové zaznamenané množství na objednávce, jako jsou prodejní objednávky)
- Objednané množství (celkové zaznamenané objednané množství, jako jsou prodejní objednávky)

Tyto informace jsou zaznamenány pro uvolněný produkt pro každý sklad a synchronizovány podle sledování změn, když se změní úroveň zásob.

Ve službě Field Service, řešení integrace vytváří deníky zásob pro deltu, takže úrovně ve službě Field Service odpovídají množstvím v aplikaci Supply Chain Management.

Aplikace Supply Chain Management bude sloužit jako hlavní zdroj pro úroveň zásob. Proto je důležité nastavit integraci pro pracovní příkazy, převody a opravy ze služby Field Service do aplikace Supply Chain Management, pokud se tato funkce používá ve službě Field Service, dohromady se synchronizací množství zásob z aplikace Supply Chain Management.

Produkty a sklady, kde jsou zásoby řízení z aplikace Supply Chain Management lze ovládat pomocí Rozšířeného dotazu a filtrování (Power Query).

> [!NOTE]
> Poznámka: Je možné vytvořit více skladů ve službě Field Services (pomocí **Je externě spravován = Ne**) a poté je namapovat do jediného skladu v aplikaci Supply Chain Management pomocí funkce filtrování a pokročilých dotazů. Používá se v situacích, kdy si přejete, aby služba Field Service spravovala podrobné informace o zásobách a jen odesílala aktuální informace do aplikace Supply Chain Management. V tomto případě neobdrží služba Field Service aktualizace úrovně zásob z aplikace Supply Chain Management. Další informace získáte v části [Synchronizace skladových úprav z aplikace Field Service do Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronizace pracovních příkazů z Field Service na prodejní objednávky navázané na projekt v Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="field-service-crm-solution"></a>Řešení Field Service CRM
Entita **zásoby externího produktu** je nová entita, která se používá pouze pro jištění při integraci. Tato entita přijme integrované hodnoty úrovně zásob z aplikace Supply Chain Management a potom tyto hodnoty transformuje do deníků ručních zásob, které poté změní produkty zásob skladu.

## <a name="prerequisites-and-mapping-setup"></a>Nastavení mapování a předpokladů

### <a name="data-integration"></a>Integrace dat
Aby projekt fungoval, je nutné zajistit, aby byl klíč integrace aktualizován pro msdynce_externalproductinventories.
1.  Přejděte na **Integrace dat > Sady připojení**.
2.  Vyberte použitou sadu připojení.
3.  Na kartě **Klíč integrace** se ujistěte, že jsou do msdynce_externalproductinventories přidány následující klíče:
      - msdynce_productnumber (číslo produktu)
      - msdynce_warehouseid (ID skladu)
      
### <a name="data-integration-project"></a>Projekt integrace dat
Můžete použít filtry s pokročilým dotazováním a filtrování, pomocí kterých lze řídit, že informace o zásobách budou z aplikace Supply Chain Management do služby Field Service odesílat pouze požadované produkty a sklady.

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

### <a name="product-inventory-supply-chain-management-to-field-service-product-inventory"></a>Zásoby produktu (Supply Chain Management do Field Service): Zásoby produktu

[![Mapování šablony v integraci dat](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]