---
title: Nastavení oprávnění pro objednávání produktů jménem jiného uživatele
description: Toto téma vysvětluje, jak udělit zaměstnancům oprávnění k přípravě nákupních žádanek jménem ostatních pracovníků.
author: kamaybac
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchReqAuthorization, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d0408085d401a34a409bfe46bc6845a9c81a2eea
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811887"
---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a>Nastavení oprávnění pro objednávání produktů jménem jiného uživatele

[!include [banner](../../includes/banner.md)]

Toto téma vysvětluje, jak udělit zaměstnancům oprávnění k přípravě nákupních žádanek jménem ostatních pracovníků. Jinak řečeno, „pořizovatel“ nákupního požadavku může vytvořit požadavek za jiného „žadatele“. Postup rovněž ukazuje, jak udělit pracovníkovi oprávnění objednat zboží a služby u různých právnických osob nebo provozních jednotek. Obvykle jsou tyto úlohy prováděny vedoucím nákupu. Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a>Udělení oprávnění zadat nákupní žádanky jménem jiného pracovníka
1. V navigačním podokně přejděte na **Moduly > Zásobování a nákup > Nastavení > Zásady > Oprávnění nákupní žádanky**. Ujistěte se, že je v poli **Aktuální zobrazení** vybrána možnost **Podle pořizovatele**. V seznamu v levém podokně se zobrazí osoby, kterým mohou mít udělena oprávnění k přípravě žádanek jménem ostatních uživatelů.  
2. Vyberte osobu, které chcete udělit oprávnění (pořizovatel).
3. Vyberte **přidat**.
4. Vyhledejte a vyberte osobu, kterou chcete přidat jako žadatele.
    - Žadatel je osoba, jejímž jménem může pořizovatel vytvořit požadavky.  
    - V poli **Autorizace** vyberte **Konkrétní**, pokud má být pořizovatel schopen vytvářet nákupní žádanky jménem vybraného pracovníka. Vyberte **Vykazování**, pokud pořizovatel má být také schopen vytvářet nákupní žádanky jménem všech pracovníků, kteří jsou podřízeni danému pracovníkovi.  
5. V poli **Platnost** zadejte datum.
6. Do pole **Vypršení platnosti** zadejte datum.

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a>Zobrazení zpracovatelů, kteří mají oprávnění k vytváření nákupních žádanek pro vybraného pracovníka
1. V poli **Aktuální zobrazení** vyberte **Podle žadatele**. Toto zobrazení popisuje seznam pořizovatelů, kterým byla udělena oprávnění k vytváření nákupních žádanek jménem vybraného zaměstnance.  
2. Pomocí rychlého filtru vyhledejte pracovníka, kterého jste právě vytvořili jako žadatele.
3. Vyberte žadatele. Seznam Pořizovatel popisuje uživatele, kteří mají oprávnění k objednání položek jménem žadatele, který je vybrán v levém podokně.  Zde můžete přidat další zpracovatele. Toto zobrazení umožňuje také udělit oprávnění žadatelům pro vytvoření žádanek u právnických osob a provozních jednotek, které nejsou primární právnickou osobou nebo provozní jednotkou daného uživatele.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]