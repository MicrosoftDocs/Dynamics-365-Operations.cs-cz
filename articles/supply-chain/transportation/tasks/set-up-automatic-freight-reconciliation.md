---
title: Nastavení automatického odsouhlasení dopravného
description: Tato procedura ukazuje, jak nastavit data pro automatické odsouhlasení dopravného.
author: ShylaThompson
manager: tfehr
ms.date: 10/16/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSFreightBillType, TMSFreightBillTypeAssignment, TMSCarrierCodeLookup, DefaultDashboard, TMSAuditMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6f11edc15821faad84485d5b81e4a9ded0b7e974
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423599"
---
# <a name="set-up-automatic-freight-reconciliation"></a>Nastavení automatického odsouhlasení dopravného

[!include [banner](../../includes/banner.md)]

Tato procedura ukazuje, jak nastavit data pro automatické odsouhlasení dopravného. Obvykle to provádějí vedoucí skladu. Tento postup můžete projít v ukázkových datech společnosti USMF.


## <a name="set-up-the-freight-bill-type"></a>Nastavení typu účtu dopravného
1. Přejděte do nabídky Správa přepravy > Nastavení > Odsouhlasení dopravného > Typ účtu dopravného.
    * Typ kusovníku dopravného definuje, jak by měly být spárovány účty za dopravné a faktury dopravce.  
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Typ účtu dopravného.
4. Do pole Sestavení modulu zadejte Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer.
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

