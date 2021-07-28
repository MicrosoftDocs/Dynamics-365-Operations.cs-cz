---
title: Daň se nevypočítá nebo je částka daně nulová
description: Toto téma poskytuje informace o řešení potíží, které mohou pomoci, když je částka daně 0 (nula) nebo se daň nevypočítá.
author: shtao
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: c731e0284b720394059384e21deea1ea4407718c
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6352803"
---
# <a name="tax-isnt-calculated-or-the-tax-amount-is-zero"></a>Daň se nevypočítá nebo je částka daně nulová

[!include [banner](../includes/banner.md)]

Transakce může mít částku řádku, která není 0 (nula), ale buď se nevypočítá daň, nebo vypočítaná částka daně je 0. Chcete-li tento problém vyřešit, postupujte podle pokynů v následujících částech.

## <a name="verify-that-tax-codes-are-correctly-selected-by-the-transaction"></a>Ověřte, zda jsou transakcí správně vybrány daňové kódy

Pokud transakce nevybírá správné daňové kódy nebo nevybírá žádné daňové kódy, daně z ní nebudou vypočítány. Podle následujícího postupu ověřte, zda jsou transakcí správně vybrány daňové kódy. 

1. Na řádku transakce na záložce s náhledem **Detaily řádku** na kartě **Nastavení** v části **DPH** ověřte, zda jsou v polích **Skupina DPH položky** a **Skupina DPH** vybrané správné daňové skupiny. Pokud nejsou vybrány správné daňové skupiny, vyberte je.

    [![Pole Skupina DPH zboží a Skupina DPH.](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)

2. Přejděte k nabídce **Daň** \> **Nepřímé daně** \> **DPH** \> **Skupiny DPH**.
3. Vyberte příslušnou skupinu DPH a poté si na záložce s náhledem **Nastavení** poznamenejte kód DPH v poli **Kód DPH**.

    [![Stránka Skupiny DPH.](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)

4. Přejděte k nabídce **Daň** \> **Nepřímé daně** \> **DPH** \> **Skupiny DPH položky**.
5. Vyberte příslušnou skupinu DPH položky a poté na záložce s náhledem **Nastavení** ověřte, že daňový kód v poli **Kód DPH** odpovídá daňovému kódu skupiny DPH.

    [![Stránka Skupiny DPH položky.](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)

6. Pokud se daňové kódy neshodují, aktualizujte kód DPH pro jednu ze skupin.

## <a name="verify-that-the-selected-tax-codes-arent-exempt-and-that-they-have-the-correct-tax-rate-value"></a>Ověřte, zda vybrané daňové kódy nejsou osvobozeny a zda mají správnou hodnotu sazby daně

Pokud jsou daňové kódy osvobozeny, nebo pokud je sazba daně 0 (nula), bude výsledek výpočtu daně 0. Postupujte podle těchto pokynů, abyste zjistili, zda jsou vybrané daňové kódy osvobozeny, a ověřte, zda se na ně vztahuje správná sazba daně.

1. Přejděte k nabídce **Daň** \> **Nepřímé daně** \> **DPH** \> **Skupiny DPH**.
2. Vyberte příslušnou skupinu DPH a poté na záložce s náhledem **Nastavení** ověřte, že není zaškrtnuto políčko **Osvobození**. Pokud je vybráno, vymažte jej.

    [![Zaškrtávací políčko Osvobození na stránce Skupiny DPH.](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)

3. Přejděte k nabídce **Daň** \> **Nepřímé daně** \> **DPH** \> **Kódy DPH**.
4. Vyberte příslušný kód DPH a poté ověřte, zda není sazba daně v poli **Hodnota** nastavena na 0 (nula). Pokud je 0, aktualizujte pole tak, aby bylo nastaveno na správnou sazbu daně.

    [![Pole Hodnota na stránce Hodnoty kódu DPH.](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)

## <a name="determine-whether-zero-is-the-correct-tax-amount"></a>Zjistěte, zda nula je správná částka daně

V některých scénářích je částka daně 0 (nula) správná. Pomocí těchto kroků zjistíte, zda 0 je správná částka daně pro vaši transakci.

1. Přejděte k nabídce **Hlavní kniha** \> **Nastavení hlavní knihy** \> **Parametry hlavní knihy**.
2. Na kartě **DPH** v poli **Metoda výpočtu** ověřte, že je vybrána možnost **Celkem**.

    [![Pole Metoda výpočtu na stránce Parametry hlavní knihy.](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)

3. Přejděte k nabídce **Daň** \> **Nepřímé daně** \> **DPH** \> **Kódy DPH**.
4. Vyberte příslušný kód DPH, vyberte možnost **Výpočet** \> **Základ marže** a ověřte, zda je základ marže nastaven na hodnotu **Čistá částka zůstatku faktury** nebo **Celková fakturovaná částka, včetně částek DPH**. Další informace viz [Celková fakturovaná částka, včetně částek DPH](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).
5. Pokud jsou v krocích 2 a 4 nastaveny správné hodnoty, určete, zda je celková částka transakce 0 (nula). Pokud je celková částka 0, je očekávaným výsledkem částka daně 0. Protože výpočet daně je založen na celkové částce zůstatku faktury a tato částka není řádek po řádku, bude částka daně 0 po výpočtu daně přidělena každému řádku.

## <a name="determine-whether-customization-exists"></a>Zjištění, zda existuje přizpůsobení

Pokud jste dokončili kroky v předchozích částech, ale problém se vám nepodařilo vyřešit, zjistěte, zda existuje přizpůsobení. Pokud neexistuje žádné přizpůsobení, vytvořte požadavek na službu Microsoft pro další podporu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
