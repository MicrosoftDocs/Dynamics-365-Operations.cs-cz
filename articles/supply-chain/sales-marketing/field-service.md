---
title: "Integrace s aplikací Microsoft Dynamics 365 for Field Service"
description: "Toto téma obsahuje přehled integrace s aplikací Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
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
ms.sourcegitcommit: a57e23691a6b4d48c6b8dd6d1f61fc9730365b39
ms.openlocfilehash: 0c1268d2fddcf7b28ecfc3197f21e9d30a5a5855
ms.contentlocale: cs-cz
ms.lasthandoff: 05/31/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a>Integrace s aplikací Microsoft Dynamics 365 for Field Service

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations umožňuje synchronizaci obchodních procesů mezi aplikací Finance and Operations a Microsoft Dynamics 365 for Field Service. Scénáře integrace jsou konfigurovány s použitím rozsáhlých šablon integrátoru dat a Common Data Service (CDS) pro umožnění synchronizace obchodních procesů.

[![Synchronizace obchodních procesů mezi aplikacemi Finance a Operations and Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)

První fáze integrace mezi  Field Service a Finance and Operations se zaměřuje na povolení pracovních příkazů a smluv ve Field Service pro fakturaci ve Finance and Operations. Podporovaný tok začíná ve Field Service, kde jsou informace z pracovních příkazů synchronizovány s Finance and Operations jako prodejní objednávky. V modulu Finance and Operations jsou prodejní objednávky fakturovány ke generování faktur. Kromě toho jsou informace z faktur smluv ve službě Field Service synchronizovány do aplikace Finance and Operations. Integrátor dat Microsoft Dynamics 365 synchronizuje data pomocí upravitelné projektů. Standardní šablony lze používat k vytváření projektů vlastní integrace, kde další standardní a vlastní pole a také entity, mohou být mapovány pro účely úpravy integrace a plnění konkrétních požadavků.

První fáze integrace mezi Field Service a Finance and Operations umožňuje synchronizaci následujících položek:

- [Produkty v modulu Finance and Operations na produkty v modulu Field Service, které zahrnují informace o typu produktu](field-service-product.md)
- [Pracovní příkazy ve službě Field Service do prodejních objednávek v aplikaci Finance and Operations](field-service-work-order.md)
- [Faktury v aplikaci Field Service na volné textové faktury ve Finance and Operations](field-service-invoice.md)

Příklad synchronizace výrobního příkazu mezi Field Service a Finance and Operations uvádí krátké video na YouTube [Synchronizace výrobního příkazu mezi Dynamics 365 for Field Service a Finance and Operations](https://www.youtube.com/watch?v=hAB4TDVMjxU).

## <a name="system-requirements-for-finance-and-operations"></a>Systémové požadavky aplikaci Finance and Operations
Integrace Field Service podporuje následující verze:

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a>Dynamics 365 for Finance and Operations, verze 8.0 (duben 2018) nebo pozdější

- Aplikace Dynamics 365 for Finance and Operations verze 8.0 (duben 2018) byla vydána v dubnu 2018 a má číslo sestavení aplikace 8.0.30.8020 s aktualizací platformy 15 (7.0.4841.35234). 

## <a name="system-requirements-for-field-service"></a>Požadavky na systém pro Field Service
Chcete-li použít řešení integrace Field Service, je nutné nainstalovat následující komponenty:

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a>Microsoft Dynamics 365 for Field Service 9.0 or later

- Dynamics 365 for Field Service verze 1612 (9.0.1.733) (DB 9.0.1.733) online nebo vyšší verze.
- Řešení Prospect to Cash (P2C) pro Dynamics 365, verze 1.15.0.1 nebo novější. Řešení je k dispozici ke stažení na webech [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- Řešení integrace Field Service pro Dynamics 365, verze 1.0.0.0 nebo novější. Řešení je k dispozici ke stažení na webech [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration).

