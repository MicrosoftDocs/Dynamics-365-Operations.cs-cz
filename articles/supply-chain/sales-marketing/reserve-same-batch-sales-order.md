---
title: Rezervace stejné dávky pro prodejní objednávku
description: Tento článek vysvětluje, jak nastavit produkt pro umožnění rezervací zásob pomocí jedné dávky zásob.
author: omulvad
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e0937be76aa687ed986ff83e67f2db3e2dadd0f0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807649"
---
# <a name="reserve-the-same-batch-for-a-sales-order"></a>Rezervace stejné dávky pro prodejní objednávku

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje, jak nastavit produkt pro umožnění rezervací zásob pomocí jedné dávky zásob.

Rezervace stejné dávky umožňuje rezervovat zásoby pro řádek prodejní objednávky z jediné dávky zásob. Například zákazník, který si objedná tapetu, může požadovat, aby byla celá objednávka zadána ze stejné dávky nebo šarže, aby se zabránilo nekonzistenci mezi rolemi. Chcete-li nastavit produkt tak, aby používal rezervaci stejné dávky, musí být aktivní následující nastavení ve skupině modelů zboží, skupině sledovací dimenze a skupině dimenze úložiště, kterou chcete přiřadit k produktu:

- **Skupiny modelů položek** – Skupina modelů položek musí mít skupinu vybrána pole **Výběr ze stejné dávky** a **Požadavek na konsolidaci** ve skupině polí **Rezervace** pro zásady skladu.
- **Skupiny sledovací dimenze** – Skupina sledovací dimenze musí mít vybráno pole **Plán disponibility podle dimenzí** pro číslo dávky.
- **Skupiny dimenze úložiště** – Skupina dimenze úložiště musí mít vybráno pole **Plán disponibility podle dimenzí** pro pole **Lokalita** a **Sklad**.

Když rezervujete zásoby pro produkt na řádku prodejní objednávky, který je nastaven pro výběr ze stejné dávky, systém se pokusí rezervovat objednané množství z jediné dávky zásob. Dále jsou zvažovány jakékoli požadavky atributů dávek. Pokud nelze množství vyplnit z jedné dávky, zobrazí se strana **Konflikt rezervací stejné dávky**. Tato stránka popisuje problémy a také akce, které lze provést, chcete-li pokračovat v rezervaci. Následující podmínky mohou bránit rezervaci dávky:

- Dispoziční kód dávky má možnost **Blokovat rezervaci** pro prodej označenu jako **Blokováno**.
- Platnost dávky vypršela, na základě data vypršení platnosti a všech dnů prodejnosti příslušného odběratele. Položky lze stále ještě považována za rezervaci, pokud se skupina modelu zboží pro položku „nejdříve končící platnost – nejdříve ze skladu“ (FEFO) – řízenou podle data a pokud je jako kritérium pro výdej vybráno datum doporučené spotřeby.
- Dávka neobsahuje dostatek zbývajících dní skladovatelnosti na základě data vypršení platnosti a data doporučené spotřeby, a navíc žádné dny prodejnosti odběratele.

U položek přidružených ke skupině dimenzí úložiště, která má povolenu možnost **Použít procesy řízení skladu**, lze vyhradit specifická čísla dávek pomocí hierarchie rezervací, kde je definována dimenze zásob čísla dávky nad dimenzí skladového místa. Tento typ hierarchie rezervací je také známý jako *Batch-above \[location\]*. Stránka **Rezervace dávky** pro řádky prodejního a převodního příkazu umožňuje také vybrat a rezervovat více řádků na základě dostupných čísel dávek. Další informace, jak postupovat v případě, že používáte hierarchii rezervací s dimenzí čísla dávky pod skladovým místem (*Batch-below \[location\]*), naleznete v části [Flexibilní zásada rezervace dimenze na úrovni skladu](../warehousing/flexible-warehouse-level-dimension-reservation.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
