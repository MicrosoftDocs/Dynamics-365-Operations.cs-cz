---
title: Integrace s aplikací Microsoft Dynamics 365 for Field Service
description: Toto téma poskytuje přehled o integraci s Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 02/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: efda4e39f63155785386ecec6d21973e01a0f69f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564010"
---
# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a>Integrace s aplikací Microsoft Dynamics 365 for Field Service

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations umožňuje synchronizaci obchodních procesů mezi aplikacemi Finance and Operations a Microsoft Dynamics 365 for Field Service. Scénáře integrace jsou konfigurovány s použitím rozsáhlých šablon integrátoru dat a Common Data Service (CDS) pro umožnění synchronizace obchodních procesů.
Standardní šablony lze používat k vytváření projektů vlastní integrace, kde další standardní a vlastní pole a také entity, mohou být mapovány pro účely úpravy integrace a plnění konkrétních obchodních potřeb. 

Integrace Field Service staví na současné funkci potenciálního zákazníka k hotovosti.

![Synchronizace obchodních procesů mezi aplikacemi Finance and Operations a Field Service](./media/field-service-integration.png)

První fáze integrace mezi  Field Service a Finance and Operations se zaměřuje na povolení pracovních příkazů a smluv ve Field Service pro fakturaci ve Finance and Operations. Podporovaný tok začíná ve Field Service, kde jsou informace z pracovních příkazů synchronizovány s Finance and Operations jako prodejní objednávky. V modulu Finance and Operations jsou prodejní objednávky fakturovány ke generování faktur. Kromě toho jsou informace z faktur smluv ve službě Field Service synchronizovány do aplikace Finance and Operations. Integrátor dat Microsoft Dynamics 365 synchronizuje data pomocí upravitelné projektů. Standardní šablony lze používat k vytváření projektů vlastní integrace, kde další standardní a vlastní pole a také entity, mohou být mapovány pro účely úpravy integrace a plnění konkrétních požadavků.

První fáze integrace mezi Field Service a Finance and Operations umožňuje synchronizaci následujících položek:

- [Produkty v modulu Finance and Operations na produkty v modulu Field Service, které zahrnují informace o typu produktu](field-service-product.md)
- [Pracovní příkazy ve službě Field Service do prodejních objednávek v aplikaci Finance and Operations](field-service-work-order.md)
- [Faktury v aplikaci Field Service na volné textové faktury ve Finance and Operations](field-service-invoice.md)

Příklad synchronizace výrobního příkazu mezi Field Service a Finance and Operations uvádí krátké video na YouTube [Jak synchronizovat výrobní příkaz s integrací Microsoft Dynamics 365](https://www.youtube.com/watch?v=46ylO7raZAo).

## <a name="integration-with-microsoft-dynamics-365-for-field-service-including-inventory-and-project-information"></a>Integrace s aplikací Microsoft Dynamics 365 for Field Service, včetně informací a zásobách a projektu

Další funkce v této druhé fázi se zaměřovala na to, aby technikům v terénu poskytovala přehled o skladových informacích z modulu Finance and Operations, a umožnila jim tak aktualizovat úrovně zásob a provádět převod materiálů. Kromě toho společnosti zajišťující instalaci nebo servis prodaného zboží budou využívat lepší kontrolu a viditelnost plného prodejního a servisního procesu s integrací z projektů.

### <a name="functionality-includes-integration-of"></a>Funkce zahrnuje integraci následujících informací:
- Informace o skladovacím místě
- Informace o množství na skladě
- Převody zásob
- Úpravy zásob
- Projekty Dynamics 365 for Finance and Operations spojené s pracovními příkazy Dynamics 365 for Field Service
- Pracovní příkazy Dynamics 365 for Field Service s odkazem na projekty Dynamics 365 for Finance and Operations, použijte toto číslo projektu na prodejní objednávky Dynamics 365 for Finance and Operations, abyste povolili fakturaci z projektu. 

![Synchronizace obchodních procesů mezi aplikacemi Finance and Operations a Field Service](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-finance-and-operations-enables-synchronization-with-the-following-templates"></a>Druhá fáze integrace mezi Field Service a Finance and Operations umožňuje synchronizaci s následujícími šablonami:
- Sklady (Fin and Ops do Field Service) - Sklady z modulu Finance and Operations do Field Service [Pokročilý dotaz] 
- Zásoby produktu (Fin and Ops to Field Service) - Informace na úrovni zásob z aplikace Finance and Operations do Field Service [Pokročilý dotaz] 
- Úprava produktu (Field Service do Fin and Ops) - Úprava zásob z aplikace Field Service do Finance and Operations [Pokročilý dotaz] 
- Převody zásob (Field Service do Fin and Ops) - převody zásob z aplikace Field Service do Finance and Operations [Pokročilý dotaz] 
- Projekty (Fin and Ops do Field Service) - Seznam projektů z Finance and Operations do Field Service [Pokročilý dotaz] 
- pracovní příkazy s projektem (Field Service do Fin and Ops) - Pracovní příkazy v Field Service do příkazů k prodeji ve Finance and Operations, s podporou projektu [Pokročilý dotaz] 
- Produkty Field Service Products se skladovou jednotkou (Fin and Ops do Sales) - prodejné vydané produkty Finance and Operations pro Field Service, včetně skladové jednotky 

## <a name="system-requirements"></a>Systémové požadavky

### <a name="system-requirements-for-finance-and-operations"></a>Systémové požadavky aplikaci Finance and Operations
Integrace Field Service podporuje následující verze:

- Dynamics 365 for Finance and Operations verze 8.1.2 (Prosinec 2018) byla vydána v 2018 dne a má číslo sestavení aplikace 8.1.195 s aktualizací Platform Update 22 (7.0.5095). 

### <a name="system-requirements-for-field-service"></a>Požadavky na systém pro Field Service
Chcete-li použít řešení integrace Field Service, je nutné nainstalovat následující komponenty:

- Field Service for Dynamics 365 (verze 8.2.0.286) nebo novější na Dynamics 365 9.1.x - vydána v listopadu 2018
- Řešení Prospect to Cash (P2C) pro Dynamics 365, verze 1.15.0.1 nebo novější. Řešení je k dispozici ke stažení z [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- Řešení 'Field Service Integration, Project and Inventory' pro Dynamics 365, verze 2.0.0.0 nebo novější. Řešení je k dispozici ke stažení z [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).
