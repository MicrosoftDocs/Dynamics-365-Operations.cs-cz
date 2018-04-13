---
title: "Definice zásad výdajů"
description: "Můžete definovat zásady výdajů, které musí pracovníci dodržovat při zadávání a odesílání sestav výdajů a cestovních žádanek v aplikaci Microsoft Dynamics 365 for Finance and Operations."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 3b2a28fe6acf03e52c292048a797ce997f58bcce
ms.contentlocale: cs-cz
ms.lasthandoff: 03/26/2018

---

# <a name="expense-policies"></a>Zásady výdajů

[!INCLUDE [banner](../includes/banner.md)]

Můžete definovat zásady, které musí pracovníci dodržovat při zadávání a odesílání sestav výdajů a cestovních žádanek.         
Implementací zásad výdajů budete moci efektivně spravovat výdaje.         

Můžete například nastavit zásadu pro výdaje za hotel v New Yorku, která stanoví, že výdaje nesmí přesáhnout 250 USD za jeden nocleh.       
Pokud pracovník odešle sestavu výdajů nebo cestovní žádanku, ve kterém sazba za pokoj přesáhne tuto částku, systém oznámí        
pracovníkovi, že částka zásad pro výdaje byla překročena Můžete konfigurovat zprávu, kterou zaměstnanec obdrží při        
definování zásady.      
        
Můžete definovat tři typy zásad:         
        
- Upozornění - Umožňuje pracovníkovi odeslat výkaz výdajů nebo cestovní žádanku, ale výdaje budou označeny pro všechny schvalující osoby a        
  pro pozdější vykazování.        

- Chyba – Požaduje po pracovníkovi opravit výdaje, aby byly v souladu se zásadou před odesláním sestavy výdajů nebo cestovní žádanky.       
 
  - Zdůvodnění – Požaduje po pracovníkovi nebo manažerovi zadat odůvodnění částky přesahující zásadu před odesláním sestavy výdajů nebo cestovní žádanky.        
 
  Můžete také nastavit rozsah dat, pro které jsou zásady výdajů platné. Například letenky pro lety z Dánska      
  do New York City mohou být během cestovní špičky v průběhu dovolených drahé. Můžete definovat pravidlo pro ceny letenek, které bude omezovat      
  náklady na lety do New York City na 5000 DKK, a také zadat, že toto pravidlo má platit od 15. března      
  do 15. září.

