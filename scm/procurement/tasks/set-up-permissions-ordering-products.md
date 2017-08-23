--- 
title: "Nastavení oprávnění pro objednávání produktů jménem jiného uživatele"
description: "Tento postup popisuje, jak udělit zaměstnancům oprávnění k přípravě nákupních žádanek jménem ostatních pracovníků."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 8f12f9eb949034f9bef91d93f31a0f3373e39e98
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a>Nastavení oprávnění pro objednávání produktů jménem jiného uživatele

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje, jak udělit zaměstnancům oprávnění k přípravě nákupních žádanek jménem ostatních pracovníků. Jinak řečeno, pořizovatel" nákupního požadavku může vytvořit požadavek za jiného žadatele. Postup rovněž ukazuje, jak udělit pracovníkovi oprávnění objednat zboží a služby u různých právnických osob nebo provozních jednotek. Obvykle jsou tyto úlohy prováděny vedoucím nákupu. Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a>Udělení oprávnění zadat nákupní žádanky jménem jiného pracovníka
1. Přejděte na Zásobování a zdroje > Nastavení > Zásady > Oprávnění nákupní žádanky.
    * Ujistěte se, že je v poli Aktuální zobrazení vybrána možnost Podle pořizovatele.  V seznamu v levém podokně se zobrazí osoby, kterým mohou mít udělena oprávnění k přípravě žádanek jménem ostatních uživatelů.  
2. Vyberte osobu, které chcete udělit oprávnění (pořizovatel).
3. Klepněte na možnost Přidat.
4. Vyhledejte a vyberte osobu, kterou chcete přidat jako žadatele.
    * Žadatel je osoba, jejímž jménem může pořizovatel vytvořit požadavky.  
    * V poli Autorizace vyberte Konkrétní, pokud má být pořizovatel schopen vytvářet nákupní žádanky jménem vybraného pracovníka. Vyberte Vykazování, pokud pořizovatel má být také schopen vytvářet nákupní žádanky jménem všech pracovníků, kteří jsou podřízeni danému pracovníkovi.  
5. V poli Platnost zadejte datum.
6. Do pole Vypršení platnosti zadejte datum.

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a>Zobrazení zpracovatelů, kteří mají oprávnění k vytváření nákupních žádanek pro vybraného pracovníka
1. V poli Aktuální zobrazení vyberte „Podle žadatele“.
    * Toto zobrazení popisuje seznam pořizovatelů, kterým byla udělena oprávnění k vytváření nákupních žádanek jménem vybraného zaměstnance.  
2. Pomocí rychlého filtru vyhledejte pracovníka, kterého jste právě vytvořili jako žadatele.
3. Vyberte žadatele.
    * Seznam Pořizovatel popisuje uživatele, kteří mají oprávnění k objednání položek jménem žadatele, který je vybrán v levém podokně.   Zde můžete přidat další zpracovatele.   Toto zobrazení umožňuje také udělit oprávnění žadatelům pro vytvoření žádanek u právnických osob a provozních jednotek, které nejsou primární právnickou osobou nebo provozní jednotkou daného uživatele.  


