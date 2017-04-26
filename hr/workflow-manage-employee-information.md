---
title: "Pracovní postupy lze použít ke správě informací o zaměstnancích"
description: "Toto téma vysvětluje, jak můžete použít funkci pracovního postupu pro lidské zdroje ke správě informací o zaměstnancích. Například můžete přidružit pracovní pozice a konfigurace pracovního postupu pro schválení zahájení po zaměstnanci změnit jejich záznam."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: a76ec0cd86bcc810b42ae3cd8efd8a584e6c4da3
ms.openlocfilehash: f286436aa4833babaeb3de875ee393d18e5f8eea
ms.lasthandoff: 03/31/2017


---

# <a name="use-workflows-to-manage-employee-information"></a>Pracovní postupy lze použít ke správě informací o zaměstnancích

[!include[banner](includes/banner.md)]


Toto téma vysvětluje, jak můžete použít funkci pracovního postupu pro lidské zdroje ke správě informací o zaměstnancích. Například můžete přidružit pracovní pozice a konfigurace pracovního postupu pro schválení zahájení po zaměstnanci změnit jejich záznam.

Možnosti pracovních postupů pro lidské zdroje obsahuje velký počet pracovních postupů pro správu lidských zdrojů aktivit. Navíc četné možnosti jsou k dispozici, aby mohli upravit konkrétní pracovní postupy a přidružit hierarchie vykazování. Pracovní postupy jsou k dispozici pro správu změn na několik standardních typů informací o zaměstnancích. Pozice můžete přidružit pracovní postup. Poté Pokud zaměstnanci změnit jejich záznam zaměstnance, zahájení pracovního postupu, který vyžaduje schválení před uložením nové informace. Pro následující typy informací, které vám pomohou efektivně spravovat změny a zachovat přesné údaje zaměstnanců jsou předdefinované pracovní postupy:

-   Identifikační čísla
-   Kurzy
-   Vzdělání
-   Obrázek
-   Zapůjčené položky
-   Odborné zkušenosti
-   Zkušenost z projektu
-   Dovednosti
-   Pozice důvěry
-   Akce lidských zdrojů
-   Registrace kurzu

Když zaměstnanci přijatí, přeneseny nebo ukončena, pracovní postup může zahrnovat proces recenzování. Tímto způsobem může být přezkoumána dokumentu nebo podmínky akce může být definován jako součást pracovního postupu. Po dokončení procesu recenzování bylo dokončeno dokladu nebo akce a pracovní postup přejde ke kroku konečné schválení.

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>Hierarchie pozic přidružení pracovního postupu
Pracovní postup lze přidružit jakékoli hierarchii, který konfigurujete. Například pozice souvisí s organizační hierarchii matice, mohou nakonfigurovat pracovní postup, který směruje výdaje pro konkrétní projekt realizace projektu místo vedoucího zaměstnance, který je přidružen k této pozici. Chcete-li vytvořit nový pracovní postup nebo změnit existující pracovní postup na **lidských zdrojů pracovního postupu** klepněte na tlačítko **nový**. Vyberte pracovní postup v seznamu spustit Návrháře pracovního postupu. Chcete-li vytvořit nový pracovní postup nebo změnit existující pracovního postupu kroky můžete použít návrháře. Změníte-li existující pracovní postup, jsou změny uloženy jako novou verzi. Proto můžete se vždy vrátit zpět k předchozí verzi Pokud budete muset.

## <a name="configure-a-human-resources-workflow"></a>Konfigurace pracovního postupu lidských zdrojů
Chcete-li konfigurovat základní pracovní postup, který je spuštěn po zaměstnanci požadovat změny osobního identifikačního, postupujte takto.

1.  Na **workflowy lidských zdrojů** klepněte na tlačítko **nové**.
2.  V seznamu pracovních postupů, které jsou k dispozici, vyberte **identifikačních čísel**.
3.  Klepněte na tlačítko **spuštění** spuštění Návrháře pracovního postupu a po zobrazení výzvy zadejte uživatelské jméno a heslo.
4.  Přetáhněte **identifikační číslo schválení** prvek ze seznamu prvků workflowu na plátno návrháře.
5.  Prvek schválení pro připojení **spuštění** a **Dokončit**.
6.  Poklepejte na **schválit prvek**a potom klepněte pravým tlačítkem myši a vyberte **vlastnosti**.
7.  Postupujte takto Chcete-li přidat pracovní položku pokyny:
    1.  Vyberte **přiřazení**a potom vyberte **hierarchie** ve skupinovém rámečku přiřazení typu.
    2.  Ve skupinovém rámečku **hierarchie** výběru, vyberte **nastavitelné hierarchie**.
    3.  Přidat podmínku ukončení a zavřete stránku.

8.  Dokončete všechny další pokyny (by měl existovat žádná další upozornění).
9.  Klikněte na možnost **Uložit a zavřít**. Nový pracovní postup aktivovat, pokud dialogové okno se otevře a vyberte **aktivní**.
10. Přejít na **lidských zdrojů**&gt;**pozice**&gt;**typy hierarchie pozice**.
11. Vyberte **matice**.
12. Přidat **identifikační číslo pracovníka** pracovního postupu do seznamu.





