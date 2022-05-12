---
title: Šablony rozdělení výnosů fakturace předplatného
description: Toto téma vysvětluje, jak nastavit šablony rozdělení výnosů pro položky, které se prodávají jako sady.
author: JodiChristiansen
ms.date: 04/21/2022
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
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 5c2eb6c8e18770eb149c445f662ab7a90aad81a7
ms.sourcegitcommit: 367e323bfcfe41976e5d8aa5f5e24a279909d8ac
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/29/2022
ms.locfileid: "8660449"
---
# <a name="revenue-split-templates-in-subscription-billing"></a>Šablony rozdělení výnosů fakturace předplatného

Na stránce **Šablona rozdělení výnosů** nastavíte šablony pro rozdělení výnosů. Rozdělení výnosů se skládá z nadřazené položky, která má podřízené položky. Tento typ položky se často prodává zákazníkům jako jedna položka nebo sada.

Například položku počítače lze vytvořit následujícím způsobem:

- **Nadřazená položka:** Stříbrné předplatné
- **Rozepsané (podřízené) položky:**

    - Podpora
    - Údržba
    - Licence

Při vytváření nadřazené položky mějte na paměti následující omezení:

- Položka může být určena jako nadřazená pouze jednou.
- Nadřazenou položku lze vybrat jako podřízenou ve stejné šabloně.
- Platná šablona vyžaduje alespoň jednu podřízenou položku.
- Položku lze zadat jako podřízenou pro více než jednu položku sady.
- Každý vztah nadřazená-podřízená položka musí být jedinečný.

## <a name="create-a-parent-item-that-has-child-items"></a>Vytvoření nadřazené položky, která má podřízené položky

Podle následujícího postupu vytvoříte nadřazenou položku, která má podřízené položky.

1. Na stránce **Šablona rozdělení výnosů** vyberte **Nový**.
1. V poli **Nadřazená položka** vyberte nadřazenou položku. Pole **Číslo odchylky** je aktualizováno automaticky. Hodnotu v tomto poli můžete podle potřeby měnit.
1. Poté vyberte metodu přidělení v poli **Metoda přidělení**.
1. V seznamu **Položky komponenty** tlačítkem **Přidat** přidáte podřízené položky.
1. Pokud jste v poli **Metoda přidělení** vybrali **Procento**, do pole **Procento** zadejte hodnotu procenta.

    - Pokud jste v poli **Metoda přidělení** vybrali **Stejná částka**, pole **Procento** se automaticky aktualizuje, takže každá položka má stejné procento.
    - Pokud jste v poli **Metoda přidělení** vybrali **Variabilní částka**, **Nulová nadřazená částka** nebo **Nulová částka**, hodnota pole **Procento** zůstává **0** (nula) a nelze ji změnit.

1. Zvolte možnost **Uložit**.

## <a name="fields"></a>Pole

Stránka **Šablona rozdělení výnosů** obsahuje následující pole.

| Pole | Popis |
|-------|-------------|
| Nadřazená položka | Vyberte číslo položky. Tato položka se stane nadřazenou položkou pro položku sady, kterou vytvoříte. |
| Název produktu | Název produktu. |
| Metoda přidělení | <p>Vyberte metodu přidělení:</p><ul><li>**Stejná částka** – Procenta přidělení se vypočítají automaticky a rovnoměrně rozdělí mezi všechny položky v šabloně.</li><li>**Procento** – Pro přidělení můžete zadat procentuální částku. Součet všech procent se musí rovnat 100.</li><li>**Variabilní částka** – Podřízené položky, které jsou přidány, mají čistou částku 0 (nula). Cena podřízených položek musí být specifikována na úrovni transakce.</li><li>**Nulová částka** – Nadřazená položka si ponechává svou jednotkovou cenu a čistou částku. Všechny podřízené položky mají čistou částku 0 (nula).</li><li>**Nulová nadřazená částka** – Nadřazená položka má pevnou čistou částku 0 (nula). Se všemi podřízenými položkami se zachází jako se standardními položkami. Neprobíhá žádné ověření, zda součet částek podřízených položek se rovná částce nadřazené položky.</li></ul> |
| **Položky komponenty** | |
| Položka komponenty | Vyberte číslo položky. Tato položka je podřízená. |
| Číslo varianty | Pro položku vyberte číslo varianty. |
| Název produktu | Název produktu. |
| Procento | <p>Procento přidělení pro milník:</p><ul><li>Pokud je pole **Metoda přidělení** nastaveno na **Procento**, můžete zadat procento.</li><li>Pokud je pole **Metoda přidělení** nastaveno na **Stejná částka**, procento se automaticky vypočítá, takže každá položka v šabloně má stejné procento.</li><li>Pokud je pole **Metoda přidělení** je nastaveno na **Variabilní částka**, **Nulová nadřazená částka** nebo **Nulová částka**, procento je 0 (nula) a nelze je upravit.</li></ul><p>Hodnota tohoto pole může být libovolné kladné číslo mezi 0 (nulou) a 100. Součet všech procent se musí rovnat 100.</p> |
| Celkové procento | <p>Součet hodnot ve sloupci **Procento**.</p><ul><li>Pokud je pole **Metoda přidělení** nastaveno na **Stejná částka** nebo **Procento**, součet všech procent se musí rovnat 100.</li><li>Pokud je pole **Metoda přidělení** je nastaveno na **Variabilní částka**, **Nulová nadřazená částka** nebo **Nulová částka**, celkové procento je 0 (nula).</li></ul> |

## <a name="revenue-split-on-a-sales-order"></a>Rozdělení výnosů na prodejní objednávce

Chcete-li vytvořit prodejní objednávku, která obsahuje položku, která je nastavena pro rozdělení výnosů, postupujte takto.

1. Na stránce **Prodejní objednávka** vytvořte prodejní objednávku.
2. Na řádku pro každou položku, která je nastavena pro rozdělení příjmů, zaškrtněte políčko **Rozdělení výnosů**. Tato položka se stane nadřazenou položkou. Pokud je šablona již nastavena, podřízené položky se automaticky zobrazí v seznamu.
3. Chcete-li přidat další podřízené položky, vyberte **Přidat podřízenou položku rozdělení výnosů** a vyberte podřízenou položku, kterou chcete přidat.
4. Uložte objednávku.

## <a name="revenue-split-with-billing-schedules"></a>Rozdělení příjmů podle plánů fakturace

Chcete-li vytvořit plán fakturace, který obsahuje položku, která je nastavena pro rozdělení výnosů, postupujte takto.

1. Na stránce **Všechny/aktivní plány fakturace** vytvořte plán fakturace.
2. Na řádku pro každou položku, která je nastavena pro rozdělení příjmů, zaškrtněte políčko **Rozdělení výnosů**. Tato položka se stane nadřazenou položkou. Pokud je šablona již nastavena, podřízené položky se automaticky zobrazí v seznamu.
3. Chcete-li přidat další podřízené položky, vyberte **Přidat podřízenou položku rozdělení výnosů** a vyberte podřízenou položku, kterou chcete přidat.
4. Pokračujte kroky pro práci s plánem fakturace.

> [!NOTE]
> Pokud je možnost **Automaticky vytvořit rozdělení výnosů** nastavena na **Ano** na stránce **Parametry opakované fakturace smlouvy**, dojde k následujícím akcím:
>
> - Pokud je řádková položka nastavena jako nadřazená v šabloně rozdělení výnosů, automaticky je zaškrtnuto políčko **Rozdělení výnosů**.
> - Podřízené položky jsou automaticky zadány do řádku prodejní objednávky nebo plánu fakturace.
>
> Pokud je možnost **Automaticky vytvořit rozdělení výnosů** nastavena na **Ne**, příslušné chování je vysvětleno dříve.
