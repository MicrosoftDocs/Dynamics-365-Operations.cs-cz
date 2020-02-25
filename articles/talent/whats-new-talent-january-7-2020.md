---
title: Co je nového nebo změněného v aplikaci Dynamics 365 Talent (7. ledna 2020)
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-01-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e227c614fdbfe6f3dd410f1a533c593979abf1ec
ms.sourcegitcommit: 615ed3e4260192ba36826e128f1afa1588e94845
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/21/2020
ms.locfileid: "2974423"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-7-2020"></a>Co je nového nebo změněného v aplikaci Dynamics 365 Talent (7. ledna 2020)

Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Změny v aplikaci Attract

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Změny v aplikaci Onboard

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Změny v Core HR

Změny popsané v této části se vztahují na číslo sestavení 8.1.2697. Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Microsoft Dynamics Lifecycle Services (LCS).

 
### <a name="cant-delete-workers-that-dont-have-employment-records---386157"></a>Nelze odstranit pracovníky, kteří nemají záznamy o zaměstnání – (386157)

Tato změna přidá možnost odstranění do formuláře **Pracovníci bez zaměstnání**. Pracovníci se v tomto formuláři zobrazují v případě, že pro daného pracovníka neexistuje budoucí, aktivní nebo historická zaměstnání. V této verzi je možnost odstranění povolena pouze správcům systému. Avšak ve vydání příští týden bude zabezpečení aktualizováno tak, aby všichni uživatelé s rolí asistenta lidských zdrojů mohli odebírat zaměstnance bez zaměstnání. Tyto změny můžete provést také ručně pomocí následujících kroků.

1. Přejděte na **Konfigurace zabezpečení**.
2. Na kartě **Oprávnění** vyfiltrujte seznam **Oprávnění**, aby bylo možné **spravovat pracovníky**.
3. Ve sloupci **Reference** vyberte **zobrazit položky nabídky**.
4. V **Zobrazit položky nabídky** vyberte **HcmWOrkersWithoutEmployment**.
5. Nastavte oprávnění **Odstranit**, které má být uděleno.
6. Vyberte kartu **nepublikované objekty**.
7. Zvolte **Publikovat vše**.
