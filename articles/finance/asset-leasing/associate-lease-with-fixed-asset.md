---
title: Přidružení dlouhodobého majetku k leasingům
description: V tématu je vysvětleno, jak přidružit existující dlouhodobý majetek k novému leasingu.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0e2261755d98ee38564b4b864daf8e79551d1239
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814073"
---
# <a name="associate-fixed-assets-with-leases"></a>Přidružení dlouhodobého majetku k leasingům

[!include [banner](../includes/banner.md)]

V tématu je vysvětleno, jak přidružit existující dlouhodobý majetek k novému leasingu. Když přidružíte dlouhodobý majetek k leasingu, bude hodnotou používaného majetku při počátečním uznání pořizovací cena dlouhodobého majetku.

Než budete moci přidružit dlouhodobý majetek k leasingu, musíte vytvořit záznam pro dlouhodobý majetek v části Dlouhodobý majetek. Pak na stránce **Shrnutí leasingu** musíte vytvořit leasing a propojit majetek s tímto leasingem.

1. Přidejte leasing podle pokynů v části [Přidání nebo kopírování leasingů](add-lease.md). Na stránce **Přidat leasing** v poli **Číslo dlouhodobého majetku** vyberte majetek, který ještě nebyl získán.
2. Vyberte **Knihy** a potvrďte platební kalendář.
3. Vyberte **Počáteční uznání**.
4. Vyberte **Deník leasingu majetku**.

    Položka deníku počátečního uznání pro leasing debetuje dlouhodobý majetek pro částku, která je obvykle debetována z účtu používaného majetku.

    Nyní můžete zobrazit typ transakce a knihu pro dlouhodobý majetek.

5. Vyberte **Podrobnosti deníku**.
6. Vyberte **Řádky** pro zobrazení jednotlivých řádků pro položku deníku.
7. Vyberte řádek deníku, který obsahuje majetek, a poté vyberte kartu **Dlouhodobý majetek**.

    Karta **Dlouhodobý majetek** ukazuje typ transakce a knihu. Ve výchozím nastavení je pole **Typ transakce** nastaveno na **Pořizovací cena** a pole **Kniha** je nastaveno na aktuální knihu pro dlouhodobý majetek.

Po zaúčtování položky deníku počátečního uznání se transakce zobrazí jako transakce pořízení pro dlouhodobý majetek. Chcete-li zobrazit tabulku transakcí, přejděte na **Dlouhodobý majetek \> Dlouhodobý majetek \> Dlouhodobý majetek**, vyberte příslušný majetek a poté vyberte **Ocenění**. Měli byste vidět, že položka deníku počátečního uznání vytvořila transakci pořízení pro zadaný dlouhodobý majetek.

Dlouhodobý majetek lze nyní odepisovat pomocí standardní funkce odpisování v části Dlouhodobý majetek. Další informace o odpisech naleznete v tématu [Odpisové metody a způsoby odpisu](../fixed-assets/depreciation-methods-conventions.md).

> [!NOTE]
> Pokud přidružíte dlouhodobý majetek k leasingu, tlačítka **Odpis majetku** a **Snížení hodnoty leasingu** jsou v leasingu majetku deaktivována. Transakce odpisů majetku a snížení hodnoty leasingu si můžete prohlédnout v části Dlouhodobý majetek. Tlačítko **Transakce majetku**, které otevírá formulář dotazu, je také deaktivováno. Můžete také otevřít formulář dotazu **Transakce majetku** v části Dlouhodobý majetek.  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]