---
title: Možnosti vykazování v aplikaci Talent
description: Toto téma vysvětluje postup řešení problému, kdy zákazník chce přizpůsobit sestavy aplikace Dynamics 365 Talent nebo vytvořit nové sestavy.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 50342c847200d015a66c6f22007070bb26c6caef
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009345"
---
# <a name="reporting-options-in-talent"></a>Možnosti vykazování v aplikaci Talent

[!include [banner](includes/banner.md)]

**Podrobnosti o prostředí**

Tento problém se vztahuje na všechna prostředí.

**Příznak**

Zákazník chce přizpůsobit sestavy aplikace Dynamics 365 Talent nebo vytvořit nové sestavy.

**Výdej**

Uživatel nemůže přizpůsobit integrované sestavy Microsoft Power BI.

**Řešení**

- Data aplikace Core HR, která přecházejí do Common Data Service, lze vykazovat prostřednictvím konektoru PowerApps Common Data Service do Power BI Desktop. Všimněte si, že Common Data Service obsahuje podmnožinu dat aplikace Core HR. Další informace o Power BI a řídicích panelech uvádí téma [Vytváření sestav a řídicích panelů Power BI pomocí PowerApps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).
- Elektronické výkaznictví je k dispozici pro některé sestavy v aplikaci Talent. Přizpůsobení požadované zákazníky lze provádět pomocí možností konfigurace elektronického výkaznictví.
- Data lze exportovat do aplikace Microsoft Excel nebo Microsoft Word pomocí různých datových entit, které aplikace Talent nabízí prostřednictvím integrace s Microsoft Office.

**Dlouhodobé řešení**

Další možnosti Power BI budou k dispozici a více dat a entit se stane součástí Common Data Service.
