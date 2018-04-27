--- 
title: "Přidání existující aktivity k verzi výrobního toku"
description: "Při vytvoření nových verzí výrobních toků se můžete rozhodnout přidat aktivity vytvořené pro starší verze do nové verze."
author: cvocph
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: a74fb34db71ba4b539c1b6ede361329aaeb94920
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="add-an-existing-activity-to-a-production-flow-version"></a>Přidání existující aktivity k verzi výrobního toku

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Při vytvoření nových verzí výrobních toků se můžete rozhodnout přidat aktivity vytvořené pro starší verze do nové verze. Tato procedura ukazuje, jak je vytvořena nová verze pro stávající výrobní tok bez kopírování aktivit. V dalším kroku je přidána existující aktivita do nové verze. 

Tento úkol vyžaduje výrobní tok s verzí a již vytvořenými aktivitami.


## <a name="create-a-new-production-flow-version"></a>Vytvořit novou verzi výrobního toku
1. Přejděte na Řízení výroby > Nastavení > Tok štíhlé výroby > Výrobního toky.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. Klikněte na odkaz na vybraném řádku v seznamu.
4. Klikněte na možnost Upravit.
5. Označte v seznamu vybraný řádek.
6. Do pole Datum vypršení platnosti zadejte datum a čas.
    * Všimněte si, že před vytvořením nové verze výrobního toku je třeba zkontrolovat datum vypršení platnosti a čas aktivní verze. Nová verze bude vytvořena s datem začátku platnosti, které se připojuje k datu vypršení platnosti vybrané verze.  
7. Klepněte na možnost Přidat.
8. Vyberte Ne v poli Kopírovat z verze.
    * Vyberte Ne, chcete-li začít prázdnou verzí, pokud většina aktivit zkopírované verze bude nahrazeno novými aktivitami. Ručně přidejte nezměněné aktivity k funkci Přidat existující ve formuláři Aktivita.  
9. Vyberte Ne v poli Duplicitní kanbanová pravidla.
    * Když aktivity nejsou zkopírovány do nové verze, není možné kopírovat kanbanová pravidla v době vytvoření nové verze.   Místo toho budete používat funkci vytvoření náhradního kanbanu později ve formuláři kanbanového pravidla pro nahrazení kanbanových pravidel staré verze toku produkce kanbanovými pravidly používajícími aktivity nové verze.  
10. Klikněte na tlačítko OK.
11. Vyhledejte na seznamu požadovaný záznam a vyberte ho.

## <a name="add-an-existing-activity"></a>Přidání existující aktivity
1. Klepněte na aktivity.
2. Klepnutím na možnost Přidat existující otevřete dialogové okno.
    * Najděte a vyberte existující aktivitu, kterou chcete přidat do nové verze výrobního toku.  Všimněte si, že v seznamu jsou uvedeny všechny aktivity, které byly vytvořeny pro tento výrobní tok pro všechny předchozí verze toku.  
3. V poli Aktivita zadejte nebo vyberte hodnotu.
4. Klikněte na tlačítko OK.


