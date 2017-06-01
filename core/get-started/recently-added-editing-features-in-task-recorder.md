---
title: "Nedávno přidané funkce úprav v Záznamníku úkolů"
description: "Pokud používáte Záznamník úkolů k vytváření průvodců úlohami, můžete upravit soubory efektivněji pomocí funkce popsané v tomto tématu."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Core
ms.custom: 266464
ms.assetid: b4640e67-4b92-4855-8041-1bfc71aadc47
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 272856c01074a352e3945f29e9cdf7655aaf22ba
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="recently-added-editing-features-in-task-recorder"></a>Nedávno přidané funkce úprav v Záznamníku úkolů

[!include[banner](../includes/banner.md)]


Pokud používáte Záznamník úkolů k vytváření průvodců úlohami, můžete upravit soubory efektivněji pomocí funkce popsané v tomto tématu.

Tyto funkce jsou k dispozici v nabídce **Nastavení &gt; Záznamník úloh &gt; Upravit záznam**.

-   Vložte kroky bez opětovného nahrávání celého souboru.
-   Přesuňte kroky v rámci dílčího úkolu bez opětovného nahrávání celého souboru.
-   Sbalte pole pro název a popis záznamu

## <a name="insert-steps-without-rerecording-the-entire-file"></a>Vložte kroky bez opětovného nahrávání celého souboru.
Nyní můžete přidat krok kamkoli v průvodci záznamem úloh bez přehrávání nebo opětovného nahrávání celého souboru.

1.  Vyberte krok, za který se má vložit nový krok. Zkontrolujte, zda je krok zvýrazněný.

Aby záznamník úkolů mohl vložit krok, musí mít otevřenou správnou stránku. Správná stránka je stránka, na které se nový krok objeví. Záznamník úkolů má mechanismus, který určuje, co je aktivní stránka, a zakáže funkci, pokud není otevřena správná stránka. 

[![tg1](./media/tg1.png)](./media/tg1.png) 


Pokud jste na správné stránce, je k dispozici možnost **Vložit krok**.

[![tg2](./media/tg2-231x300.png)](./media/tg2.png)

2. Klikněte na **Vložit krok**.

Po klepnutí na tlačítko **Vložit krok** Záznamník úkolů se přepne do režimu záznamu. Jakákoli akce provedená v uživatelském rozhraní nyní budou zaznamenány a doplněny jako kroky.

3. Klepněte na tlačítko **Stop**.

Můžete opakovat proces a přidat tolik kroků nebo přesunout tolik dílčích úkolů, kolik potřebujete (viz níže pro dílčí úkoly).

4. Po dokončení úprav Průvodce záznamem úloh klikněte na **Úpravy byly dokončeny**a pak zvolte jednu z možností uložení nebo publikování Průvodce záznamem úloh.

## <a name="move-steps-under-a-subtask-without-rerecording-the-entire-file"></a>Přesuňte kroky v rámci dílčího úkolu bez opětovného nahrávání celého souboru.
Kroky můžete v rámci dílčího úkolu přesouvat bez opětovného nahrávání celého souboru. Můžete také přesunout krok dílčího úkolu nebo koncového dílčího úkolu, pokud chcete seskupit stávající blok kroků.

1.  Vyberte krok nebo krok dílčího úkolu, který chcete přesunout. Zkontrolujte, zda je krok zvýrazněný.
2.  Klikněte na tři tečky a potom na tlačítko **Přesunout krok za**.

[![tg3](./media/tg3.png)](./media/tg3.png)

3. Vyberte krok nebo krok dílčího úkolu, za který chcete přesunout krok nebo krok dílčího úkolu. Záznamník úkolů krok přesune.

4. Chcete-li přesunout koncový krok dílčího úkolu, klikněte na tři tečky, klikněte na **Přesunout krok za** a potom vyberte krok, za který chcete krok dílčího úkolu přesunout.

Pokud chcete, aby první krok v průvodci záznamem úloh spadal do rámce dílčího úkolu, vytvořte krok dílčího úkolu jako druhý a pak do něj přesuňte první krok. Můžete přidat nebo přesunout tolik kroků nebo dílčích úkolů, kolik potřebujete.

5. Po dokončení úprav Průvodce záznamem úloh klikněte na **Úpravy byly dokončeny**a pak zvolte jednu z možností uložení nebo publikování Průvodce záznamem úloh.

## <a name="collapse-recording-name-and-description"></a>Sbalení pole pro název a popis záznamu
Můžete rozbalit a sbalit pole **Název záznamu** a **Popis záznamu**. Pokud jsou tato pole sbalena, další kroky budou zobrazeny v podokně úprav záznamníku úloh. 

[![tg4](./media/tg4-300x252.png)](./media/tg4.png)  

<a name="see-also"></a>Viz také
--------

[Vytváření dokumentace nebo školení pomocí záznamu úkolů](/dynamics365/operations/dev-itpro/user-interface/task-recorder)

[Stručná reference pro záznamník úloh](/dynamics365/operations/dev-itpro/user-interface/task-recorder-quick-reference)




