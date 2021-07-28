---
title: Přehled integrace se službou Microsoft Dynamics 365 Field Service
description: Toto téma poskytuje přehled o integraci s Microsoft Dynamics 365 Field Service.
author: ChristianRytt
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 2ceb95198332d6a9da057d657771fe6fcca5c5b9
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359598"
---
# <a name="integration-with-microsoft-dynamics-365-field-service-overview"></a>Přehled integrace se službou Microsoft Dynamics 365 Field Service

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Supply Chain Management umožňuje synchronizaci obchodních procesů mezi aplikacemi Dynamics 365 Supply Chain Management a Dynamics 365 Field Service. Scénáře integrace jsou konfigurovány s použitím rozsáhlých šablon integrátoru dat a Microsoft Dataverse pro umožnění synchronizace obchodních procesů.
Standardní šablony lze používat k vytváření projektů vlastní integrace, kde další standardní a vlastní sloupce a tabulky, mohou být mapovány pro účely úpravy integrace a plnění konkrétních obchodních potřeb. 

Integrace Field Service staví na současné funkci potenciálního zákazníka k hotovosti.

![Synchronizace obchodních procesů mezi Supply Chain Management a Field Service.](./media/field-service-integration.png)

První fáze integrace mezi Field Service a Supply Chain Management se zaměřuje na povolení pracovních příkazů a smluv ve Field Service pro fakturaci v Supply Chain Management. Podporovaný tok začíná ve Field Service, kde jsou informace z pracovních příkazů synchronizovány s Supply Chain Management jako prodejní objednávky. V Supply Chain Management jsou prodejní objednávky fakturovány za účelem generování fakturačních dokumentů. Kromě toho jsou informace z faktur smluv ve službě Field Service synchronizovány do aplikace Supply Chain Management. Integrátor dat Microsoft Dynamics 365 synchronizuje data pomocí upravitelné projektů. Standardní šablony lze používat k vytváření projektů vlastní integrace, kde další standardní a vlastní sloupce a také tabulky, mohou být mapovány pro účely úpravy integrace a plnění konkrétních požadavků.

První fáze integrace mezi Field Service a Finance and Supply Chain Management umožňuje synchronizaci následujících položek:

- [Synchronizace produktů v Supply Chain Management do produktů ve Field Service](field-service-product.md)
- [Synchronizace pracovních příkazů ve službě Field Service do prodejních objednávek v aplikaci Supply Chain Management](field-service-work-order.md)
- [Synchronizace smluvních faktur v Field Service na volné textové faktury v Supply Chain Management](field-service-invoice.md)

Příklad synchronizace výrobního příkazu mezi Field Service a Supply Chain Management uvádí krátké video na YouTube [Jak synchronizovat výrobní příkaz s integrací Microsoft Dynamics 365](https://www.youtube.com/watch?v=46ylO7raZAo).

## <a name="integration-with-field-service-including-inventory-and-project-information"></a>Integrace s aplikací Field Service, včetně informací a zásobách a projektu

Další funkce v této druhé fázi se zaměřovala na to, aby technikům v terénu poskytovala přehled o skladových informacích z modulu Supply Chain Management, a umožnila jim tak aktualizovat úrovně zásob a provádět převod materiálů. Kromě toho společnosti zajišťující instalaci nebo servis prodaného zboží budou využívat lepší kontrolu a viditelnost plného prodejního a servisního procesu s integrací z projektů.

### <a name="functionality-includes-integration-of"></a>Funkce zahrnuje integraci následujících informací:
- Informace o skladovacím místě
- Informace o množství na skladě
- Převody zásob
- Úpravy zásob
- Projekty Supply Chain Management spojené s pracovními objednávkami Dynamics 365 Field Service
- Pracovní příkazy Dynamics 365 Field Service s odkazem na projekty Supply Chain Management, použijte toto číslo projektu na prodejní objednávky, abyste povolili fakturaci z projektu. 

![Synchronizace obchodních procesů mezi Supply Chain Management a Field Service.](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-supply-chain-management-enables-synchronization-with-the-following-templates"></a>Druhá fáze integrace mezi Field Service a Supply Chain Management umožňuje synchronizaci s následujícími šablonami:
- Sklady (Supply Chain Management do Field Service) - sklady ze Supply Chain Management do Field Service [rozšířený dotaz] 
- Zásoby produktu (Supply Chain Management do Field Service) - informace o úrovni zásob ze Supply Chain Management do Field Service [rozšířený dotaz] 
- Úprava zásob (Field Service do Supply Chain Management) - Úprava zásob z Field Service do Supply Chain Management [rozšířený dotaz] 
- Převody zásob (Field Service do Supply Chain Management) - Převody zásob z Field Service do Supply Chain Management [rozšířený dotaz] 
- Projekty (Supply Chain Management do Field Service) - seznam projektů ze Supply Chain Management do Field Service 
- pracovní příkazy s projektem (Field Service do Supply Chain Management) - Pracovní příkazy v Field Service do příkazů k prodeji v Supply Chain Management, s podporou projektu [Pokročilý dotaz] 
- Produkty Field Service Products se skladovou jednotkou (Supply Chain Management do Sales) - prodejné vydané produkty Supply Chain Management pro Field Service, včetně skladové jednotky 

## <a name="system-requirements"></a>Systémové požadavky

### <a name="system-requirements-for-supply-chain-management"></a>Systémové požadavky pro Supply Chain Management
Integrace Field Service podporuje následující verze:

- Dynamics 365 for Finance and Operations verze 8.1.2 (Prosinec 2018) byla vydána v 2018 dne a má číslo sestavení aplikace 8.1.195 s aktualizací Platform update 22 (7.0.5095). 

### <a name="system-requirements-for-field-service"></a>Požadavky na systém pro Field Service
Chcete-li použít řešení integrace Field Service, je nutné nainstalovat následující komponenty:

- Field Service (verze 8.2.0.286) nebo novější na Dynamics 365 9.1.x - vydána v listopadu 2018
- Řešení Prospect to Cash (P2C) pro Dynamics 365, verze 1.15.0.1 nebo novější. Řešení je k dispozici ke stažení z [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- Řešení 'Field Service Integration, Project and Inventory' pro Dynamics 365, verze 2.0.0.0 nebo novější. Řešení je k dispozici ke stažení z [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]