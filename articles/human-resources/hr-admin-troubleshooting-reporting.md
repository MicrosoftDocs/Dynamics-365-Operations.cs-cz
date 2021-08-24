---
title: Možnosti vykazování
description: Tento článek vysvětluje postup řešení problému, kdy zákazník chce přizpůsobit sestavy aplikace Microsoft Dynamics 365 Human Resources nebo vytvořit nové sestavy.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 733ae0725f6fd9508e7d9e168d97f30a6c37f442930fb76c9415358c4dc888ec
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740784"
---
# <a name="reporting-options"></a>Možnosti vykazování

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**Podrobnosti o prostředí**

Tento problém se vztahuje na všechna prostředí.

**Příznak**

Zákazník chce přizpůsobit sestavy aplikace Dynamics 365 Human Resources nebo vytvořit nové sestavy.

**Výdej**

Uživatel nemůže přizpůsobit integrované sestavy Microsoft Power BI.

**Řešení**

- Data aplikace Human Resources, která přecházejí do Dataverse, lze vykazovat prostřednictvím konektoru Power Apps Dataverse do Power BI Desktop. Všimněte si, že Dataverse obsahuje podmnožinu dat aplikace Human Resources. Další informace o Power BI a řídicích panelech uvádí téma [Vytváření sestav a řídicích panelů Power BI pomocí Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).
- Elektronické výkaznictví je k dispozici pro některé sestavy v aplikaci Human Resources. Přizpůsobení požadované zákazníky lze provádět pomocí možností konfigurace elektronického výkaznictví.
- Data lze exportovat do aplikace Microsoft Excel nebo Microsoft Word pomocí různých datových entit, které aplikace Human Resources nabízí prostřednictvím integrace s Microsoft Office.

**Dlouhodobé řešení**

Další možnosti Power BI budou k dispozici a více dat a entit se stane součástí Dataverse.


[!INCLUDE[footer-include](../includes/footer-banner.md)]