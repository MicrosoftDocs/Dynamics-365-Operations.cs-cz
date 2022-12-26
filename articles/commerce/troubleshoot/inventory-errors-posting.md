---
title: Chyby při zaúčtování výkazu způsobené nedostupnými zásobami nebo konflikty při aktualizaci
description: Tento článek poskytuje možná řešení problémů souvisejících se zásobami během zaúčtování výpisu v Microsoft Dynamics 365 Commerce.
author: Shajain
ms.date: 12/19/2022
ms.topic: Troubleshooting
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.openlocfilehash: cebb890b42def6e9b002b01be63266b88bfc35a4
ms.sourcegitcommit: 4ad87483ba0bfea3e04fdb7e578d8abc34e607a4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2022
ms.locfileid: "9887623"
---
# <a name="statement-posting-errors-due-to-unavailable-inventory-or-update-conflicts"></a>Chyby při zaúčtování výkazu způsobené nedostupnými zásobami nebo konflikty při aktualizaci

[!include [banner](../../includes/banner.md)]

Tento článek poskytuje možná řešení problémů souvisejících se zásobami během zaúčtování výpisu v Microsoft Dynamics 365 Commerce.

## <a name="description"></a>popis

Během účtování transakcí Commerce se mohou zobrazit chybové zprávy související s problémy se zásobami nebo konflikty při aktualizacích.

### <a name="inventory-issues-error-message"></a>Chybová zpráva týkající se problémům se zásobami

Pokud narazíte na problémy se zásobami, zobrazí se chybová zpráva podobná tomuto příkladu:

> xx nelze vyskladnit, protože pouze yy jsou dostupné ze skladu.

### <a name="update-conflict-error-messages"></a>Chybové zprávy týkající se konfliktů při aktualizaci

Konflikt při aktualizaci může nastat, když metoda ocenění zásob je buď *standardní cena* nebo *klouzavý průměr*. Protože obě tyto metody představují trvalé účtování, konečná cena je určena v době zaúčtování.

Pokud používáte metodu *klouzavý průměr*, zobrazená chybová zpráva ohledně konfliktu při aktualizaci se podobá tomuto příkladu:

> Po výpočtu proporcionálních výdajů se neočekává hodnota zásob xx.xx

Pokud používáte metodu *standardní cena*, zobrazená chybová zpráva ohledně konfliktu při aktualizaci se podobá tomuto příkladu:

> Standardní náklady neodpovídají finanční hodnotě zásob po aktualizaci. Hodnota = xx.xx, množství = rr.rr, standardní cena = zz.zz

## <a name="resolutions"></a>Rozhodnutí

### <a name="workaround-for-the-inventory-error"></a>Řešení chyby zásob

Chybu zásob můžete zmírnit buď ruční aktualizací zásob pro danou položku, nebo povolením záporného fyzického skladu pro skupinu modelů položek, která je přidružena k položce v ústředí Commerce Headquarters.

Pro zajištění konzistentního účtování Microsoft doporučuje, abyste povolili záporný fyzický sklad u skupiny modelů položek. V některých případech se nebudou moci výkazy zaúčtovat, pokud není povolen záporný fyzický sklad.

Například pro položku nejsou k dispozici žádné zásoby, ale pokladník položku vrátí a poté ji přidá zpět do stejné transakce za sníženou cenu, aby napodobil cenovou shodu. V tomto případě budou transakce vrácení i prodejní transakce načteny do stejného výpisu objednávky jednoho zákazníka. Protože však neexistuje žádná záruka, že řádek vráceného zboží (který zvyšuje zásoby) bude zaúčtován před zaúčtováním řádku prodeje (který snižuje zásoby), může dojít k chybám zásob. Je-li v tomto případě povolen záporný fyzický sklad, zaúčtování transakce není negativně ovlivněno a systém bude správně odrážet zásoby.

#### <a name="enable-negative-physical-inventory-for-an-item-model-group"></a>Povolení záporného fyzického skladu pro skupinu modelů položek

Chcete-li povolit záporný fyzický sklad pro skupinu modelů položek v ústředí Commerce Headquarters, postupujte takto.

1. Přejděte do části **Řízení zásob \> Nastavení \> Zásoby**.
1. V levém navigačním podokně vyberte skupinu modelů položek.
1. V sekci **Zásady zásob** v části **Záporný sklad** vyberte zaškrtávací políčko **Záporný fyzický sklad**.

![Záporný fyzický sklad je povolen.](./media/Physical_Negative_Inventory.png)

### <a name="workaround-for-the-update-conflict-error"></a>Řešení chyby týkající se konfliktů aktualizace

Možná řešení, jak opravit chybu konfliktu aktualizací, naleznete v části [Konflikt aktualizace nastane, když metoda ocenění zásob je buď standardní cena nebo klouzavý průměr](/troubleshoot/dynamics-365/supply-chain/costing/update-conflict-standard-cost-moving-average-inventory-valuation).

> [!NOTE]
> V případě chyby konfliktu aktualizací nemusíte odstraňovat objednávky zákazníků, které byly vygenerovány pomocí agregačního kroku zaúčtování. Po implementaci navrhovaných řešení by měl být výkaz zaúčtován, pokud se znovu pokusíte o jeho zaúčtování.
