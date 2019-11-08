---
title: EUR-00015 Nastavení DIČ
description: Tato procedura vás provede předpoklady registrace DIČ, jako je nastavení typu registrace a jeho přiřazení kategorii registrace.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxRegistrationType, TaxRegistrationTypeCreate, TaxRegistrationLegislationTypes
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 127e6caf6a6273df36f580b32fa81219b88b8a29
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183472"
---
# <a name="eur-00015-set-up-vat-id"></a>EUR-00015 Nastavení DIČ

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tato procedura vás provede předpoklady registrace DIČ, jako je nastavení typu registrace a jeho přiřazení kategorii registrace. Další informace o ID registrace a zpracování ID registrace, včetně povinných požadavků, najdete v tématu nápovědy věnovaném ID registrace a zpracování ID registrace. 

Informace zde uvedené se vztahují na všechny evropské země/oblasti. Tento úkol byl vytvořen za použití ukázkových dat společnosti DEMF s primární adresou právnické osoby v Německu. Tento úkol je určen pro správce systému. Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.

1. Přejděte na položky Správa organizace > Globální adresář > Typy registrace > Typy registrace.
2. Kliknutím na možnost Nový otevřete dialogové okno.
3. Do pole Název zadejte DIČ.
4. Do pole Popis zadejte Číslo DPH.
5. V poli Země/oblast zadejte nebo vyberte hodnotu DEU.
6. Vyberte Ano v poli Jedinečný.
    * Zaškrtněte toto políčko, chcete-li ověřit, zda je DPH jedinečná.  
7. Vyberte možnost Primární v poli Země.
    * Toto políčko zaškrtněte, pokud bude DIČ platit pro všechny adresy patřící do určené země nebo regionu.  
8. Klikněte na položku Vytvořit.
9. Klepněte na možnost Přidat.
10. V poli Země/oblast zadejte nebo vyberte hodnotu ITA.
11. Do pole formát napište '###########'.
    * Při zadání ID registrace tohoto typu pro vybranou zemi nebo oblast bude ID registrace ověřeno na základě tohoto formátu.  
12. Zaškrtněte políčko Jedinečné.
    * Zaškrtněte toto políčko, chcete-li ověřit, zda je DPH jedinečná.  
13. Zaškrtněte políčko Primární pro zemi.
    * Toto políčko zaškrtněte, pokud bude DIČ platit pro všechny adresy patřící do určené země nebo regionu.  
14. Klikněte na položku Uložit.
15. Přejděte na položky Správa organizace > Globální adresář > Typy registrace > Kategorie registrace.
16. Klikněte na položku Nová.
17. V poli Země/oblast zadejte nebo vyberte hodnotu DIČ, DEU.
18. V poli kategorie registrace vyberte DIČ.
    * Přiřaďte typ registrace, který jste vytvořili dříve, k předdefinované kategorii registrace.  
19. Klikněte na položku Nová.
20. V poli Země/oblast zadejte nebo vyberte hodnotu DIČ, ITA.
21. V poli kategorie registrace vyberte DIČ.
    * Přiřaďte typ registrace, který jste vytvořili, k předdefinované kategorii registrace.  
22. Klikněte na položku Uložit.
