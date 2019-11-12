---
title: Rozvrh údržby
description: Tohle téma popisuje rozvrh údržby v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fab21d6f3a1b7386d304ece6ebf3b93cdc0c504d
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570000"
---
# <a name="maintenance-schedule"></a>Rozvrh údržby

[!include [banner](../../includes/banner.md)]

 

Rozvrh údržby obsahuje seznam všech očekávaných plánů preventivní údržby, požadavků na údržbu a pořadí údržby, které mají být provedeny. Některé řádky rozvrhu mohly být převedeny na pracovní příkazy.

Čtyři zobrazení rozvrhu údržby se mírně liší v závislosti na řádcích rozvrhu údržby, které chcete zobrazit.

| Položka nabídky                  | Popis obsahu                                                                                                                                             |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Rozvrh kompletní údržby       | Zobrazí se všechny řádky rozvrhu údržby.     |
| Můj plán majetku        | V tomto seznamu jsou uvedeny všechny řádky rozvrhu údržby obsahující majetek instalovaný ve funkčních místech, ke kterému se vztahujete coby pracovník (nastavení v části [Pracovníci údržby a skupiny pracovníků](../setup-for-objects/workers-and-worker-groups.md)). |
| Otevřít řádky rozvrhu údržby | Řádky rozvrhu údržby se stavem „Vytvořeno“ jsou zobrazeny v tomto seznamu, což znamená, že dosud nebyly převedeny na pracovní příkaz, nebo byly zrušeny.                                            |
| Otevřít skupiny rozvrhu údržby | V tomto seznamu jsou uvedeny řádky rozvrhu údržby související s fondem pracovních příkazů.                                                                                                                  |

>[!NOTE]
>Pokud je v několika fondech pracovních příkazů uveden řádek rozvrhu údržby (viz [Fondy pracovních příkazů](../work-orders/work-order-pools.md)), zobrazí se jeden záznam pro každý fond v části **Otevřené fondy rozvrhu údržby**. To je provedeno za účelem optimalizace možností filtrování ve fondech pracovních příkazů.

Otevření rozvrhu údržby:

1. Klikněte na položky v částech **Správa majetku** > **Společné** > **Rozvrh údržby** > **Všechny rozvrhy údržby** nebo **Otevřené řádky rozvrhu údržby** nebo **Otevřené fondy rozvrhu údržby**.

2. Chcete-li aktualizovat rozvrh údržby, klikněte na možnost **Plán údržby** nebo **Pořadí údržby**. 

3. Řádek rozvrhu údržby můžete upravit tak, že jej vyberete a kliknete na tlačítko **Upravit**. Můžete například snadno aktualizovat úroveň služeb nebo pracovníka odpovědného za práci. Upravit lze pouze řádky rozvrhu údržby, které ještě nebyly připojeny k pracovnímu příkazu.

4. Řádek rozvrhu údržby můžete odstranit tak, že jej vyberete na stránce seznamu a kliknete na tlačítko **Odstranit**.

5. Řádek rozvrhu údržby můžete zahodit tak, že jej vyberete na stránce seznamu a kliknete na tlačítko **Zahodit**. Tato funkce je užitečná, pokud má například majetek jeden plán údržby 2 000 km a druhý plán údržby 10 000 km. Poté může být vhodné zahodit řádek vytvořený z plánu údržby 2 000 km, pokud se shoduje s 10 000 km, 20 000 km, 30 000 km atd. Pokud zahodíte řádek rozvrhu údržby související s plánem údržby, tento řádek se po naplánování plánu údržby již nikdy nezobrazí.

6. Chcete-li, aby byly všechny vybrané řádky zahrnuty do stejného fondu pracovních příkazů , můžete vybrat počet řádků rozvrhu údržby v části **Všechny rozvrhy údržby** a kliknout na položku **Fond pracovních příkazů**.

7. Můžete vybrat počet řádků rozvrhu údržby v části **Všechny rozvrhy údržby** nebo **Otevřené řádky rozvhu** údržby nebo **Otevřené fondy rozvrhu údržby** a kliknout na **Upravit plán**, chcete-li provést stejné úpravy na několika řádcích. Můžete změnit očekávaná počáteční a koncová data, úroveň služeb a skupinu zodpovědných pracovníků údržby nebo zodpovědného pracovníka údržby související s vybranými řádky rozvrhu údržby.

- Pokud řádek rozvrhu údržby souvisí s pracovním příkazem, v poli **Pracovní příkaz** se zobrazí ID pracovního příkazu.  
- V zobrazení podrobností **Všechen majetek** > na záložce s náhledem **Plány údržby majetku** můžete vybrat plány údržby pro majetek. Později, pokud odstraníte řádek plánu údržby související s majetkem v části **Všechen majetek**, automaticky odstraníte také všechny řádky rozvrhu údržby se stavem „Vytvořeno“, které byly vytvořeny na základě plánu údržby. Viz také [Vytvoření majetku](../objects/create-an-object.md).

Na následujícím obrázku je uvedena stránka seznamu **Všechny rozvrhy údržby**.

![Obrázek č. 1](media/16-preventive-maintenance.png)

