---
title: Přidružení dlouhodobého majetku k leasingům
description: V tématu je vysvětleno, jak přidružit existující dlouhodobý majetek k novému leasingu.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseDetail
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: bd55d433b0961b8b210b9c28d7340ff880635a85
ms.sourcegitcommit: 3af457fc216bd0020843291ca57fd379acb53c96
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/17/2021
ms.locfileid: "7392467"
---
# <a name="associate-fixed-assets-with-leases"></a>Přidružení dlouhodobého majetku k leasingům

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

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

Pokud je k dlouhodobému majetku přidružen leasing, pole **Životnost** v knize dlouhodobého majetku bude aktualizováno tak, aby odpovídalo nejmenší hodnotě z následujících kritérií: 

 - Očekávaná doba použitelnosti majetku
 - Doba trvání leasingu z přidružené knihy leasingu

Pokud je pole **Převod vlastnictví** nastaveno na **Ano** u leasingové knihy, hodnota v poli **Doba životnosti** bude vždy očekávanou dobou použitelnosti aktiva. 
 
Životnost se bude aktualizovat při každé úpravě leasingu, aby bylo zajištěno, že používaný majetek bude odepisován po dobu trvání leasingu, jako by byl odepisován při leasingu majetku.

> [!NOTE]
> Pokud přidružíte dlouhodobý majetek k leasingu, tlačítka **Odpis majetku** a **Snížení hodnoty leasingu** jsou v leasingu majetku deaktivována. Transakce odpisů majetku a snížení hodnoty leasingu si můžete prohlédnout v části Dlouhodobý majetek. Tlačítko **Transakce majetku**, které otevírá formulář dotazu, je také deaktivováno. Můžete také otevřít formulář dotazu **Transakce majetku** v části Dlouhodobý majetek.  

Stránky **Dlouhodobý majetek** a **Kniha dlouhodobého majetku** zobrazí ID leasingu, které je spojeno s dlouhodobým majetkem. Pokud je k leasingu přidružen dlouhodobý majetek, ID leasingu a popis leasingu se zobrazí na pevné záložce **Informace o leasingu** na stránce **Dlouhodobý majetek**. U knih dlouhodobého majetku, které jsou přiřazeny ke knihám leasingu, pole **ID leasingu**, **Popis leasingu** a **Typ knihy** zobrazí informace o zvolené knize dlouhodobého majetku na pevné záložce **Informace o leasingu**, aby označily, že je spojena s knihou leasingu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
