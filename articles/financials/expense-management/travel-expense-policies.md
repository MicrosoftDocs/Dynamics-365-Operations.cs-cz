---
title: "Definice zásad výdajů"
description: "Můžete definovat zásady výdajů, které musí pracovníci dodržovat při zadávání a odesílání sestav výdajů a cestovních žádanek v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition."
author: saraschi2
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 9a5ce1a3b6519b510c9f5aa5618ab91f77a2d91a
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="expense-policies"></a>Zásady výdajů

[!include[banner](../includes/banner.md)]

Můžete definovat zásady, které musí pracovníci dodržovat při zadávání a odesílání sestav výdajů a cestovních žádanek. Implementací zásad výdajů budete moci efektivně spravovat výdaje. 

Můžete například nastavit zásadu pro výdaje za hotel v New Yorku, která stanoví, že výdaje nesmí přesáhnout 250 USD za jeden nocleh. Pokud pracovník odešle sestavu výdajů nebo cestovní žádanku, ve kterých cena za pokoj překročí tuto částku, systém upozorní pracovníka, že překročil částku zásady nastavenou pro výdaje. Můžete konfigurovat zprávu, kterou zaměstnanec obdrží při definování zásady. 

Můžete definovat tři typy zásad: 

 - Upozornění - Umožňuje pracovníkovi odeslat výkaz výdajů nebo cestovní žádanku, ale výdaje budou označeny pro všechny schvalující osoby a  
 pro pozdější vykazování. 
 - Chyba – Požaduje po pracovníkovi opravit výdaje, aby byly v souladu se zásadou před odesláním sestavy výdajů nebo cestovní žádanky. 
 - Zdůvodnění – Požaduje po pracovníkovi nebo manažerovi zadat odůvodnění částky přesahující zásadu před odesláním sestavy výdajů nebo cestovní žádanky. 

Můžete také nastavit rozsah dat, pro které jsou zásady výdajů platné. Například ceny letenek pro lety mezi Dánskem a New Yorkem mohou být během vrcholné prázdninové sezóny drahé. Můžete definovat pravidlo výdajů pro lety, které omezuje náklady na lety do New Yorku až do výše 5000 DKK, a můžete specifikovat, že toto pravidlo bude platné od 15. března do 15. září. 

