---
title: Rozdělení zákazníka v plánech fakturace
description: Tento článek popisuje, jak rozdělit zákazníka při použití fakturace předplatného.
author: JodiChristiansen
ms.date: 11/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-11-05
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: cfbe61ca4b7e809a8183f4622bf6db4fc83a4d83
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746309"
---
# <a name="customer-split-on-billing-schedules"></a>Rozdělení zákazníka v plánech fakturace

V plánu fakturace je *fakturační účet* zákazník, který obdrží fakturu prodejní objednávky, aby mohl zaplatit fakturu. V některých scénářích může fakturu zaplatit více než jeden zákazník. Funkce **Rozdělení zákazníků** umožňuje přidat další zákazníky, kterým lze fakturovat stejný fakturační plán. Chcete-li povolit tuto funkci, přejděte na **Fakturace předplatného \> Opakovaná fakturace smlouvy \> Nastavení \> Parametry opakované fakturace smlouvy** a nastavte možnost **Rozdělení zákazníků** na **Ano**.

## <a name="customer-split-on-the-billing-schedule-header"></a>Rozdělení zákazníka v hlavičce plánů fakturace

Po vytvoření plánu fakturace lze do záhlaví plánu fakturace přidat další zákazníky.

Chcete-li přidat zákazníka, postupujte takto:

1. Na kartě **Plán fakturace** vyberte **Rozdělit zákazníka**. Pole **Zákaznický účet** a **Název zákaznického účtu** v horní části specifikují zákazníka, který je přiřazen jako **Zákazník plánu fakturace**.

    > [!NOTE]
    > Účet zákazníka, který přidáte, nemůže být stejný jako účet faktury.

2. Na kartě **Řádky rozdělení zákazníka** vyberte **Přidat řádek**.
3. Vyberte zákazníka a poté zadejte procento každé faktury pro tohoto zákazníka.
4. Ve výchozím nastavení se jako počáteční a koncové datum používají počáteční a koncové datum fakturačního plánu. Pokud nový zákazník zaplatí zadané procento pouze za část rozvrhu fakturace, zadejte různá data zahájení a ukončení. Pokud má například plán fakturace datum zahájení 1. ledna a datum ukončení 31. prosince a novému zákazníkovi je účtováno 40 procent za prvních devět měsíců, zadejte 1. leden jako počáteční datum a 30. září jako datum ukončení a **40,00** jako procento.

Nemůžete přidat více než jednoho zákazníka do řádků rozdělení zákazníka. V tomto případě nesmí celkové zadané procento přesáhnout 100 procent. Zadejte zákaznické reference a zákaznické požadavky jako informační pole, která se zobrazí na řádku prodejní objednávky během procesu **Vygenerovat fakturu**.

Podrobnosti řádku zobrazí kontaktní informace, dodací adresu, fakturační adresu a platební údaje přidaných zákazníků. Tyto informace se zákazníkům zobrazí také na prodejní objednávce.

Když do záhlaví plánu fakturace přidáte informace o rozdělení zákazníků, pokud jsou v plánu fakturace řádky nevyfakturovaného plánu fakturace, zobrazí se následující zpráva, která vás vyzve ke stažení změn: „Chcete stáhnout změnu z záhlaví k řádkům? Změny aktualizují pouze řádky fakturačního plánu, které nejsou účtovány." Vyberte **Ano** k aktualizaci informací o rozdělení zákazníků na řádku plánu fakturace. Změny nebudou aktualizovány, pokud byl řádek plánu fakturace již vyúčtován.

Pokud je plán fakturace vytvořen pomocí možnosti **Kopírovat plán**, budou výchozí informace zadány na řádky záhlaví rozdělení zákazníka. Nemůže být stejný jako zákaznický účet.

Když je dokončen proces **Vygenerovat fakturu**, vytvoří se více prodejních objednávek. (Při použití automatického účtování bude také vytvořeno více prodejních faktur.) Tyto prodejní objednávky a prodejní faktury lze zobrazit na kartě **Faktura** na pevné záložce **Podrobnosti řádku** na strně **Zobrazit detail fakturace**. **Násobek** se zobrazí na řádku podrobností fakturace, což znamená, že bylo vytvořeno více prodejních objednávek a prodejních faktur.

## <a name="customer-split-on-billing-schedule-lines"></a>Rozdělení zákazníka na řádcích plánu fakturace

Rozdělení zákazníků lze přidat k jednotlivým řádkům plánu fakturace, pokud chcete rozdělit pouze konkrétní řádky plánu fakturace. Vyberte zaškrtávací políčko **Rozdělení zákazníka** na řádku a poté vyberte **Rozdělení zákazníka** v nabídce pro řádek plánu fakturace pro aktualizaci nebo zadání informací o rozdělení zákazníků.

Informace o auditu se aktualizují, pokud byl plán fakturace již vyúčtován, ale poté bylo procento změněno na řádku plánu fakturace. Všechny řádky, které budou účtovány po této změně, budou používat nové procento.

> [!NOTE]
> - Možnost rozdělení zákazníka nelze použít u skladových produktů.
> - Pokud je zaškrtnuto políčko **Nevyfakturované příjmy**, políčko **Rozdělení zákazníka** nelze zaškrtnout.
> - Pokud použijete možnost **Pouze rozdělení příjmů**, nadřazený řádek má možnost **Rozdělení zákazníka**, ale podřízené řádkové položky nikoli.
