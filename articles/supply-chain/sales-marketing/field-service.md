---
title: "Integrace s aplikací Microsoft Dynamics 365 for Field Service"
description: "Toto téma obsahuje přehled integrace s aplikací Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 08/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 95031534c43dc0578e258bc3e5376c429d72b0ab
ms.openlocfilehash: 673ab2a101cee1a3dbbb1249f582d959cecc7f7f
ms.contentlocale: cs-cz
ms.lasthandoff: 12/23/2018

---

# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a>Integrace s aplikací Microsoft Dynamics 365 for Field Service

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations umožňuje synchronizaci obchodních procesů mezi aplikací Finance and Operations a Microsoft Dynamics 365 for Field Service. Scénáře integrace jsou konfigurovány s použitím rozsáhlých šablon integrátoru dat a Common Data Service (CDS) pro umožnění synchronizace obchodních procesů.
Standardní šablony lze používat k vytváření projektů vlastní integrace, kde další standardní a vlastní pole a také entity, mohou být mapovány pro účely úpravy integrace a plnění konkrétních obchodních potřeb. 

Integrace Field Service staví na současné funkci potenciálního zákazníka k hotovosti.

![Synchronizace obchodních procesů mezi aplikacemi Finance and Operations a Field Service](./media/field-service-integration.png)

První fáze integrace mezi  Field Service a Finance and Operations se zaměřuje na povolení pracovních příkazů a smluv ve Field Service pro fakturaci ve Finance and Operations. Podporovaný tok začíná ve Field Service, kde jsou informace z pracovních příkazů synchronizovány s Finance and Operations jako prodejní objednávky. V modulu Finance and Operations jsou prodejní objednávky fakturovány ke generování faktur. Kromě toho jsou informace z faktur smluv ve službě Field Service synchronizovány do aplikace Finance and Operations. Integrátor dat Microsoft Dynamics 365 synchronizuje data pomocí upravitelné projektů. Standardní šablony lze používat k vytváření projektů vlastní integrace, kde další standardní a vlastní pole a také entity, mohou být mapovány pro účely úpravy integrace a plnění konkrétních požadavků.

První fáze integrace mezi Field Service a Finance and Operations umožňuje synchronizaci následujících položek:

- [Produkty v modulu Finance and Operations na produkty v modulu Field Service, které zahrnují informace o typu produktu](field-service-product.md)
- [Pracovní příkazy ve službě Field Service do prodejních objednávek v aplikaci Finance and Operations](field-service-work-order.md)
- [Faktury v aplikaci Field Service na volné textové faktury ve Finance and Operations](field-service-invoice.md)

Příklad synchronizace výrobního příkazu mezi Field Service a Finance and Operations uvádí krátké video na YouTube [Jak synchronizovat výrobní příkaz s integrací Microsoft Dynamics 365](https://www.youtube.com/watch?v=46ylO7raZAo).

## <a name="system-requirements-for-finance-and-operations"></a>Systémové požadavky aplikaci Finance and Operations
Integrace Field Service podporuje následující verze:

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a>Dynamics 365 for Finance and Operations, verze 8.0 (duben 2018) nebo pozdější

- Aplikace Dynamics 365 for Finance and Operations verze 8.0 (duben 2018) byla vydána v dubnu 2018 a má číslo sestavení aplikace 8.0.30.8020 s aktualizací platformy 15 (7.0.4841.35234). 

## <a name="system-requirements-for-field-service"></a>Požadavky na systém pro Field Service
Chcete-li použít řešení integrace Field Service, je nutné nainstalovat následující komponenty:

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a>Microsoft Dynamics 365 for Field Service 9.0 or later

- Dynamics 365 for Field Service verze 1612 (9.0.1.733) (DB 9.0.1.733) online nebo vyšší verze.
- Řešení Prospect to Cash (P2C) pro Dynamics 365, verze 1.15.0.1 nebo novější. Řešení je k dispozici ke stažení na webech [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- Řešení integrace Field Service pro Dynamics 365, verze 1.0.0.0 nebo novější. Řešení je k dispozici ke stažení na webech [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegration).

# <a name="integration-with-microsoft-dynamics-365-for-field-service-including-inventory-and-project-information"></a>Integrace s aplikací Microsoft Dynamics 365 for Field Service, včetně informací o zásobách a projektu

Další funkce v této druhé fázi se zaměřovala na to, aby technikům v terénu poskytovala přehled o skladových informacích z modulu Finance and Operations, a umožnila jim tak aktualizovat úrovně zásob a provádět převod materiálů. Kromě toho společnosti zajišťující instalaci nebo servis prodaného zboží budou využívat lepší kontrolu a viditelnost plného prodejního a servisního procesu s integrací z projektů.

### <a name="functionality-includes-integration-of"></a>Funkce zahrnuje integraci následujících informací:
- Informace o skladovacím místě
- Informace o množství na skladě
- Převody zásob
- Úpravy zásob
- Projekty aplikace Dynamics 365 for Finance and Operations spojené s pracovními příkazy aplikace Dynamics 365 for Field Service
- Pracovní příkazy aplikace Dynamics 365 for Field Service s odkazem na projekty aplikace Dynamics 365 for Finance and Operations, toto číslo projektu použijte pro prodejní objednávku aplikace Dynamics 365 for Finance and Operation, aby bylo povoleno fakturování z projektu. 

![Synchronizace obchodních procesů mezi aplikacemi Finance and Operations a Field Service](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-finance-and-operations-enables-synchronization-with-the-following-templates"></a>Druhá fáze integrace mezi Field Service a Finance and Operations umožňuje synchronizaci s následujícími šablonami:
- Sklady (Fin and Ops do Field Service) - Sklady z modulu Finance and Operations do Field Service [Pokročilý dotaz] 
- Zásoby produktu (Fin and Ops to Field Service) - Informace na úrovni zásob z aplikace Finance and Operations do Field Service [Pokročilý dotaz] 
- Úprava produktu (Field Service do Fin and Ops) - Úprava zásob z aplikace Field Service do Finance and Operations [Pokročilý dotaz] 
- Převody zásob (Field Service do Fin and Ops) - převody zásob z aplikace Field Service do Finance and Operations [Pokročilý dotaz] 
- Projekty (Fin and Ops do Field Service) - Seznam projektů z Finance and Operations do Field Service [Pokročilý dotaz] 
- pracovní příkazy s projektem (Field Service do Fin and Ops) - Pracovní příkazy v Field Service do příkazů k prodeji ve Finance and Operations, s podporou projektu [Pokročilý dotaz] 
- Produkty Field Service Products se skladovou jednotkou (Fin and Ops do Sales) - prodejné vydané produkty Finance and Operations pro Field Service, včetně skladové jednotky 

## <a name="system-requirements-for-finance-and-operations"></a>Systémové požadavky aplikaci Finance and Operations
Integrace Field Service podporuje následující verze:

- Aplikace Dynamics 365 for Finance and Operations verze 8.1.2 (prosinec 2019) byla vydána v prosinci 2019 a má číslo sestavení aplikace 8.1.195 s aktualizací platformy 22 (7.0.5095). 

## <a name="system-requirements-for-field-service"></a>Požadavky na systém pro Field Service
Chcete-li použít řešení integrace Field Service, je nutné nainstalovat následující komponenty:

- Field Service for Dynamics 365 (verze 8.2.0.286) nebo pozdější verze Dynamics 365 9.1.x - vydaná v listopadu 2018
- Řešení Prospect to Cash (P2C) pro Dynamics 365, verze 1.15.0.1 nebo novější. Řešení je k dispozici ke stažení na webech [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- Řešení 'Field Service Integration, Project and Inventory' pro Dynamics 365, verze 2.0.0.0 nebo novější. Řešení je k dispozici ke stažení na webech [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).

