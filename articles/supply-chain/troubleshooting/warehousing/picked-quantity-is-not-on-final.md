---
title: Zásilku nemůžete potvrdit, protože položky nebyly vybrány
description: Zásilku nemůžete potvrdit, protože položky nebyly vybrány
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f3ebd47ffc85d4ca257b404579d60d679f7929b6
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301298"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a>Zásilku nemůžete potvrdit, protože položky nebyly vybrány

Kód chyby: LoadNotPickedAndMovedToFinalShippingLocation

## <a name="symptoms"></a>Příznaky

Když se pokusíte potvrdit dodávku, systém zobrazí následující chybovou zprávu:

> Některé položky, které jsou nezbytné pro vytížení %1, dosud nebyly vyzvednuty a přesunuty na konečné skladové místo.

Proto nemůžete potvrdit dodání pro zásilku.

## <a name="cause"></a>Příčina

Dodávku nebo zásilku nelze v aktuálním stavu potvrdit, protože může existovat jedna z následujících podmínek:

- Související práce ještě nebyly vybrány a přesunuty na konečné místo dodání.
- Vybrané množství práce neodpovídá vytvořenému množství práce na řádku dodávky.
- Direktiva umístění byla nakonfigurována s umístěním balení jako konečné místo odeslání při použití kontejnerizace šablony vlny.

## <a name="resolution"></a>Řešení

Náklad nebo zásilka je aktuálně ve stavu, kdy se potvrzení zásilky nezdaří. Chcete-li problém opravit, proveďte jeden nebo více z následujících úkolů:

- Zkontrolujte řádky nákladu a ujistěte se, že všechny související práce byly dokončeny na konečném místě přepravy a že množství odpovídá
- Zrušte ID práce, která byla vytvořena s umístěním balení jako konečné místo odeslání, překonfigurujte direktivu umístění a znovu uvolněte náklad.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Zkontrolujte řádky nákladu a ujistěte se, že všechny související práce byly dokončeny na konečném místě přepravy a že množství odpovídá

Pomocí následujících kroků zkontrolujte řádky nákladu a ujistěte se, že všechny související práce byly dokončeny na konečném místě přepravy a že množství odpovídá

1. Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.
1. Vyberte dodávku, pro kterou nelze potvrdit odeslání.
1. Na záložce s náhledem **Řádky nákladu** vyberte řádek nákladu.
1. Poznamenejte si hodnotu pole **Množství vytvořených prací**.
1. V podokně akcí na kartě **Náklady** ve skupině **Související informace** vyberte **Práce**.
1. Ověřte, že práce byla dokončena na konečném místě přepravy a že vybrané množství práce odpovídá vytvořenému množství práce na řádku zatížení.
1. Tento postup opakujte pro všechny řádky nákladů, abyste se ujistili, že jsou splněna všechna kritéria.

### <a name="cancel-the-work-ids-that-have-been-created-with-the-packing-location-as-the-final-shipping-location-reconfigure-the-location-directive-and-rerelease-the-load"></a>Zrušte ID práce, která byla vytvořena s umístěním balení jako konečné místo odeslání, překonfigurujte direktivu umístění a znovu uvolněte náklad

Pomocí následujícího postupu zrušíte ID práce, která mají místo balení jako konečné umístění s automatizovanou kontejnerizací.

1. Přejděte k nabídce **Řízení skladu \> Periodické úkoly \> Vyčistit \> Zrušit práci**.
1. Otevře se dialogové okno **Zrušit práci**. Do pole **ID práce** zadejte ID práce, kterou chcete zrušit. Vybrané ID práce musí mít hodnotu **Pracovní stav** nastavenou na *Otevřeno*, *Probíhá*, *Zrušeno*, *Kombinovaéý* nebo *Uzavřeno*.
1. Vyberte **OK**.
1. Vyberte možnost **Ano** k potvrzení, že chcete práci zrušit.
1. Podle potřeby opakujte tento postup pro další ID práce.

Další informace viz [Zrušení práce skladu pro zpracování výjimek](../../warehousing/cancel-warehouse-work.md).

Pomocí následujícího postupu překonfigurujte direktivu umístění, takže při nastavení automatické kontejnerizace pro šablonu vlny nepoužije umístění balení jako konečné místo odeslání.

1. Přejděte na **Řízení skladu \> Nastavení \> Směrnice skladového místa**.
1. V poli **Typ pracovního příkazu** vyberte možnost *Prodejní objednávky*.
1. Vyberte direktivu umístění, kterou používáte pro automatizovanou kontejnerizaci.
1. Na panelu nástrojů záložky s náhledem **Akce směrnic skladového místa** vyberte možnost **Upravit dotaz**.
1. V dialogovém okně editoru dotazů na kartě **Oblast** najděte řádek, kde je **Pole** nastaveno na *Profil umístění* a ověřte, že pole **Kritéria** pro tento řádek není nastaveno na profil polohy, který má **Typ umístění** nastaveno na *Balení*. Upravte pole **Kritéria** pro opravu konečného skladového místa.

Pomocí následujícího postupu znovu uvolněte náklad a vytvořte pracovní ID se správným konečným místem odeslání.

1. Přejděte do **Řízení skladu \> Náklady \> Pracovní plocha plánování nákladu**.
1. V sekci **Náklady** vyhledejte náklad, který je třeba uvolnit.
1. Na panelu nástrojů v sekci **Náklady** vyberte **Uvolnění \> Uvolnění do skladu** pro uvolnění vybraného nákladu do skladu.
1. Podle potřeby opakujte tento postup pro další náklady.
