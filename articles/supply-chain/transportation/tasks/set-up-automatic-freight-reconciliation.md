--- 
title: "Nastavení automatického odsouhlasení dopravného"
description: "Tato procedura ukazuje, jak nastavit data pro automatické odsouhlasení dopravného."
author: BibiSp
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 97f0c4d8fe06ab2fc252b9543cb688306214c79f
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-automatic-freight-reconciliation"></a>Nastavení automatického odsouhlasení dopravného

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tato procedura ukazuje, jak nastavit data pro automatické odsouhlasení dopravného. Obvykle to provádějí vedoucí skladu. Tento postup můžete projít v ukázkových datech společnosti USMF.


## <a name="set-up-the-freight-bill-type"></a>Nastavení typu účtu dopravného
1. Přejděte do nabídky Správa přepravy > Nastavení > Odsouhlasení dopravného > Typ účtu dopravného.
    * Typ kusovníku dopravného definuje, jak by měly být spárovány účty za dopravné a faktury dopravce.  
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Typ účtu dopravného.
4. Do pole sestavení modulu zadejte "Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer".
    * Toto je standardní knihovna kódu modulu odpovídající řízení přepravy.  
5. Do pole Třída modulu zadejte "Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer".
    * Toto je standardní třída modulu odpovídající řízení přepravy.  
6. Klikněte na položku Nová.
7. V poli Popis vyberte hodnotu, která by měla odpovídat hodnotě na účtu dopravného a faktuře dopravce.  
8. V poli Párování požadováno vyberte Ano.
    * Pokud nastavíte do tohoto pole hodnotu Ano, znamená to, že hodnota vybraná v poli Popis musí odpovídat faktuře za dopravu i faktuře dopravce. Pokud je nastavena na hodnotu Ne, může být pole na jedné z nich prázdné.  
9. Klikněte na položku Uložit.

## <a name="set-up-the-freight-bill-type-assignment"></a>Nastavení přiřazení typu účtu dopravného
1. Zavřete stránku.
2. Přejděte do nabídky Správa přepravy > Nastavení > Odsouhlasení dopravného > Přiřazení typů účtu dopravného.
    * Přiřazení typu účtu dopravného se používá k určení, jaký typ účtu dopravného se používá pro konkrétní dopravce.   
3. Klikněte na položku Nová.
4. V poli Režim zadejte nebo vyberte hodnotu.
5. V poli Dopravce dodávky zadejte nebo vyberte hodnotu.
6. V poli Typ účtu dopravného vyberte typ účtu dopravného, který jste vytvořili dříve.
7. Zavřete stránku.

## <a name="set-up-the-audit-master"></a>Nastavení hlavního auditu
1. Přejděte do nabídky Správa přepravy > Nastavení > Odsouhlasení dopravného > Hlavní audit.
    * Hlavní audit definuje přípustné limity pro automatické odsouhlasení dopravného. Určuje, o kolik se mohou lišit peněžní částky na účtu dopravného a faktuře dopravce, a umožňuje odsouhlasení. Také definuje, jak zpracovat nesrovnalosti.  
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole ID hlavního auditu.
4. V poli Dopravce dodávky vyberte stejného dopravce dodávky jako dříve.
5. V poli Typ účtu dopravného vyberte typ účtu dopravného, který jste vytvořili dříve.
6. Rozbalte oddíl Tolerance.
7. V poli Minimální úroveň tolerance zadejte číslo.
8. V poli Maximální úroveň tolerance zadejte číslo.
9. Rozbalte sekci Výsledek.
10. V poli Kód důvodu přeplatku zadejte nebo vyberte hodnotu.
    * Pokud se peněžní částky na účtu dopravného a faktuře dopravce liší, kódy důvodu přeplatku či nedoplatku určují účty, na kterých má být registrován rozdíl, dokud je rozdíl v rámci úrovní tolerance.  
11. V poli Kód důvodu nedoplatku zadejte nebo vyberte hodnotu.
12. Zavřete stránku.


