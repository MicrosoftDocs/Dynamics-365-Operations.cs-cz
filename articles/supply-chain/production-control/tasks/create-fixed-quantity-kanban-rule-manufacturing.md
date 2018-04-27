--- 
title: "Vytvoření kanbanového pravidla pro pevné množství pro výrobu"
description: "Tento postup se zaměřuje na nastavení potřebného k vytvoření pevné výroby kanbanového pravidla pro zaměření aktivit přeměny v pracovní buňce ve štíhlém prostředí."
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8020a37bf0c725fc260574cfe87861aeb017519e
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-fixed-quantity-kanban-rule-for-manufacturing"></a>Vytvoření kanbanového pravidla pro pevné množství pro výrobu

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Tento postup se zaměřuje na nastavení potřebného k vytvoření pevné výroby kanbanového pravidla pro zaměření aktivit přeměny v pracovní buňce ve štíhlém prostředí. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Tento postup je určen pro technologa výrobních procesů nebo správce hodnotového proudu, kteří připravují výrobu nového nebo změněného výrobku.


## <a name="create-new-kanban-rule"></a>Vytvořit nové kanbanové pravidlo
1. Otevřete Kanbanová pravidla.
2. Klikněte na položku Nová.
    * Všimněte si, že výchozí typ je výroba a strategie doplnění je pevná. Není nutné tyto parametry měnit.  
3. V poli První aktivita plánu zadejte nebo vyberte hodnotu.
    * Toto je aktivita, která bude provedena pro kanbany založené na tomto kanbanovém pravidlu.  Vyberte hodnotu „SpeakerTestAndPackaging“.  
4. Rozbalte sekci Podrobnosti.
5. V poli Produkt zadejte nebo vyberte hodnotu.
    * Vyberte volbu „L0050“.  
6. V poli Měrná jednotka zadejte nebo vyberte hodnotu.
    * Vyberte minuty.  
7. Do pole Doba realizace zadejte číslo.
    * Zadejte 5.  

## <a name="set-quantities"></a>Nastavit množství
1. Rozbalte sekci Množství.
2. Nastavte výchozí množství na „10“.
    * Jedná se o množství, které bude přeneseno pro každý kanban.  
3. Zaškrtněte políčko odchylky množství produktu.
    * Díky tomu lze dokončit vybrané kanbany s odchylkou od výchozího množství.  Umožňuje kanbany dokončit s množstvím od 8 do 12, obě odchylky nastaveny na 2.  
4. Nastavte odchylku menší než „2“.
    * To vám poskytne dokončení do 10 - 2 = 8  
5. Nastavte odchylku vyšší než „2“.
    * To vám poskytne dokončení až do 10 + 2 = 12  
6. V poli Pevné kanbanové množství zadejte číslo.
    * To je počet kanbanů, které mají být aktivní. V tomto případě 5 kanbanů zpracovává každých 10.  
7. V poli Minimální hranice výstrahy zadejte hodnotu „2“.
    * Slouží ke sledování minimálního množství plných kanbanů, které mají být na místě určení. Toto se například používá na přehled kanbanového množství.  
8. V poli Maximální hranice výstrahy zadejte hodnotu „4“.
    * Slouží ke sledování maximálního množství plných kanbanů, které mají být na místě určení. Toto se například používá na přehled kanbanového množství.  
9. Do pole Automaticky plánované množství zadejte hodnotu „1“.
    * Toto nastavení na 1 znamená, že každý kanban bude automaticky naplánován.   Pokud zadáme 3, kanbany nebudou plánovány, dokud nebudou prázdné 3 kanbany, které jsou připraveny pro plánování. To je užitečné pro seskupení práce a jako prevence velkého nastavování.  

## <a name="create-kanbans"></a>Vytvořit kanbany
1. Rozbalte sekci Kanbany.
2. Klikněte na položku Uložit.
    * Kanbanové pravidlo je třeba uložit, aby bylo možné vytvořit kanbany.  
3. Klepněte na možnost Přidat.
    * Všimněte si, že neexistují žádné aktivní kanbany, protože navržený Počet nových kanbanů je 5. To je stejné jako Pevné kanbanové množství.  
4. Klikněte na položku Vytvořit.
    * Dojde k vytvoření 5 kanbanů.  
    * Všimněte si, že 5 kanbanů po 10, bylo vytvořeno pro toto výrobní kanbanové pravidlo. Tento krok je posledním krokem v tomto postupu.  


