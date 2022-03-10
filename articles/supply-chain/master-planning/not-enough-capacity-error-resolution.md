---
title: Oprava chyby modulu plánování „Nebyla nalezena dostatečná kapacita“ a končené kapacity
description: Toto téma poskytuje informace o důvodech a řešeních chyby „výrobní zakázky“ %1 nebylo možné naplánovat. Chyba modulu plánování „Nebyla nalezena dostatečná kapacita“
author: ChristianRytt
ms.date: 7/29/2021
ms.topic: article
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-19
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: becd537d37a8ba8931f2598dccbae8554a4d168e
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985023"
---
# <a name="fix-the-not-enough-capacity-could-be-found-scheduling-engine-error"></a>Opravte chybu modulu plánování „Nebyla nalezena dostatečná kapacita“

[!include [banner](../includes/banner.md)]

Při spuštění plánování se může zobrazit následující chybová zpráva:

> Výrobní zakázku %1 se nepodařilo naplánovat. Nebyla nalezena dostatečná kapacita.

Existuje několik důvodů, proč může plánovací modul selhat a vydat tuto chybovou zprávu. Toto téma poskytuje pokyny, které vám pomohou najít hlavní příčinu chyby a poté ji zmírnit.

## <a name="review-the-applicable-resources"></a>Zkontrolujte příslušné zdroje

K chybě může dojít, pokud požadavky na provoz v místě výrobní zakázky nesplňují žádné použitelné zdroje.

Pokud chcete zkontrolovat příslušné zdroje, postupujte následovně.

1. Jděte na **Kontrola produkce \> Výrobní zakázky \> Všechny výrobní zakázky** a otevřete nebo vyberte výrobní zakázku, kterou nelze naplánovat.
1. V podokně akcí na kartě **Výrobní objednávka** ve skupině **Podrobnosti prodeje** zvolte **Odhad**.
1. Na stránce **Výrobní trasa** vyberte operaci a poté v podokně akcí vyberte **Použitelné zdroje**.
1. V dialogovém okně **Použitelné zdroje** nastavte pole **Použít požadavky pro** na *Plánování operací* nebo *Plánování práce*, v závislosti na typu plánování, které používáte.
1. Ujistěte se, že v místě výrobní zakázky jsou příslušné zdroje.

## <a name="review-the-calendars-that-are-associated-with-resources"></a>Projděte si kalendáře související se zdroji

K chybě může dojít, pokud není ke zdroji nebo skupině zdrojů přidružen žádný kalendář nebo pokud přidružený kalendář není správně nastaven (například nemá žádnou pracovní dobu nebo jeho účinnost v procentech je 0 \[nula\]).

Chcete -li ověřit, že je kalendář přiřazen ke zdroji nebo skupině zdrojů, postupujte takto.

1. Jděte na **Kontrola produkce \> Výrobní zakázky \> Všechny výrobní zakázky** a otevřete nebo vyberte výrobní zakázku, kterou nelze naplánovat.
1. V podokně akcí na kartě **Výrobní objednávka** ve skupině **Podrobnosti prodeje** zvolte **Odhad**.
1. Na stránce **Výrobní trasa** vyberte operaci a poté v podokně akcí vyberte **Použitelné zdroje**.
1. V dialogovém okně **Použitelné zdroje** vyberte zdroj a poté vyberte **Zobrazit zdroj**. Případně vyberte a podržte (nebo klikněte pravým tlačítkem) v poli **Skupina zdrojů** a pak vyberte **Zobrazit podrobnosti**.
1. Na stránce **Zdroje** nebo **Skupiny zdrojů** na záložce s náhledem **Kalendáře** se ujistěte, že je ke zdroji nebo skupině zdrojů přidružen kalendář.

> [!NOTE]
> Pokud k chybě dojde během plánování operací, musíte se ujistit, že je kalendář přidružen ke všem příslušným skupinám zdrojů.

Chcete -li zkontrolovat nastavení kalendáře, postupujte takto.

1. Jděte na **Správa organizace \> Nastavení \> Kalendáře \> Kalendáře** a vyberte kalendář, který je přidružen ke zdroji nebo skupině zdrojů.
1. V podokně akcí zvolte **Pracovní doba**.
1. Na stránce **Pracovní doba** se ujistěte, že stránka není prázdná. Kromě toho se ve dnech, které vás zajímají, ujistěte, že pole **Kontrola** není nastaveno na *Zavřeno*, existuje pracovní doba a pole **Účinnost je v procentech** není nastaveno na *0* (nula).

Pokud je kalendář přidružen k základnímu kalendáři, musíte také zkontrolovat nastavení základního kalendáře.

> [!NOTE]
> V plánování operací se kalendář skupiny zdrojů používá k určení časů zahájení a dat ukončení každé operace. Také omezuje dobu, kterou může systém naplánovat pro jednu konkrétní operaci na jeden konkrétní den v jedné konkrétní skupině zdrojů. Pokud je například pracovní doba pro skupinu zdrojů v jeden konkrétní den od 8:00 do 16:00, zatížení, které jedna operace na skupinu prostředků přenese, nesmí překročit zatížení, které se vejde do osmi hodin, bez ohledu na množství dostupné kapacity, kterou má skupina zdrojů v daný den. Dostupná kapacita však může dále omezit zatížení.

## <a name="review-the-scheduling-parameters"></a>Pojďme si projít parametry plánování.

Aby byl zajištěn dobrý výkon, modul pro plánování bude hledat zdroj pouze po určitou dobu a určitý počet konfliktů plánování.

Chcete -li zkontrolovat parametry plánování, postupujte podle těchto kroků.

1. Přejděte do nabídky **Správa organizace \> Nastavení \> Parametry plánování**.
1. Proveďte jeden z následujících kroků:

    - Pokud je možnost **Časový limit plánování povolen** nastavena na *Ne*, přejděte ke kroku 3.
    - Pokud je možnost **Časový limit plánování povolen** nastavena na *Ano*, zvyšte hodnotu v poli **Maximální doba plánování na sekvenci**, aby zpracování mělo více času na dokončení.

1. Proveďte jeden z následujících kroků:

    - Pokud je možnost **Časový limit optimalizace plánování povolen** nastavena na *Ne*, přejděte ke kroku 4.
    - Pokud je možnost **Časový limit optimalizace plánování povolen** nastavena na *Ano*, zvyšte hodnotu v poli **Časový limit pokusů o optimalizaci**, aby zpracování mělo více času na dokončení.

1. Pokud jste na stránce změnili některá nastavení, přeplánujte objednávku a zkuste to znovu.

## <a name="review-capacity"></a>Kontrola kapacity

K chybě může dojít, když provádíte konečné plánování, ale není k dispozici žádná volná kapacita.

Chcete-li provést nekonečné plánování kapacity, postupujte následovně.

1. Jděte na **Kontrola produkce \> Výrobní zakázky \> Všechny výrobní zakázky** a vyberte nebo otevřete výrobní zakázku, kterou nelze naplánovat.
1. V podokně akcí na kartě **Plán** ve skupině **Výrobní zakázka** vyberte **Naplánovat operace** nebo **Naplánovat úlohy**.
1. V dialogovém okně **Plánování operací** nebo **Plánování zakázek** nastavte možnost **Konečná kapacita** na *Ne*.
1. Výběrem **OK** naplánujte příkaz.

Chcete-li zkontrolovat dostupnou kapacitu zdroje, postupujte takto.

1. Jděte na **Správa organizace \> Zdroje \> Zdroje** a vyberte zdroj, který je použitelný pro objednávku, kterou nelze naplánovat.
1. V podokně akcí na kartě **Zdroje** ve skupině **Zobrazení** vyberte **Zatížení kapacity** nebo **Zatížení kapacity, graficky**, a ujistěte se, že je k dispozici kapacita.

Chcete-li zkontrolovat dostupnou kapacitu skupiny zdrojů, postupujte následovně.

1. Jděte na **Správa organizace \> Zdroje \> Skupiny zdrojů** a vyberte skupinu zdrojů, která je použitelnýá pro objednávku, kterou nelze naplánovat.
1. V podokně akcí na kartě **Skupina zdrojů** ve skupině **Zobrazení** vyberte **Zatížení kapacity** nebo **Zatížení kapacity, graficky**, a ujistěte se, že je k dispozici kapacita.

## <a name="master-planning-books-a-resource-when-the-resource-calendar-is-closed"></a>Hlavní plánování rezervuje zdroj, když je kalendář zdrojů uzavřen

Při použití plánování operací bude hlavní plánování plánovat kapacitu podle kalendáře primární skupiny zdrojů. Rezervuje sekundární operaci současně s primární operací a nebere v úvahu kalendáře ani kapacitu sekundární operace. To může mít za následek naplánování výrobní zakázky v uzavřeném kalendáři nebo v době, kdy sekundární operace není k dispozici (kalendář uzavřen, není kapacita).

Při použití plánování úloh bude hlavní plánování při plánování zakázky brát v úvahu kapacitu a kalendář primární i sekundární operace. Aby mohla být objednávka naplánována, musí být kalendáře zdrojů obou operací otevřené a mít volnou kapacitu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
