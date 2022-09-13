---
title: Ruční zpracování výjimek z prodeje a vychystávání linky převodu
description: Tento článek popisuje, jak mohou správci ručně vybrat (nebo zrušit výběr) transakce zásob, aby opravili problémy způsobené poškozenými daty prodejních a převodních objednávek.
author: perlynne
ms.date: 08/19/2022
ms.topic: article
ms.search.form: WHSManualSalesLinePicking, WHSManualInventTransferLinePicking, InventTransPick, WHSLoadLineManualCorrection, WHSTroubleshootingSelfService
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: d2f89a7109060e69aca6a06eadaedc017728bbae
ms.sourcegitcommit: 0220be95c007c77ba3b73fed8ac68a3d72dc2884
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403651"
---
# <a name="manually-handle-sales-and-transfer-line-picking-exceptions"></a>Ruční zpracování výjimek z prodeje a vychystávání linky převodu

[!include [banner](../includes/banner.md)]

Ruční zpracování výjimek z prodejních a převodních řádků umožňuje správcům opravit problémy, které jsou způsobeny poškozenými daty prodejních a převodních objednávek. Umožňuje důvěryhodným uživatelům ručně vybírat (nebo odebírat) transakce zásob, které souvisejí s řádky prodejních a převodních objednávek, zatímco skladové procesy již probíhají.

Zde popsaná funkce by měla být použita pouze v případech, kdy systém nemůže dokončit zpracování zásobníku skladových procesů obvyklým způsobem. Ve výchozím nastavení ji mohou používat pouze uživatelé, kteří mají roli správce systému. Přístup k němu však můžete udělit přiřazením oprávnění *Ruční výběr prodejních řádků* k jiným rolím, jak požadujete.

## <a name="turn-on-this-feature-for-your-system"></a>Zapnutí této funkce ve vašem systému

Než budete moci použít některou z funkcí popsaných v tomto článku, je třeba je v systému zapnout. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav těchto funkcí a zapnout je. V pracovním prostoru **Správa funkcí** jsou tyto funkce uvedeny pod následujícími názvy:

- *Služba ručního výdeje řádku prodeje pro správce nebo podobné důvěryhodné uživatele*<br>(Od verze Supply Chain Management 10.0.25 je tato funkce povinná a nelze ji vypnout.)
- *Služba ručního výdeje řádku převodu pro správce nebo podobné důvěryhodné uživatele*

## <a name="correct-transactions-related-to-sales-or-transfer-order-lines"></a>Oprava transakcí souvisejících s řádky prodejních nebo převodních příkazů

Následující postup použijte k opravě transakcí, které souvisejí s řádky prodejních nebo převodních příkazů.

1. V závislosti na typu objednávky, kterou musíte opravit, proveďte jeden z těchto kroků:

    - Chcete-li opravit transakci, která souvisí s prodejní objednávkou, přejděte na **Warehouse Management \> Periodické úkoly \> Uklidit \> Ruční výběr prodejního řádku**.
    - Chcete-li opravit transakci, která souvisí s objednávkou převodu, přejděte na **Warehouse Management \> Periodické úkoly \> Uklidit \> Ruční výběr řádků převodu**.

1. Na stránce **Ruční výběr prodejních řádků** nebo **Ruční výběr řádků přenosu** pomocí filtrů v horní části mřížky najděte řádek, který hledáte, a poté vyberte řádek cílové objednávky v horní mřížce.
1. Použijte karty **Transakce se zásobami**, **Řádky vkládání**, **Řádky práce** a **Řádky kontejneru** ve spodní části k zobrazení dalších informace o vybraném řádku. Informace na těchto kartách poskytují základní přehled o souvisejících skladových procesech a jejich stavech.
1. V podokně akcí vyberte **Vybrat** k otevření vybraného řádku objednávky na stránce **Vybrat** pro transakce se zásobami. Tento krok můžete provést i pro řádky objednávek, které již byly uvolněny na sklad. (Řádky objednávek, které byly uvolněny do skladu, obvykle nelze otevřít na stránce **Vybrat**.)

    > [!NOTE]
    > Při otevření stránky **Vybrat** můžete obdržet různá varování. Proveďte jakoukoli akci, kterou tato varování doporučují. Můžete například obdržet varování o řádcích objednávek, které jsou propojeny s prací ve skladu. V tomto případě má smysl pokusit se zrušit práci pomocí standardní funkce [zrušit práci](cancel-warehouse-work.md), než provedete ruční opravu.

1. Vyberte řádek v mřížce **Transakce** a poté vyberte **Přidat řádek výběru** na panelu nástrojů **Transakce**.
1. Vybraný řádek se přesune do mřížky **Řádky výběru**. Nastavte příslušné hodnoty pro všechny sloupce, ve kterých chybí požadované informace. (Například určete umístění a registrační značku, ze kterých má být položka vybrána/odvybrána.)
1. Vyberte **Potvrdit výběr všech** na panelu nástrojů **Řádky výběru**.

## <a name="correct-load-line-quantities"></a>Opravy množství na řádcích nákladu

Následujícím postupem opravíte množství řádku nákladu.

1. V závislosti na typu objednávky, kterou musíte opravit, proveďte jeden z těchto kroků:

    - Chcete-li opravit transakci, která souvisí s prodejní objednávkou, přejděte na **Warehouse Management \> Periodické úkoly \> Uklidit \> Ruční výběr prodejního řádku**.
    - Chcete-li opravit transakci, která souvisí s objednávkou převodu, přejděte na **Warehouse Management \> Periodické úkoly \> Uklidit \> Ruční výběr řádků převodu**.

1. Na stránce **Ruční výběr prodejních řádků** nebo **Ruční výběr řádků přenosu** pomocí filtrů v horní části mřížky najděte řádek, který hledáte, a poté vyberte řádek cílové objednávky v horní mřížce.
1. Na kartě **Řádky nákladu** ve spodní části vyberte **Upravit řádky nákladu ručně** na panelu nástrojů.
1. Na stránce **Upravit řádky výběru ručně** v mřížce **Transakce se zásobami** zkontrolujte transakce zásob, které se týkají vybraného řádku výběru.
1. V horní mřížce opravte podle potřeby množství řádku výběru v následujících sloupcích:

    - **Množství vytvořené práce**
    - **Vyskladněné množství**
    - **Plánované množství pro cross docking**

    Systém ověří všechny změny, které v těchto sloupcích provedete.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
