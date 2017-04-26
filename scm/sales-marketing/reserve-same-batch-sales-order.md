---
title: "Stejné dávky pro prodejní objednávky rezervovat"
description: "Tento článek vysvětluje, jak nastavit produkt pro umožnění rezervací zásob pomocí jedné dávky zásob."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: e9f48e6e057517bb7632e8c855f4439c446f3d30
ms.lasthandoff: 03/31/2017


---

# <a name="reserve-the-same-batch-for-a-sales-order"></a>Stejné dávky pro prodejní objednávky rezervovat

[!include[banner](../includes/banner.md)]


Tento článek vysvětluje, jak nastavit produkt pro umožnění rezervací zásob pomocí jedné dávky zásob.

Rezervace stejné dávky umožňuje rezervovat zásoby pro řádek prodejní objednávky z jediné dávky zásob. Například zákazník, který si objedná tapetu, může požadovat, aby byla celá objednávka zadána ze stejné dávky nebo šarže, aby se zabránilo nekonzistenci mezi rolemi. Chcete-li nastavit produkt tak, aby používal rezervaci stejné dávky, musí být aktivní následující nastavení ve skupině modelů zboží, skupině sledovací dimenze a skupině dimenze úložiště, kterou chcete přiřadit k produktu:

-   **Skupiny modelů položek** – Skupina modelů položek musí mít skupinu vybrána pole **Výběr ze stejné dávky** a **Požadavek na konsolidaci** ve skupině polí **Rezervace** pro zásady skladu.
-   **Skupiny sledovací dimenze** – Skupina sledovací dimenze musí mít vybráno pole **Plán disponibility podle dimenzí** pro číslo dávky.
-   **Skupiny dimenze úložiště** – Skupina dimenze úložiště musí mít vybráno pole **Plán disponibility podle dimenzí** pro pole **Lokalita** a **Sklad**.

Když rezervujete zásoby pro produkt na řádku prodejní objednávky, který je nastaven pro výběr ze stejné dávky, aplikace Microsoft Dynamics 365 for Operations se pokusí rezervovat objednané množství z jediné dávky zásob. Dále jsou zvažovány jakékoli požadavky atributů dávek. Pokud nelze množství vyplnit z jedné dávky, zobrazí se strana **Konflikt rezervací stejné dávky**. Tato stránka popisuje problémy a také akce, které lze provést, chcete-li pokračovat v rezervaci. Následující podmínky mohou bránit rezervaci dávky:

-   Dispoziční kód dávky má možnost **Blokovat rezervaci** pro prodej označenu jako **Blokováno**.
-   Platnost dávky vypršela, na základě data vypršení platnosti a všech dnů prodejnosti příslušného odběratele. Položky lze stále ještě považována za rezervaci, pokud se skupina modelu zboží pro položku „nejdříve končící platnost – nejdříve ze skladu“ (FEFO) – řízenou podle data a pokud je jako kritérium pro výdej vybráno datum doporučené spotřeby.
-   Dávka neobsahuje dostatek zbývajících dní skladovatelnosti na základě data vypršení platnosti a data doporučené spotřeby, a navíc žádné dny prodejnosti odběratele.





