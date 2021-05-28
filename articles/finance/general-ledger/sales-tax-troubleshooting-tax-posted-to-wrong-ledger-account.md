---
title: Daň je v dokladu zaúčtovaná na nesprávný účet hlavní knihy
description: Toto téma poskytuje informace o řešení potíží, které mohou pomoci při zaúčtování daně na nesprávný účet hlavní knihy v dokladu.
author: qire
ms.date: 04/12/2021
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
ms.openlocfilehash: 3d197046bd547757f32712a50949b41897f6fedf
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020084"
---
# <a name="tax-is-posted-to-the-wrong-ledger-account-in-the-voucher"></a>Daň je v dokladu zaúčtovaná na nesprávný účet hlavní knihy

[!include [banner](../includes/banner.md)]

Daň se může během zaúčtování zaúčtovat na nesprávný účet hlavní knihy. Chcete-li tento problém vyřešit, postupujte podle pokynů v následujících částech. Příklady v tomto tématu používají jako obchodní dokument prodejní objednávku.

## <a name="find-the-tax-code-of-the-incorrectly-posted-tax-transaction"></a>Najděte daňový kód nesprávně zaúčtované daňové transakce

1. Na stránce **Transakce dokladu** vyberte transakci, se kterou chcete pracovat, a poté vyberte možnost **Zaúčtování DPH**.

    [![Tlačítko Zaúčtování DPH na stránce Transakce dokladu](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)

2. Zkontrolujte hodnotu v poli **Kód DPH**. V tomto příkladu je hodnota **DPH 19**.

    [![Pole Kód DPH na stránce Zaúčtování DPH](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)

## <a name="check-the-ledger-posting-group-of-the-tax-code"></a>Zkontrolujte skupinu účtování hlavní knihy kvůli daňovému kódu

1. Přejděte k nabídce **Daň** \> **Nepřímé daně** \> **DPH** \> **Kódy DPH**.
2. Najděte a vyberte daňový kód a poté zkontrolujte hodnotu v poli **Skupina účtování hlavní knihy**. V tomto příkladu je hodnota **DPH**.

    [![Pole Skupina zaúčtování hl. knihy na stránce Kódy DPH](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)

3. Hodnota v poli **Skupina zaúčtování hl. knihy** je prázdná. Chcete-li zobrazit podrobnosti o konfiguraci skupiny, vyberte odkaz. Případně vyberte a podržte (nebo klikněte pravým tlačítkem) v poli a poté vyberte **Zobrazit podrobnosti**.

    [![Příkaz Zobrazit podrobnosti](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)

4. V poli **DPH na výstup** ověřte správnost čísla účtu podle typu transakce. Pokud není správné, vyberte správný účet k zaúčtování. V tomto příkladu by měla být DPH prodejní objednávky zaúčtována na účet závazků DPH 222200.

    [![Pole Splatná DPH na stránce Skupiny zaúčtování hlavní knihy](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)

    Následující tabulka poskytuje informace o jednotlivých polích na stránce **Skupiny zaúčtování hlavní knihy**.

    | Pole                  | popis |
    |------------------------|-------------|
    | Splatné DPH      | Hlavní účet pro odchozí DPH (DPH splatnou finančnímu úřadu). |
    | DPH na vstupu   | Hlavní účet pro příchozí DPH (DPH přijímanou od finančního úřadu). |
    | Importní DPH – výdaj        | Hlavní účet, který se používá k zaúčtování odpočitatelné importní daně, kterou dodavatelé nevyžadují ani nehlásí daňovému úřadu jako součást daně ze zboží a služeb v Evropské unii (EU) / harmonizované DPH (HST). **Importní daň** musí být vybrána pro kód DPH ve skupině DPH, která je použitá v transakci. Toto pole nebude k dispozici v případě, že je vybrána možnost **Použít daňové předpisy pro DPH** na stránce **Parametry hlavní knihy**. |
    | Splatná importní DPH        | Hlavní účet, který se používá k účtování příchozích importních daní, které se platí finančním úřadům. |
    | Účet vyrovnání     | Hlavní účet, který se používá k zaúčtování čistého zůstatku účtů hlavní knihy, které jsou specifikovány v polích **Splatná importní DPH** a **Pohledávka DPH**. |
    | Platební sleva dodavatele   | Hlavní účet, který se používá pro zaúčtování slevy v hotovosti pro kódy DPH, které jsou přidružené k této skupině zaúčtování hlavní knihy. |
    | Platební sleva odběratele | Hlavní účet, který se používá pro zaúčtování slevy v hotovosti pro kódy DPH, které jsou přidružené k této skupině zaúčtování hlavní knihy. |

    Více informací naleznete v tématu [Nastavení účetních skupin pro DPH](tasks/set-up-ledger-posting-groups-sales-tax.md).

## <a name="debug-in-code-to-check-ledger-dimensions"></a>Ladění kódu pro kontrolu dimenzí hlavní knihy

V kódu je účet zaúčtování určen dimenzí hlavní knihy. Dimenze hlavní knihy uloží ID záznamu účtu do databáze.

1. U prodejní objednávky přidejte zarážku u metod **Tax::saveAndPost()** a **Tax::post()**. Věnujte pozornost hodnotě **\_LedgerDimension**.

    [![Ukázka kódu prodejní objednávky, která má zarážku](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)

    U nákupní objednávky přidejte zarážku u metod **TaxPost::saveAndPost()** a **TaxPost::postToTaxTrans()**. Věnujte pozornost hodnotě **\_LedgerDimension**.

    [![Ukázka kódu prodejní objednávky, která má zarážku](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)

2. Spuštěním následujícího dotazu SQL vyhledejte zobrazenou hodnotu účtu v databázi na základě ID záznamu uloženého dimenzí hlavní knihy.

    ```sql
    select * from DIMENSIONATTRIBUTEVALUECOMBINATION where recid={the value of _ledgerDimension}
    ```

    [![Zobrazená hodnota ID záznamu](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)

3. Prozkoumejte zásobník volání a zjistěte, kde je přiřazena hodnota **ledgerDimension**. Hodnota je obvykle od **TmpTaxWorkTrans**. V tomto případě byste měli přidat zarážku na **TmpTaxWorkTrans::insert()** a **TmpTaxWorkTrans::update()**, abyste zjistili, kde je přiřazená hodnota.

## <a name="determine-whether-customization-exists"></a>Zjištění, zda existuje přizpůsobení

Pokud jste dokončili kroky v předchozích částech, ale problém se vám nepodařilo vyřešit, zjistěte, zda existuje přizpůsobení. Pokud neexistuje žádné přizpůsobení, vytvořte požadavek na službu Microsoft pro další podporu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
