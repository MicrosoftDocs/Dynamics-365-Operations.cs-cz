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
ms.sourcegitcommit: 03a932652cdd93b2a5917d0fca72809d1648b678
ms.openlocfilehash: b1acf0b64914a3199fcf44f8377e32b26f0af99e
ms.contentlocale: cs-cz
ms.lasthandoff: 04/25/2018

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

Pokud se chcete podívat na příklad, jak můžete synchronizovat pracovní objednávku mezi aplikací Field Service a Finance and Operations, podívejte se na krátké video na YouTube:

> [!Video https://www.youtube.com/embed/hAB4TDVMjxU]

[Synchronizace pracovního příkazu mezi službou Field Service a aplikací Finance and Operations (video na YouTube)](https://youtu.be/hAB4TDVMjxU)

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

