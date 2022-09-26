---
title: Označení dávky jako K dispozici nebo Není k dispozici pomocí kódů dispozice dávky
description: Tento článek popisuje, jak nastavit a používat kódy dispozice dávky k označení dávek jako K dispozici nebo Není k dispozici, což využijete při hlavním plánování, rezervacích, výdeji nebo expedici.
author: t-benebo
ms.date: 09/16/2022
ms.topic: article
ms.search.form: PdsDispositionMaster, InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-16
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: cfb0743a573550de93d75063df517e0c143f2568
ms.sourcegitcommit: 20ce54cb40290dd116ab8b157c0a02d6757c13f5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/20/2022
ms.locfileid: "9542465"
---
# <a name="use-batch-disposition-codes-to-mark-batches-as-available-or-unavailable"></a>Označení dávky jako K dispozici nebo Není k dispozici pomocí kódů dispozice dávky

Tento článek popisuje, jak nastavit a používat *kódy dispozice dávky*. Každý kód dispozice dávky má stav *K dispozici* nebo *Není k dispozici*. Kódy dispozice dávky přiřadíte k dávkám zásob, abyste označili, zda jsou jednotlivé dávky k dispozici pro hlavní plánování, rezervaci, výdej nebo expedici.

Chcete-li použít kódy dispozice dávky, musíte nastavit kódy a přiřadit je k dávkám, které chcete spravovat.

## <a name="set-up-batch-disposition-codes"></a>Nastavení kódů dispozice dávky

Musíte nastavit každý kód dispozice dávky, který chcete použít ve vašem systému. Můžete vytvořit tolik kódů, kolik chcete. (Můžete například vytvořit kódy pro označení různých důvodů, proč může nebo nemůže být dávka k dispozici.) Často však budete mít pouze dva kódy: jeden pro stav *K dispozici* a jeden pro stav *Není k dispozici*. Můžete také vytvořit vlastní kódy, které umožňují použití dávky jen pro některé operace, ale ne pro jiné.

Kódy dispozice dávky nastavíte dle těchto kroků.

1. Přejděte do nabídky **Řízení zásob \> Nastavení \> Dávka \> Vzor dispozice dávky**.
1. Stránka **Vzor dispozice dávky** obsahuje seznam vašich aktuálních kódů dispozice dávky a umožňuje je vytvářet, odstraňovat a upravovat. Proveďte jeden z následujících kroků:

    - Chcete-li upravit existující kód, vyberte jej v podokně seznamu.
    - Chcete-li vytvořit nový kód, v podokně Akce vyberte **Nový**.

1. V záhlaví nového nebo vybraného kódu nastavte následující pole:

    - **Kód dispozice dávky** – Zadejte zobrazovaný název kódu.
    - **Popis** – Popište způsob použití kódu.
    - **Stav dispozice dávky** – Vyberte stav, který platí pro dávky, ke kterým je kód přiřazen:

        - *Není k dispozici* – Dávky nelze použít pro hlavní plánování, rezervaci, výdej nebo expedici. Když vyberete tuto hodnotu, všechny možnosti **blokování** na záložce s náhledem **Nastavení** jsou nastaveny na *Ano* a všechny **možnosti čisté hodnoty** jsou nastaveny na *Ne*. Některá z těchto nastavení však můžete změnit a přidat výjimky.
        - *K dispozici* – Dávky lze použít pro hlavní plánování, rezervaci, výdej nebo expedici. Když vyberete tuto hodnotu, všechny možnosti **blokování** na záložce s náhledem **Nastavení** jsou nastaveny na *Ne* a všechny **možnosti čisté hodnoty** jsou nastaveny na *Ano*. Zatímco je pole **Stav dispozice dávky** nastaveno jako *K dispozici*, tato nastavení jsou pouze pro čtení.

1. Pokud nastavíte pole **Stav dispozice dávky** jako *Není k dispozici*, můžete přizpůsobit stav blokování každé operace (rezervace, výdej a expedice) pro každý typ objednávky (prodej, převod a výroba). U výrobních zakázek můžete zablokovat nebo odblokovat deník výrobních výdejek. Můžete také zablokovat nebo odblokovat hlavní plánování. Pomocí možností na záložce s náhledem **Nastavení** můžete zablokovat nebo odblokovat každou operaci podle potřeby. Nastavením **Možnosti čisté hodnoty** na *Ano* povolíte hlavní plánování, nebo jejím nastavením na *Ne* zablokujete hlavní plánování.

## <a name="assign-batch-disposition-codes-to-batches"></a>Přiřazení kódů dispozice dávky k dávkám

Po definování kódů dispozice dávky šarží je přiřaďte k dávkám dle následujícího postupu.

1. Přejděte na **Řízení skladu \> Nastavení \> Zásoby \> Dávky**.
1. Vyberte jednu nebo více dávek, kterým chcete přiřadit kód dispozice dávky.
1. V podokně akcí na kartě **Obnovit** zvolte **Obnovit kód dispozice dávky**.
1. V dialogovém okně **Změna omezení skladové dávky** nastavte pole **Nový kód dispozice dávky** na název kódu, který chcete přiřadit.
1. Volbou **OK** použijete nové nastavení a uložíte provedené změny.

    Na stránce **Dávky** jsou aktualizovány hodnoty ve sloupcích **Kód dispozice dávky** a **Stav dispozice dávky** tak, aby odpovídaly novým nastavením pro vybrané dávky.

## <a name="master-planning-example"></a>Příklad hlavního plánování

Tento příklad ukazuje, jak mohou kódy dispozice dávky ovlivnit hlavní plánování.

V tomto příkladu jsou kódy dispozice dávky nastaveny následujícím způsobem:

- *P-K dispozici:*

    - **Stav dispozice dávky:** *K dispozici*
    - **Možnost čisté hodnoty:** *Ano*

- *P-Není k dispozici:*

    - **Stav dispozice dávky:** *Není k dispozici*
    - **Možnost čisté hodnoty:** *Ne*

Existuje produkt (*Produkt-1*), který má dvě dávky: *Dávka-A* a *Dávka-B*. Tyto dávky jsou nastaveny následujícím způsobem:

- *Dávka-A:*

    - **Kód dispozice dávky:** *P-K dispozici*
    - **Množství na skladě:** 1

- *Dávka-B:*

    - **Kód dispozice dávky:** *P-Není k dispozici*
    - **Množství na skladě:** 1

Pro množství 2 produktu *Produkt-1* existuje prodejní objednávka (*PO1)*. Termín dodání je tři dny ode dneška.

Spustíte hlavní plánování a nastavíte následující hodnoty, které jsou relevantní pro tento příklad:

- **Plánovaná objednávka:** *Nákupní objednávka*
- **Strategie doplnění:** *Požadavek*
- **Doba realizace:** *0*

V důsledku běhu plánování systém použije dostupnou dávku (*Dávka-A*) na pokrytí množství 1 produktu *Produkt-1* pro prodejní objednávku *PO1*. Nemůže však použít dávku *Dávka-B*, protože tato dávka je pro plánování označena jako Není k dispozici. Proto pro pokrytí zbývajícího množství systém vytvoří plánovanou nákupní objednávku (*PNO1*) pro novou dávku produktu *Produkt-1*.

Následující obrázek znázorňuje časovou osu pro výsledek plánování.

![Příklad, který ukazuje, jak mohou kódy dispozice dávky ovlivnit hlavní plánování.](media/batch-codes-planning-example.png "Příklad, který ukazuje, jak mohou kódy dispozice dávky ovlivnit hlavní plánování")
