---
title: "Zobrazení nákladů na vyráběnou položku"
description: "Konstantní náklady na vyráběnou položku reflektují doby nastavení operace a komponent s konstantní kvalitou nebo s konstantní odpadovostí."
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 274483
ms.assetid: 6f5b851b-c5a7-43ef-b380-0d316667c1ef
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 66dbd107b47b8a064cbe2e284bcabea47c471089
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="display-charges-for-a-manufactured-item"></a>Zobrazení nákladů na vyráběnou položku

[!include[banner](../includes/banner.md)]


Konstantní náklady na vyráběnou položku reflektují doby nastavení operace a komponent s konstantní kvalitou nebo s konstantní odpadovostí.

Vypočtená částka nákladů na zboží může být zobrazena s náklady na jednotku zboží. Vedlejší náklady však někdy bývají zobrazeny jako dvě samostatná pole a nejsou zahrnuty do jednotkových nákladů na zboží. Pokud se poplatky zobrazují s použitím samostatných polí, bude v jednom poli zobrazena celková částka nákladů a ve druhém poli bude zobrazena velikost šarže nákladů (označená jako cenová jednotka), která byla použita pro amortizaci částky. Na stránce Cena zboží se například náklady zobrazují jako dvě samostatná pole. Na stránce Dokončené se však zobrazují celkové náklady na zboží podle jednotky a amortizované náklady jsou zahrnuty do jednotkových nákladů.

Náklady pro vyráběnou položku jsou vždy zahrnuty do jednotkových nákladů dané položky pro účely standardních nákladů. Mohou být volitelně zahrnuty pro účely plánovaných nákladů. Zásady v rámci nákladové verze vynucují zahrnutí nákladů do nákladů na vyráběné zboží. Když aktivujete záznam nákladů na zboží, budou aktualizovány náklady s použitím údajů o základních nákladech, které se zobrazují na stránce Cena zboží. Vedlejší náklady jsou zobrazeny jako dvě samostatná pole a nejsou zahrnuty do jednotkových nákladů na zboží. Při každé aktivaci jsou aktualizovány údaje o základních nákladech na zboží, a to i tehdy, pokud aktivace odpovídá různým pracovištím. Z tohoto důvodu byste měli považovat informace o základních nákladech za referenční informace.






